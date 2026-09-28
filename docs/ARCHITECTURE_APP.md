# L'architecture d'une app Kete

> **Statut : proposition.** Pile tranchée : tout en TypeScript (D-016). Découpage par features et
> écrans conçus pour chaque métier (D-015). Règles de conception : `CONCEPTION.md`.

## 1. La forme : un monolithe modulaire

Une app Kete est **un seul déploiement**, découpé en **modules métier**. Pas de microservices :
une personne et ses agents doivent pouvoir tout comprendre.

| App | Modules métier |
|---|---|
| Nettio | clients, dépôts, atelier, caisse, agences |
| Firmo | messages, devis, factures, clients, modèles |
| Nyatefe | [À DÉFINIR AVEC L'AUTEUR] |
| Kete Cockpit | produits, événements, santé, attention, brief |

## 2. Les couches, dans chaque module

| Couche | Contient | Dépend de |
|---|---|---|
| **Surfaces** | Web (PWA), API, MCP, espace opérateur, webhooks, worker | Application |
| **Application** | Les cas d'usage (« créer un dépôt ») et les politiques d'accès | Domaine, ports |
| **Domaine** | Les règles du métier, les états, les événements de domaine | Rien |
| **Ports** | Les interfaces : dépôt de données, paiement, messages, fichiers, IA, événements | — |
| **Adaptateurs** | Base Neon, Compte Kete, Chariow, e-mail, stockage, outbox, modèle d'IA | Ports |

Les dépendances pointent **vers le domaine**. Aucun nom de fournisseur dans le domaine ni dans
l'application. **Toutes les surfaces appellent les mêmes cas d'usage** : un geste fait depuis Claude
passe par les mêmes règles que depuis l'écran.

## 3. L'arborescence

```
nettio/
├── CLAUDE.md                     contexte + renvoi à la doctrine kete
├── kete.json                     le manifeste (contrat manifest.v1)
├── package.json · tsconfig.json · vite.config.ts · drizzle.config.ts
├── docs/
│   ├── ARCHITECTURE.md           vue d'ensemble + schéma (Mermaid)
│   ├── decisions/                0001-titre.md, une décision par fichier
│   ├── flows/                    paiement, brouillon validé, hors ligne (séquences)
│   └── generated/                base, capacités, événements, API : générés, ne pas éditer
├── src/
│   ├── features/                 ← une feature = un dossier
│   │   ├── deposits/
│   │   │   ├── README.md         rôle, cycle de vie (schéma), commandes, capacités
│   │   │   ├── deposit.record.ts le schéma unique (Zod)
│   │   │   ├── domain/           règles : prix, acompte, transitions
│   │   │   ├── commands/         create-deposit.ts · mark-ready.ts · cancel-deposit.ts
│   │   │   ├── queries/          deposits-of-the-day.ts
│   │   │   ├── policies.ts       qui a le droit de faire quoi
│   │   │   ├── infrastructure/   deposit.table.ts (Drizzle) · deposit.repository.ts
│   │   │   ├── ui/               DepositForm.tsx · DepositCard.tsx · DepositList.tsx
│   │   │   ├── capabilities.ts   gestes exposés à l'agent, avec leur autonomie
│   │   │   ├── events.ts         ce que la feature annonce
│   │   │   ├── index.ts          sa seule porte d'entrée publique
│   │   │   └── __tests__/
│   │   ├── customers/  workshop/  cashier/  agencies/  pricing/
│   ├── routes/                   pages TanStack Start, fines (URL en français : /depots)
│   │   ├── __root.tsx
│   │   ├── _app/depots/index.tsx · _app/depots/$id.tsx
│   │   └── verification/$draftId.tsx
│   ├── server/                   api/ (REST /api/v1) · mcp/ · admin/ · webhooks/
│   ├── worker/                   outbox, rappels, résumé quotidien (pg-boss)
│   ├── platform/                 câblage : auth, base, adaptateurs, outbox, brouillons, i18n
│   └── shared/                   argent, identifiants, dates
├── db/migrations/                chaque table créée avec sa politique RLS
├── messages/                     fr.json, en.json : aucune chaîne en dur
└── tests/                        rls/ · e2e/ · evals/
```

## 4. Ce que le châssis fournit, ce que l'app écrit

| Le châssis (`kete-core`) fournit | L'app écrit |
|---|---|
| Connexion au Compte Kete, lecture du jeton, organisation active | Ses rôles métier et leur traduction |
| Outbox, événements signés, `/health`, manifeste | Ses événements métier et `metrics.daily` |
| Table et écran des brouillons de l'agent (préparé, corrigé, vérifié, refusé) | Ce que l'agent peut préparer |
| Module de l'espace opérateur, audit | Ses gestes d'opérateur métier |
| Déclaration des capacités MCP | Ses capacités |
| Ports et adaptateurs : paiement, messages, fichiers, IA | Rien : elle les utilise |
| Design system, i18n, bouton de retour | Ses écrans métier |

## 5. Les règles de données

- **Postgres (Neon), une base par app.** Chaque table porte `organization_id`.
- **RLS dans la migration créatrice.** L'app se connecte avec un rôle sans contournement de RLS ;
  l'organisation active est posée pour chaque requête.
- **Tables communes** fournies par le châssis : `kete_outbox`, `drafts`, `audit_log`,
  `idempotency_keys`.
- **Références externes par identifiant** : personne et organisation du Compte Kete, jamais de
  copie de leur profil (on lit les paramètres génériques dans Mon espace Kete).

## 6. Les droits

- Le jeton donne : la personne, l'organisation active, son rôle d'organisation, ses apps.
- L'app traduit en **rôle métier** (gérant, caissier…), éventuellement par agence.
- Chaque cas d'usage vérifie une **politique** côté serveur, pour toutes les surfaces.
- Un **agent** agit avec les droits de la personne, jamais plus, et selon l'échelle d'autonomie.

## 7. Le hors ligne (pour les apps qui en ont besoin, comme Nettio)

- Les écrans lisent un cache local (IndexedDB) et écrivent des **commandes** dans une file locale,
  chacune avec une clé d'idempotence.
- Au retour du réseau, les commandes sont rejouées sur le serveur, qui reste l'autorité ; une
  règle de conflit est écrite par commande.

## 8. L'IA dans l'app

- L'agent appelle une **capacité** ; si elle engage, elle crée un **brouillon** au lieu d'agir.
- Le lien de vérification ouvre l'écran du brouillon ; chaque champ montre sa provenance.
- La validation exécute le **même cas d'usage** que l'écran, et elle est tracée.
- Les corrections sont conservées comme apprentissages ; le modèle d'IA passe par un port.

## 9. Qualité et exploitation

- **Tests** : domaine (purs), cas d'usage avec adaptateurs factices, isolation RLS entre deux
  organisations en CI, contrats d'événements, bout en bout, évaluations des skills.
- **Une image, deux rôles** (web, worker), comme Pono ; migrations au démarrage avec le rôle
  propriétaire.
- **Préversion par pull request** avec une branche Neon ; mise en production via Pono.
- **Journaux structurés**, erreurs dans GlitchTip, `/health`, résumé quotidien vers Cockpit.

## 10. Les apps existantes

Firmo, Nettio et Nyatefe ne sont pas réécrites d'un coup. Elles rejoignent cette architecture par
étapes : manifeste et `/health`, puis outbox et événements, puis Compte Kete, puis ports de
paiement et brouillons.
