# Architecture

> Ce qui est **tranché** renvoie à une décision (`D-xxx`). Ce qui est marqué **proposition** attend
> la validation de l'auteur.

## 1. Les principes d'architecture

1. **Générique d'abord (D-014).** Le code métier parle à des **ports** (interfaces) ; les
   fournisseurs vivent dans des **adaptateurs**. Aucun nom de fournisseur dans le domaine.
2. **Le contrat d'abord.** Les échanges entre services sont décrits en JSON Schema versionné ;
   les types TypeScript et Python en sont générés.
3. **Chaque app est un monolithe modulaire** : domaine, application, infrastructure. Ses surfaces
   (web, API, MCP, worker) appellent les mêmes services applicatifs.
4. **L'organisation est la frontière.** Chaque table porte l'organisation, avec RLS écrite dans la
   migration qui crée la table.
5. **Chaque app reste autonome.** Elle a sa base, son outbox, ses rôles métier ; elle continue de
   servir ses utilisateurs connectés si Kete Cockpit ou un guichet tombe.
6. **Une base par service**, jamais de lecture dans la base d'un autre : on se référence par
   identifiant (personne, organisation, produit).
7. **Tout changement de code passe par Pono.**

## 2. La carte du système

| Service | Pour qui | Rôle |
|---|---|---|
| **Compte Kete** | Tout le monde | Identité, organisations, rôles d'organisation, abonnements (proposition), paramètres génériques, OAuth pour les apps et le MCP |
| **Mon espace Kete** (D-013) | Le client | Le centre unique : ses apps, son organisation, ses abonnements, ses paramètres |
| **Kete Apps** | Le client et ses équipes | Firmo, Nettio, Nyatefe : le métier |
| **Kete Cockpit** | L'équipe Kete (puis d'autres porteurs de produits) | Administrer les produits : événements, santé, brief, points d'attention |
| **Guichets MCP** | Les agents | Kete Ops pour l'équipe, Kete pour les clients |
| **Pono** | Ceux qui construisent | Le chemin sûr des changements de code |

## 3. Le Compte Kete (D-011)

- Construit sur **Better Auth**, dans un service à lui : `compte.kete.africa` (nom à confirmer).
- **Connexion par e-mail** par défaut (mot de passe ou lien magique) ; téléphone plus tard.
- **Organisations** : une entreprise cliente est une organisation, avec ses membres et un rôle
  d'organisation (propriétaire, administrateur, membre).
- **Fournisseur d'identité** pour toutes les apps (connexion unique) et **serveur d'autorisation
  OAuth** pour le MCP.
- **Le jeton** transporte : la personne, l'organisation active, son rôle d'organisation, les apps
  auxquelles l'organisation a accès.
- **Opérateurs Kete** : identité séparée, double authentification obligatoire.

## 4. Mon espace Kete (D-013)

Le centre unique du client, servi par le Compte Kete :

- **Mes outils** : les liens vers ses apps Kete, avec leur état.
- **Mon organisation** : membres, invitations, rôle d'organisation de chacun.
- **Mes abonnements** : apps, formules, échéances, factures, paiement (via le port de paiement).
- **Paramètres génériques, saisis une fois, utilisés partout** :
  - identité de l'entreprise : nom, logo, adresse, contacts, identifiants légaux (RCCM, NIF) ;
    Firmo s'en sert pour l'en-tête des devis, Nettio pour ses tickets ;
  - langue, fuseau horaire, devise ;
  - canaux de notification préférés (e-mail, WhatsApp, Telegram).
- **Sécurité** : sessions actives, double authentification.
- **Mes données** : export, suppression, et le journal des accès du support Kete.
- **Besoin d'aide** : le bouton de retour, relié au support.

Chaque app garde ses **paramètres propres** (tarifs d'un pressing, modèles de devis) chez elle.

## 5. Les rôles, sur trois niveaux

| Niveau | Où | Exemple |
|---|---|---|
| Organisation | Compte Kete | Propriétaire, administrateur, membre ; apps accessibles |
| Métier | Dans chaque app | Nettio : gérant, caissier, atelier, livreur, par agence |
| Agent | Le jeton de la personne | Jamais plus de droits que la personne ; échelle d'autonomie |

L'accès d'un opérateur Kete au compte d'un client est limité dans le temps, motivé, audité et
**visible par le client** dans Mon espace Kete.

## 6. Les ports et leurs adaptateurs (D-014)

| Port | Premier adaptateur | Suivants possibles |
|---|---|---|
| Paiement | **Chariow** (D-012) | Moneroo, Stripe |
| Messages | E-mail transactionnel (Brevo ou Resend) | WhatsApp, Telegram, via Novu |
| Identité (côté app) | Compte Kete | Identité du socle pour Kete Enterprise |
| Fichiers | Stockage S3 (Neon ou autre) | Garage, SeaweedFS |
| Modèle d'IA | Claude | Tout autre modèle : les skills restent portables |
| Hébergement | Coolify | — |
| Code et changements | GitHub, via Pono | — |
| Secrets | Variables Coolify, puis Infisical | — |
| Surveillance | Uptime Kuma, GlitchTip | — |

## 7. Le paiement (D-012)

1. Le client choisit une formule dans Mon espace Kete (ou depuis une app).
2. Le port de paiement crée une session de paiement chez **Chariow** et renvoie le lien.
3. Le client paie sur la page Chariow.
4. Chariow notifie le Compte Kete (webhook « Pulses »), qui vérifie la vente auprès de Chariow.
5. L'abonnement de l'organisation devient actif ; le prochain jeton porte l'accès à l'app.
6. Un événement `payment.succeeded` part vers Kete Cockpit par l'outbox.

**Tranché (D-016)** : la facturation des apps Kete est **centralisée dans le Compte Kete** (un client,
un compte, une facture, et des offres groupées possibles). Les apps lisent l'accès dans le jeton et
gardent un délai de grâce si le Compte Kete est momentanément injoignable.

## 8. Les contrats et les événements

| Contrat | Contenu |
|---|---|
| `manifest.v1` | Identité de l'app, environnements, santé, événements émis, capacités |
| `event.v1` | Enveloppe d'événement signée (HMAC horodaté) |
| `health.v1` | État de l'app et de ses dépendances |
| `admin.v1` | API de l'espace opérateur |
| `capability.v1` | Un geste métier exposé par MCP, avec son niveau d'autonomie |

Événements standard : `account.created`, `account.activated`, `payment.succeeded`,
`payment.failed`, `subscription.renewal_due`, `account.closed`, `metrics.daily`. Aucune donnée
métier détaillée ne quitte l'app : des faits et des compteurs.

## 9. Kete Cockpit

- **Détient** : registre des produits, événements, sondes, instantanés quotidiens, points
  d'attention, échéances, briefs, audit.
- **Flux** : événements (app vers Cockpit, par l'outbox), santé (Cockpit vers `/health`, chaque
  minute), manifeste (chaque jour), instantanés (chaque nuit), brief (8 h, Telegram), MCP Kete Ops
  (à la demande), surveillance externe par Uptime Kuma (VPS séparé).
- **Plus tard** : déploiements et erreurs reliés aux incidents, espace opérateur, fiche client
  transverse, revenus, provisioning, rapports, ouverture à d'autres porteurs de produits.

## 10. L'architecture interne d'une app

```
Surfaces      web (PWA) · API · MCP · worker
Application   cas d'usage : « créer un dépôt », « préparer un devis »
Domaine       règles du métier, sans aucun fournisseur
Ports         paiement, messages, fichiers, identité, événements, IA
Adaptateurs   Chariow, e-mail, S3, Compte Kete, outbox, modèle d'IA
```

Chaque app reçoit du châssis : connexion au Compte Kete, outbox et événements, `/health` et
manifeste, module de l'espace opérateur, déclaration des capacités, port de paiement, bouton de
retour, design system.

## 11. Données et déploiement

- **Neon** : une base par service (Compte Kete, Cockpit, chaque app), des branches pour les
  préversions, région Francfort.
- **Coolify** : zone ops (Compte Kete, Cockpit), zone produits (apps), plus tard zone clients.
- **Uptime Kuma sur un VPS séparé.**
- **Secrets** hors des dépôts ; sauvegardes testées par restauration.
- **Domaines** (proposition) : `kete.africa` (site), `compte.kete.africa`,
  `cockpit.kete.africa`, et un sous-domaine ou un domaine propre par app.

## 12. Les dépôts (D-017)

| Dépôt | Contenu |
|---|---|
| `kete` | La doctrine (ce dépôt) |
| `kete-core` | Contrats, paquets partagés (`@kete/sdk`, `auth`, `admin`, `capabilities`, `payments`, `feedback`, `notify`, `design`), service Compte Kete et Mon espace Kete, châssis |
| `kete-cockpit` | L'app d'administration, qui consomme `kete-core` comme les autres apps |
| `firmo`, `nettio`, `nyatefe` | Les apps métier |
| `pono` | Inchangé |

## 13. Questions ouvertes

1. **Les domaines** des services et des apps.
2. **Chariow** : abonnements récurrents, signature des webhooks, frais et reversement.

Pile par défaut : TypeScript (D-015).
