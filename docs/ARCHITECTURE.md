# Architecture

## Les couches

```
Qui s'en sert     Toi et ton équipe      Commerçants          Entreprises
Guichets          Kete Ops (MCP)         Kete (MCP)           Socle de l'entreprise
Ce qui tourne     Kete Cockpit           Kete Apps            Kete Enterprise (une instance chacune)
La fabrique       contrats · SDK · capacités · châssis · design · Pono pour chaque changement
Infra commune     GitHub · Coolify · Neon · Infisical · surveillance · sauvegardes · Moneroo
```

## Trois règles

1. **Chaque produit est autonome** : il fonctionne même si Kete Cockpit ou un guichet tombe.
2. **Rien ne traverse les organisations** : chaque entreprise a son instance et son guichet ; Kete
   ne voit que des agrégats.
3. **Tout changement de code passe par Pono** : garde-fous, validation humaine, retour arrière.

## Kete Cockpit

La plateforme d'administration des produits (la « plateforme centrale » des premières réflexions).
Kete en est le premier client.

- **Ce qu'il détient** : le registre des apps, un miroir minimal des personnes et des abonnements,
  les événements métier, des instantanés quotidiens, les points d'attention, les échéances,
  l'audit, les rapports.
- **Ce qu'il ne détient pas** : les données métier des apps, les mots de passe, les données de
  paiement, les logs détaillés (restés dans les outils).
- **Sorties** : brief du matin (Telegram), alertes, console (mobile d'abord), MCP.
- **V0** : registre, réception des événements, sondes de santé, instantanés, brief, MCP en lecture.
  Multi-organisation et RLS dès la première migration.

## Les contrats

Chaque app respecte des contrats versionnés (JSON Schema), sources de vérité des SDK :

| Contrat | Contenu |
|---|---|
| `manifest.v1` | Identité de l'app, environnements, santé, événements émis, capacités |
| `event.v1` | Enveloppe d'événement signée (HMAC horodaté) |
| `health.v1` | État de l'app et de ses dépendances |
| `admin.v1` | API admin standard : rechercher, suspendre, reprendre, prolonger un essai, accès support |
| `capability.v1` | Un geste métier : public, entrée, niveau d'autonomie, réversibilité |

Les apps écrivent leurs événements dans une **outbox** de leur propre base, envoyée par lots : si
Cockpit tombe, rien ne bloque l'utilisateur. Les concepts sont alignés sur ceux de KYA-Platform,
sans en copier le code tant que la propriété n'est pas réglée.

## Les trois niveaux d'administration

| Niveau | Qui | Où |
|---|---|---|
| Admin du client | Le patron du pressing | Dans l'app, propre au métier |
| Espace opérateur Kete | Le support Kete | Dans l'app, section protégée, via un module commun |
| Transverse | L'auteur, pour tout le portefeuille | Kete Cockpit |

L'accès d'un opérateur au compte d'un client est limité dans le temps, motivé, audité et **visible
par le client**.

## Les guichets MCP

- **Kete Ops** : les gestes d'opérateur de tous les produits, pour l'équipe Kete.
- **Kete** : les capacités des apps auxquelles un commerçant est abonné ; premier utilisateur :
  l'agent WhatsApp de Kete.
- **Le socle de chaque entreprise** : ses outils, ses apps, ses MCP.

Chaque produit **déclare ses capacités une seule fois** ; les guichets les exposent, vérifient les
droits et appliquent le niveau d'autonomie. Jamais de guichet commun à plusieurs organisations.

## Identité

- **Commerçants** : un Compte Kete par numéro de téléphone et code à usage unique (Better Auth,
  base de Neon Auth ; vérifier que Neon Auth expose le plugin).
- **Entreprises** : l'identité du socle (Neon Auth), et pour les outils tiers Entra ID si
  Microsoft 365, sinon Zitadel ou Authentik.
- **Opérateurs Kete** : identité séparée, double authentification.
- Pas de Keycloak par défaut.

## Paiement

**Moneroo** (orchestration, ne détient pas l'argent) derrière une interface `PaymentProvider` du
châssis. Chaque client garde son propre compte marchand. Les renouvellements vivent dans un module
du châssis. Stripe pour les cartes internationales si besoin.

## Infrastructure

- Trois zones sur Coolify : **ops** (Cockpit, surveillance, notifications), **produits**,
  **clients**.
- Surveillance de disponibilité sur un **VPS séparé**.
- Sauvegardes restic vers un stockage externe, **restauration testée**.
- Catalogue d'outils open source validés pour les entreprises, choisis sur la qualité de leur API
  plutôt que sur leur interface (les outils deviennent implicites derrière les capacités).
