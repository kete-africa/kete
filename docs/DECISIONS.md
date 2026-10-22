# Décisions

> Une décision par entrée : ce qui a été tranché, par qui, pourquoi, ce que ça coûte. On n'efface
> jamais une entrée ; on en ajoute une qui la remplace. Une proposition n'entre ici que validée par
> l'auteur.

---

## D-001 — Kete est la marque mère, à long terme

**Tranché le 2026-09-26** par l'auteur (« J'aime vraiment bien kete… Le nom est à long terme »).
Kete remplace Vitatech.

**Ce que ça coûte.** Kete Inc. (getkete.com, États-Unis) a déposé la marque KETE le 2026-04-28 pour
des logiciels d'IA de gestion. Pas de .com ; risque à l'international.
**À faire** : dépôt OAPI (classes 9, 35, 42, et 36 si paiement ou crédit), kete.africa, veille de
marque, recherche d'antériorité avant les marchés américain ou européen.

## D-002 — Trois parties, noms en anglais, dans cet ordre

**Tranché le 2026-09-28** par l'auteur : **Kete Apps**, puis **Kete Consulting**, puis
**Kete Enterprise**. Les noms sont en anglais, le contenu du site en français.

## D-003 — Kete Cockpit est une app du quotidien

**Tranché le 2026-09-28** par l'auteur. La plateforme d'administration des produits est une app de
Kete Apps, au même titre que Firmo, Nettio et Nyatefe, pour ceux qui font tourner des produits.
Elle est distincte de Pono. Kete l'utilise d'abord pour ses propres apps.

## D-004 — Pono reste un produit à part, « par Kete »

Pono garde son nom et son public mondial (ceux qui construisent avec des agents).

## D-005 — Kete est cliente de Kete

Kete fait tourner ses propres systèmes sur ses produits : Kete Cockpit pour ses apps, puis sa
propre instance de Kete Enterprise.

## D-006 — L'identité reçue : rouge chaud et racines

**Reçu le 2026-09-28** (`FONDEMENT.md`) : rouge chaud et racines dans le logo et sur le site ;
kete.africa ; « Outils de demain pour une meilleure productivité ».

## D-007 — Organisation GitHub `kete-africa`, dépôt `kete` pour la doctrine

**Tranché le 2026-09-28.** `kete` dit pourquoi et où ; le code vit dans les dépôts des produits.
Offre GitHub gratuite pour commencer ; passer à Team quand un dépôt de production privé a besoin de
la protection de branche (garde-fous de Pono).

## D-008 — Paiement par Moneroo, derrière une interface

Kete ne construit pas de passerelle de paiement : Moneroo orchestre, sans détenir l'argent.
L'argent d'un client ne transite jamais par Kete.

## D-009 — Pas de Keycloak par défaut

Commerçants : Compte Kete par téléphone. Entreprises : identité du socle. Keycloak seulement si un
déclencheur réel apparaît.

## D-010 — Le style visuel est la v1 rectangle

**Tranché le 2026-09-28** par l'auteur (« Mets le style v1 rectangle »). Remplace la v0 arrondie.

**Tranché ainsi.** La rigueur de la forme, la chaleur de la matière : rayons de 0 à 2 px, filets de
1 px, grille de 12 colonnes, Archivo élargie pour les titres, étiquettes rectangulaires avec un
carré de couleur, et la bande kete comme signature géométrique. La palette, le logo aux racines,
Instrument Sans et JetBrains Mono ne changent pas.

**Pourquoi.** La géométrie rectangulaire dit la précision et la solidité (la vérité des chiffres),
et elle vient du kete lui-même (bandes et blocs tissés), pas d'une marque étrangère.

**Ce que ça coûte.** Veiller à ce que Kete Apps restent chaleureuses pour les commerçants : plus de
rouge, une voix chaleureuse, les racines dans les illustrations.

## D-011 — Le Compte Kete repose sur Better Auth, connexion par e-mail

**Tranché le 2026-09-28** par l'auteur (« De base, on utilise le mail pour se connecter », « on
utilise Better Auth »). **Remplace D-009** pour les apps Kete.

**Tranché ainsi.** Un service Compte Kete, construit sur Better Auth, donne un seul compte pour
toutes les apps Kete. Connexion par **e-mail** par défaut ; le téléphone pourra venir ensuite
comme option. Pas de Keycloak. Les entreprises de Kete Enterprise gardent l'identité de leur socle.

## D-012 — Le paiement commence par Chariow, derrière un port générique

**Tranché le 2026-09-28** par l'auteur (« on va commencer par Chariow »). **Remplace D-008.**

**Tranché ainsi.** Le paiement passe par une interface générique ; Chariow est le premier
adaptateur. Moneroo, Stripe ou d'autres pourront suivre sans toucher aux apps. L'argent d'un
client de Kete Enterprise ne transite jamais par Kete.

## D-013 — Mon espace Kete : le centre unique du client

**Tranché le 2026-09-28** par l'auteur. Chaque client dispose d'un centre unique où il retrouve les
liens vers ses outils Kete et quelques paramètres clés génériques, communs à toutes les apps.

## D-014 — Tout élément externe passe par un port générique

**Tranché le 2026-09-28** par l'auteur (« on rédige générique afin qu'on ait des adapters pour
paiement et tout élément »). Paiement, messages, fichiers, hébergement, surveillance, IA : le
code des apps parle à une interface ; le nom du fournisseur ne vit que dans l'adaptateur.

## D-015 — Les apps sont découpées par features, avec des écrans conçus pour chaque métier

**Tranché le 2026-09-28** par l'auteur (« Je préfère la manière d'avant… Il faut toujours des
écrans adaptés et propres »).

**Tranché ainsi.** Chaque app est un monolithe modulaire découpé en features ; chaque feature porte
ses couches (domaine, commandes, requêtes, politiques, infrastructure, écrans, capacités). Les
écrans sont **conçus pour chaque métier**, jamais générés. Le châssis fournit les briques communes
(brouillons, vérification, audit, outbox, ports), pas les écrans métier.

**Reporté.** La proposition d'un « noyau Kete » qui génère formulaires, API et outils à partir de
déclarations est gardée pour plus tard (`journal/2026-09-28-noyau-kete-reporte.md`).

## D-016 — Tout en TypeScript

**Tranché le 2026-09-28** par l'auteur (« Oui, tout en typescript »). Répond à la question 1 de
`ARCHITECTURE.md`.

**Tranché ainsi.** Le Compte Kete, Kete Cockpit, `kete-core` et les nouvelles apps sont écrits en
TypeScript strict. Pile de référence : TanStack Start (React), Zod, Drizzle et Postgres (Neon),
Better Auth, une file de tâches dans Postgres (pg-boss), le SDK MCP officiel, Tailwind 4 et
`@kete/design`, Paraglide pour les traductions, Vitest et Playwright, ESLint et Prettier, et un
contrôle des frontières entre features. Python reste pour Pono, le socle KYA et d'éventuels
traitements lourds branchés par les contrats.

## D-017 — Documentation dans le dépôt, avec des schémas tenus à jour

**Tranché le 2026-09-28** par l'auteur (« Il faut la gestion de la docs avec des schémas au fur et à
mesure »). Règles dans `CONCEPTION.md`, partie E : Markdown et Mermaid à côté du code, mis à jour
dans la même pull request, une partie générée depuis le code et vérifiée en CI.

## D-018 — Un seul flux de travail pour tous les dépôts

**Tranché le 2026-09-28** par l'auteur (« on utilise toujours Spec Kit… avec Neon, on peut avoir des
branches… GitHub main, dev, feature »). Règles dans `FLUX.md` : `main` / `dev` / `NNN-slug` alignées
sur les branches Neon et les environnements Coolify ; Spec Kit pour chaque feature ; CI verte avant
toute fusion dans `dev` ; `main` par le geste humain seul, après les garde-fous de Pono.

## D-019 — Facturation centralisée et dépôts `kete-core` et `kete-cockpit`

**Tranché le 2026-09-28** par l'auteur (« go »). La facturation des apps Kete vit dans le Compte
Kete. `kete-core` porte les contrats, les paquets partagés, le Compte Kete, Mon espace Kete et le
châssis ; `kete-cockpit` est une app qui consomme `kete-core` comme les autres.

## D-020 — La documentation technique est en anglais

**Tranché le 2026-09-28** par l'auteur (« La documentation technique sera toujours en anglais »).

**Tranché ainsi.** Le code et toute la documentation technique des dépôts de code (README,
`docs/`, specs Spec Kit, schémas, décisions techniques, `CLAUDE.md`) sont en anglais. La doctrine
du dépôt `kete`, déjà rédigée, reste en français. Les écrans sont en français, et en anglais par
les traductions.

## D-021 — Chaque dépôt a sa feuille de route par phases

**Tranché le 2026-09-28** par l'auteur (« Dans chaque projet, il faut écrire le fichier roadmap des
phases »). Chaque dépôt de code porte `docs/ROADMAP.md` (en anglais, D-020) : phases contiguës,
chacune avec son objectif, son périmètre, ses dépendances et sa **preuve de fin**, sur le modèle de
Pono. La doctrine garde sa `FEUILLE_DE_ROUTE.md`, qui ordonne les dépôts entre eux.

## D-022 — Kete Cockpit vit dans `kete-core` tant que les paquets ne sont pas publiés

**Tranché le 2026-09-29** par l'auteur (« Je suis d'accord »). Amende D-019.

**Tranché ainsi.** Kete Cockpit se construit dans `kete-core`, comme une app à part
(`apps/cockpit`) : son propre déploiement, sa propre base, sa propre connexion par le Compte Kete,
comme n'importe quelle app Kete. Les paquets `@kete/*` seront publiés dans un registre privé le jour
où une app d'un autre dépôt (Nettio, Firmo) se branchera ; le Cockpit pourra alors s'extraire dans
son propre dépôt, s'il devient un produit ouvert à d'autres porteurs.

**Pourquoi.** Publier les paquets (compilation, versions, noms `@kete-africa/*`, jetons de lecture)
ne sert encore personne ; le Cockpit s'appuie sur les contrats, le Compte Kete et le système visuel
de `kete-core`, qui évoluent ensemble dans la même CI. « On ne construit que ce qui a déjà fait mal. »

## D-023 — Firmo est refondu en TypeScript, dans un nouveau dépôt `kete-africa/firmo`

**Tranché le 2026-09-29** par l'auteur (« Réécrire en TypeScript », « Nouveau dépôt vierge »).
Précise `ARCHITECTURE_APP.md` §10 pour Firmo.

**Tranché ainsi.** Firmo n'a pas encore d'utilisateur réel : on le réécrit sur l'architecture d'une
app Kete (D-015, D-016), avec sa base Neon et Neon Storage, dans un dépôt neuf
`kete-africa/firmo`. L'ancien dépôt (Python, Supabase) reste chez l'auteur comme référence : ses
tests, ses cas PDF et ses jeux d'évaluation servent d'oracle, et aucune règle métier écrite
(`decisions.md`, `model.md`) n'est perdue. Les offres, abonnements et paiements passent au Compte
Kete et au Cockpit (D-019) ; Firmo garde ses gestes métier. Les paquets `@kete/*` sont publiés
dans un registre privé (condition posée par D-022).

## D-024 — Le Compte Kete par numéro, créé en silence depuis la messagerie

**Tranché le 2026-09-29** par l'auteur (« c'est l'option 1 qui est la bonne »). Réalise
« Commerçants : Compte Kete par téléphone » (D-009) et le « téléphone plus tard » de D-011.

**Tranché ainsi.** L'usager d'une app de messagerie (Firmo d'abord) a un Compte Kete qu'il n'a
jamais eu à créer : son numéro, prouvé par la messagerie (l'expéditeur WhatsApp, le contact partagé
sur Telegram), devient une personne du Compte Kete, et son activité une organisation. Aucun
e-mail, aucun mot de passe, aucun formulaire. Le lien envoyé dans la conversation est une connexion
à usage unique et de courte durée au Compte Kete, qui ouvre l'app par la connexion unique. Le même
numéro ouvre les autres apps Kete ; l'e-mail et le mot de passe restent facultatifs, ajoutés depuis
Mon espace Kete.

**Pourquoi.** L'usage est informel : la valeur vient avant toute configuration, et une inscription
au premier message la détruirait. Un seul compte garde l'auth unique et la facturation centralisée.

## D-025 — Kete Enterprise avance dès maintenant, KYA en est le premier client autonome

**Tranché le 2026-09-30** par l'auteur (« je valide », après le choix entre un fork et une instance
autonome). Amende la règle 1 de `FEUILLE_DE_ROUTE.md` et précise D-016 pour « le socle KYA ».
Réflexion : `journal/2026-09-30-kete-enterprise-la-chaine.md`.

**Tranché ainsi.**
- Le socle se construit chez Kete, dans le dépôt `kete-africa/kete-enterprise`, **en parallèle** des
  Kete Apps.
- **KYA-Platform est une instance autonome de `kete-enterprise`** : sur les serveurs de KYA, aux
  couleurs de KYA, administrée par KYA. Le socle de KYA suit donc D-016 (TypeScript) ; l'ancien
  kya-platform (Python) reste une référence.
- **Jamais de fork.** KYA reçoit les versions (images et migrations). Ce qui est propre à KYA est de
  la configuration ou des apps connectées, dans des dépôts qui appartiennent à KYA.
- Entre Kete et KYA, le lien se limite à la **licence** et au **canal de versions**.
- La condition de l'étape 4 demeure : **la propriété est clarifiée par écrit avec KYA**, avant la
  mise en production chez KYA.

**Pourquoi.** Un fork diverge en quelques semaines et ne règle pas la propriété ; il la reporte.
Une instance autonome donne à KYA son autonomie et fait d'elle la preuve vivante de la
réversibilité promise à tous les clients (`MANDAT.md`, limite 1).

**Ce que ça coûte.** Kete Enterprise avance avant la preuve de l'étape 2 : le risque de dispersion
(`POSITIONNEMENT.md`, risque 2) est à surveiller. Tout ce que fait la console de Kete doit aussi
pouvoir être fait seul par l'administrateur d'une instance autonome : installer, mettre à jour,
revenir en arrière, sauvegarder, restaurer.

## D-026 — Une instance partagée pour les entreprises avec Kete ; les entreprises à part ont la leur

**Tranché le 2026-09-30** par l'auteur (« Une instance partagée pour les entreprises qui sont avec
moi, d'où la gestion des tenants » ; « des entreprises sur Kete avec leurs serveurs pour certaines
ressources clés, et les entreprises à part comme KYA »). Remplace « une instance par entreprise,
jamais partagée » (`OFFRES.md`).

**Tranché ainsi.** Un seul logiciel, `kete-enterprise`, plusieurs façons de le faire tourner :

| Cas | Où tourne l'instance | Qui l'administre |
|---|---|---|
| **Entreprise avec Kete** | L'instance partagée de Kete ; l'entreprise y est un **tenant**, isolé par la RLS | Kete |
| **Avec des ressources clés chez elle** | L'instance partagée ; ses fichiers, son ERP, ses apps, ses MCP ou son modèle d'IA restent sur ses serveurs et y sont reliés | Kete |
| **Entreprise à part** (KYA) | Sa propre instance, sur ses serveurs (D-025) | L'entreprise |

**Pourquoi.** Une instance par PME coûte trop cher à faire tourner, et le code isole déjà les
organisations par la RLS (constitution de `kete-core`, principe V).

**Ce que ça coûte.** L'isolation entre tenants devient la garantie la plus critique : testée en CI à
chaque changement, jamais contournée. Un tenant doit pouvoir être **exporté entier** pour partir ou
passer sur sa propre instance (`MANDAT.md`, limite 1).

## D-027 — La console de flotte de Kete Enterprise vit dans Kete Cockpit

**Tranché le 2026-09-30** par l'auteur (« Je valide »).

**Tranché ainsi.** Un module **Flotte** du Cockpit, réservé aux opérateurs Kete, gère les tenants
de l'instance partagée et les instances opérées par Kete : création, versions déployées par vagues
(Kete d'abord), santé, sauvegardes vérifiées, accès du support limité dans le temps, motivé, tracé
et visible par le client. **La console ne lit jamais les données métier d'un client** : des faits
et des compteurs. Le cœur du Cockpit reste l'outil générique des porteurs de produits. Une instance
autonome ne dépend pas du Cockpit ; l'envoi de sa santé et de faits y est facultatif et consenti.

**Pourquoi.** Le Cockpit a déjà le registre, la santé et les événements, et prévoit le
provisioning (`ARCHITECTURE.md` §9). Pour lui, une instance ou un tenant est un produit de plus ;
la flotte n'ajoute que des gestes. Pas de nouvelle app à faire vivre.

## D-028 — La frontière entre `kete-core` et `kete-enterprise`

**Tranché le 2026-09-30** par l'auteur (« D'accord »). Précise D-019.

**Tranché ainsi.** Le métier à tisser n'est pas le tissu (`VISION.md`).

- **`kete-core` est l'atelier de Kete** : ce qui permet de construire, vendre et faire tourner les
  produits. Les contrats ; les paquets `@kete/*` (dont, en phase 4, `records`, `commands`, `drafts`,
  `capabilities`, puis `ai`) ; le Compte Kete et Mon espace Kete ; Kete Cockpit et sa flotte (D-022,
  D-027) ; le modèle d'app. **Rien de ce qu'il contient n'est remis à un client.**
- **`kete-enterprise` est un produit : la chaîne d'une entreprise.** Ce qui existe *entre* ses
  outils : sa structure (unités, postes, affectations datées, délégations), ses droits avec portée,
  ses décisions (circuits d'approbation, Inbox), le registre de ses ressources (skills, apps, MCP,
  agents) avec soumission et promotion par paliers, son guichet MCP, ses agents avec fiche de poste,
  son IA interne, ses modules métier (finance et RH opérationnelles), le relais vers ses ressources,
  et l'API et le SDK de ses apps connectées. **C'est lui qui est remis au client, sous licence.**
- **Sens unique.** `kete-enterprise` dépend de `kete-core`, jamais l'inverse. Les Kete Apps ne
  dépendent pas de `kete-enterprise` : elles s'y **branchent** quand l'entreprise grandit, et
  changent de gamme sans changer d'outil.
- **Identité.** Sur l'instance partagée, le Compte Kete est l'identité, et l'organisation du Compte
  Kete est le tenant. Une instance autonome a sa propre identité (celle du socle, D-011). Le Compte
  Kete sait qui est la personne et dans quelle entreprise ; `kete-enterprise` sait où elle se trouve
  dans cette entreprise et ce qu'elle peut y faire.
- **Les mots.** L'*organisation* est l'entreprise cliente, la frontière RLS, partout dans Kete. La
  structure interne d'une entreprise se dit en *unités*.
- **Trois questions pour placer une brique.** Une Kete App en aurait-elle besoin ? Paquet de
  `kete-core`. Sert-elle à Kete pour vendre ou opérer ? Service de `kete-core`. N'a-t-elle de sens
  qu'avec des unités, des circuits et des ressources d'entreprise ? `kete-enterprise`.

**Pourquoi.** Les deux n'ont ni le même public (ceux qui construisent les produits, ou les employés
d'une entreprise), ni le même nombre d'exemplaires (un seul atelier, N instances), ni le même cycle
de vie (des bibliothèques, ou un produit installé chez des clients), ni les mêmes données (celles de
Kete, ou les plus sensibles d'une entreprise), ni la même licence (rien n'est remis, ou le produit
est remis).

**Ce que `kete-enterprise` ne devient jamais** : un ERP (il fait le travail, il intègre les livres),
un chat générique, une part de la machine commerciale de Kete, un logiciel qui a besoin de Kete pour
tourner, un lieu pour le code propre à un client.

## D-029 — Les choix techniques de Kete Enterprise

**Tranché le 2026-09-30** par l'auteur (« Je valide l'API Hono, les instances dédiées hébergées par
Kete, la gestion à distance, le relais, le modèle du chat »). Complète D-026.

**Tranché ainsi.**
- **Une API séparée en Hono**, sur Node LTS, que consomment le web, le MCP, les agents et les apps
  connectées ; les écrans en TanStack Start ; un worker pg-boss ; Drizzle et Postgres. Pas de Bun
  tant que tout l'écosystème ne migre pas ensemble.
- **Chez n'importe quel client** : `kete-enterprise` tourne sur tout Postgres 16 ou plus (avec
  pgvector) et tout stockage compatible S3, s'installe par Docker Compose ou un modèle Coolify, et
  n'appelle jamais Kete pour fonctionner.
- **Deux façons de plus de le faire tourner** : une instance dédiée hébergée par Kete ; une instance
  chez le client, administrée à distance par Kete.
- **Le relais** : un petit service chez le client, qui ouvre lui-même la connexion vers l'instance
  (aucun port entrant) et garde chez lui les secrets de ses ressources. La base de données reste
  toujours avec l'instance.
- **Le modèle du chat interne** passe par un port compatible OpenAI, DeepSeek d'abord ; le
  fournisseur se choisit selon la sensibilité des données (l'API de DeepSeek les traite en Chine).

## D-030 — Les briques communes vivent dans `kete-core`

**Tranché le 2026-09-30** par l'auteur (« On abstrait tout ce qu'on a déjà identifié » ; « Oui, tout
me va »). Précise D-028.

**Tranché ainsi.**
- **Les SDK servent à se brancher** sur un contrat ou un service : `@kete/sdk` (le protocole
  d'intégration, et lui seul : jamais un fourre-tout), `@kete/auth` (le Compte Kete), puis
  `@kete/enterprise-sdk`, publié par `kete-enterprise`, et un SDK Python quand une app Python en
  aura besoin.
- **Les briques servent à construire** une app selon les règles de Kete : `tenancy`, `commands`,
  `records`, `drafts`, `capabilities`, `ai`, `notify`, `identity` (extrait du Compte Kete), `files`,
  `payments`, `admin`, `feedback`, `design`, `testing`.
- **L'outillage sert à démarrer** : le modèle d'app et sa commande de création, les configurations,
  les vérifications.
- **Aucun paquet ne dépend d'un framework serveur** (ni Hono, ni TanStack) : des fonctions et des
  handlers `Request → Response`, qui se branchent tels quels partout ; la CI le vérifie. Le Compte
  Kete, le Cockpit et les Kete Apps restent sur TanStack Start ; seule l'API de `kete-enterprise`
  est en Hono (D-029).
- **La méthode** : une app garde sa propre gestion tant qu'elle ne se répète pas ; ce qui se répète
  est abstrait dans `kete-core`.

## D-031 — MailKite est le premier adaptateur d'e-mail

**Tranché le 2026-09-30** par l'auteur (« On commence ce fournisseur »).

**Tranché ainsi.** MailKite (envoi par API, réception en webhooks signés, boîte de réception pour
agents par MCP) est le premier adaptateur du port de messages de `@kete/notify` (D-014).

**Ce que ça coûte.** MailKite est en bêta, porté par une petite société américaine (SendHub LLC),
sur Amazon SES. Le port garde un changement de fournisseur à une ligne de configuration. Une clé par
service, limitée à son domaine ; la clé de compte, sans restriction, ne sert qu'à l'administration.
Les options sans conservation ou chiffrées sont activées, et l'accord de traitement des données est
vérifié avant l'usage pour un client.

## D-032 — La documentation s'écrit dans des formats reconnus

**Tranché le 2026-09-30** par l'auteur (« Au fur et à mesure, on doit documenter dans un format
reconnu afin que je puisse lancer la doc rapidement »). Précise D-017.

**Tranché ainsi.** Chaque dépôt publie un site **Starlight**, organisé selon **Diátaxis** (tutoriels,
guides, référence, explications). Les API REST en **OpenAPI 3.1**, générées depuis Zod ; les
événements en **AsyncAPI** ; les contrats en **JSON Schema** ; l'API des paquets par **TypeDoc** ; les
décisions techniques au format **MADR** ; les schémas en **Mermaid** (dont C4) ; les versions et
leurs journaux par **Changesets**. Un même gabarit pour tous les dépôts ; la CI refuse une doc
générée qui ne correspond plus au code.

## D-033 — Kete Cockpit sort dans son propre dépôt

**Tranché le 2026-09-30** par l'auteur (« Il faudrait par ailleurs, après, avoir le repo du
Cockpit »). Amende D-022.

**Tranché ainsi.** Une fois `kete-core` consolidé, le Cockpit sort dans `kete-africa/kete-cockpit`,
avec son historique ; il consomme les paquets publiés, garde son projet Neon, sa CI et sa doc.
`kete-core` ne garde que l'atelier : contrats, paquets, Compte Kete et Mon espace Kete, modèle d'app.

**Pourquoi.** La condition de D-022 est remplie (les paquets sont publiés), et un dépôt par
propriétaire rend le travail en parallèle sûr (D-034).

## D-034 — Les couloirs de travail et leurs propriétaires

**Tranché le 2026-09-30** par l'auteur (« Il faut qu'on fasse tout ce qu'on perçoit pour core, et
derrière je pourrai lancer les apps et enterprise en parallèle »).

**Tranché ainsi.**
- **D'abord, `kete-core` est consolidé seul**, puis trois couloirs avancent en parallèle :
  l'**atelier** (`kete-core`), les **apps** (Firmo, puis les autres, et `kete-cockpit`) et
  **Enterprise** (`kete-enterprise`).
- **Un propriétaire par dépôt**, un dossier de travail par instance d'agent (un `git worktree` si
  deux instances partagent un dépôt).
- **Les paquets se consomment en versions publiées**, jamais par la branche d'un autre couloir ; un
  besoin qui traverse deux couloirs passe par une issue.
- **L'auteur est seul à fusionner.**

## D-035 — Deux designs, plus la marque de chaque client

**Tranché le 2026-09-30** par l'auteur (« Puis-je avoir plusieurs designs ? J'aimerais copilot-demo
pour les entreprises » ; « tout me va »). Précise D-010.

**Tranché ainsi.**
- **`kete`**, la v1 rectangle (D-010), reste le style de Kete : son site, le Compte Kete, Mon espace
  Kete et les Kete Apps.
- **`workspace`** est le design de `kete-enterprise`. Il reprend l'organisation de la démo
  `copilot-demo` : assistants et conversations, bibliothèque, « enseigner » (soumettre un
  savoir-faire), agents, applications par catégorie. Il n'en reprend que les principes : **aucun
  élément de marque d'un tiers**, ni nom, ni icônes, ni police sous licence ; une police libre. Modes
  clair et sombre.
- **`@kete/design` porte trois couches** : jetons de base, jetons sémantiques, composants (qui
  n'utilisent que les jetons sémantiques). Un `DESIGN.md` par design, vérifié en CI.
- **La marque de chaque client** (logo, palette) s'applique au design `workspace` par les jetons
  sémantiques ; une palette qui ne respecte pas les contrastes est refusée.
- **Le design du Cockpit** reste à trancher.

## D-036 — `workspace` reproduit le système de `copilot-demo`

**Tranché le 2026-10-01** par l'auteur (« implémente correctement le design system de
copilot-demo que je t'ai passé »). Précise D-035.

**Tranché ainsi.**
- Le design `workspace` reprend le système de la démo **valeur pour valeur** : sombre d'abord
  (#282828, #242424, traits #494949, texte #DEDEDE et #999), barre latérale de 262 px, éléments de
  34 px, coins de 5 px, pilules de 24 px, menus et dialogues, Segoe UI à 14 px, le vert de la
  charte pour guider, l'orange pour le focus. Un mode clair s'y ajoute.
- **Deux écarts seulement** : le bouton principal prend le vert foncé de la démo (#177969), car le
  texte blanc sur #1CA18C ne se lit qu'à 3,2:1 ; Segoe UI est nommée mais jamais livrée (son
  fichier est sous licence), Inter, libre, la remplace ailleurs.
- Toujours aucun nom, logo ni icône d'application d'un tiers.

## D-037 — Une Kete App est aussi un ensemble de vues que le copilote fait apparaître

**Tranché le 2026-10-01** par l'auteur (« D'accord, merci bcp » ; « implémente toutes les phases
restantes »), sur la proposition faite à partir de sa discussion sur l'affichage des apps dans un
copilote.

**Tranché ainsi.**
- **Le standard est MCP Apps** (extension officielle de MCP, janvier 2026) : une capacité désigne
  une vue `ui://…`, un document HTML que l'hôte (le copilote de `kete-enterprise`, Claude, ChatGPT)
  affiche dans la conversation, isolé dans un iframe.
- **Deux niveaux de vues** : des **vues génériques** fournies par `kete-core` (vérification d'un
  brouillon, formulaire, tableau, détail), tirées du schéma de l'enregistrement, sans code
  d'interface ; et des **vues sur mesure** qu'une app fournit quand son métier l'exige (carte,
  éditeur, tableau de bord).
- **Le partage** : `kete-core` apprend aux apps à se montrer (contrat, `@kete/capabilities`,
  `@kete/views`, modèle d'app) ; `kete-enterprise` apprend au copilote à les afficher (l'hôte, la
  composition, le guichet, la soumission et la promotion des apps).
- **La décision humaine** : un brouillon de niveau 3 se valide dans la vue, par un outil que seule
  la vue peut appeler, jamais le modèle. Le niveau 4 (irréversible, argent, externe) renvoie à
  l'écran de l'app, avec sa confirmation. Le lien vers l'écran reste toujours le recours.

**Pourquoi.** L'app vient à la personne quand elle en a besoin, sans qu'elle ait à l'ouvrir, et la
même vue sert dans Kete et dans les copilotes du marché.

## D-038 — Une Kete App peut avoir son propre design

**Tranché le 2026-10-01** par l'auteur (« Oui, ajoute »). Précise D-035.

**Tranché ainsi.**
- Une Kete App prend `kete` par défaut, `workspace` si elle sert une entreprise, ou **son propre
  design**.
- Son design suit les mêmes trois couches : son `DESIGN.md` (jetons de base) et sa correspondance
  sémantique, générés par l'outil de `@kete/design`, avec les mêmes contrôles de contraste en CI.
  Les composants de `@kete/design` le portent sans changement.
- Le contrat commun (Compte Kete, isolation par organisation, événements, brouillons, aucune chaîne
  en dur) ne change pas : le design règle l'apparence, jamais le comportement.

## D-039 — Les agents permanents, et ce qu'ils se délèguent

**Tranché le 2026-10-01** par l'auteur (« Ecris et continue avec ce que tu dois faire »), sur
l'analyse de sa discussion sur des agents qui travaillent pour chaque employé, jour et nuit.
Précise le principe 4, l'échelle d'autonomie et D-028. Réflexion :
`journal/2026-10-01-agents-et-conformite.md`.

**Tranché ainsi.**
- **Trois sortes d'agents, une seule fiche de poste.** Les agents d'une personne ; les agents d'un
  poste, qui agissent pour qui l'occupe selon ses affectations datées, et changent de droits quand
  il change ; les agents du système, rattachés à un responsable humain nommé. Tous passent par le
  registre de `kete-enterprise` (D-028).
- **Un agent agit dans une seule organisation.** Une personne qui appartient à plusieurs
  organisations a des agents distincts dans chacune ; aucun ne franchit la frontière RLS de son
  organisation, ni ne mêle leurs contextes.
- **Permanent ne veut pas dire en boucle.** Un agent dort, et se réveille sur un événement, une
  échéance, un message ou une réponse. Ses attentes sont durables : une tâche planifiée, un
  brouillon en attente de décision. Le worker pg-boss les porte (D-029) ; pas de moteur de
  workflow à part tant qu'une limite mesurée ne l'exige pas.
- **La délégation ne fait que rétrécir.** Un agent qui confie une tâche à un autre lui remet une
  autorisation limitée à cette tâche (ressources, durée, budget), jamais plus que la sienne, qui
  n'est jamais plus que celle de la personne (principe 4). La chaîne remonte toujours à un humain ;
  sa profondeur et son budget sont plafonnés.
- **Chaque geste porte sa chaîne** : l'agent qui agit, la personne pour qui, l'agent qui l'a
  demandé, une trace commune. Le journal de chaque Kete App la garde (`@kete/commands`).
- **Un agent ne décide jamais pour un humain.** Un brouillon de niveau 3 ou 4 est validé par une
  personne, jamais par un autre agent, quelle que soit la chaîne.
- **Un budget de brouillons.** Chaque agent a un plafond de brouillons ouverts, regroupés dans
  l'Inbox ; au-delà, il attend. Trop de validations fait cliquer « Valider » sans lire.
- **Le premier agent permanent est de niveau 1** : la veille des contrôles (D-040). Il lit,
  vérifie et signale ; il ne change rien.

**Pourquoi.** Des agents qui travaillent en permanence multiplient les gestes faits au nom des
personnes. Sans chaîne jusqu'à un humain, personne ne sait plus qui a voulu quoi ; sans droits qui
rétrécissent, une délégation devient une élévation de privilèges ; sans budget de brouillons,
l'humain ne décide plus, il approuve.

**Ce que ça coûte.** Une autorisation par tâche est plus lourde qu'un jeton partagé, et un agent
bloqué par son budget attend un humain. C'est voulu.

## D-040 — La gouvernance est dans le contrat ; la conformité est un moteur de contrôles

**Tranché le 2026-10-01** par l'auteur (« Ecris et continue avec ce que tu dois faire »), sur
l'analyse de sa discussion sur la plateforme gouvernée de Microsoft et l'intégration des normes ISO.
Précise D-028 et la ligne « les contrôles » de l'architecture de Kete Enterprise.

**Tranché ainsi.**
- **Gouverner une fois, tourner partout.** La gouvernance d'une app est dans son contrat (son
  manifeste, ses capacités, ses événements, sa santé) et dans le registre qui la reçoit, jamais
  dans son hébergement : `kete-enterprise` tourne chez n'importe quel client (D-029). Une app
  faite avec n'importe quel outil entre dans Kete si elle respecte le contrat ; une app faite avec
  le modèle d'app le respecte dès sa création.
- **La carte d'identité d'une app** : `manifest.v1` déclare son responsable, les catégories de
  données qu'elle traite, son usage de l'IA et sa criticité. Le registre en déduit les contrôles
  qui s'appliquent ; le Cockpit et le registre en font l'inventaire.
- **Un seul modèle pour toute conformité** : référentiel → exigence → contrôle → preuve → écart →
  action corrective → audit. Un référentiel est une norme ISO, une loi, une politique interne, une
  exigence de client ou un contrat.
- **Un contrôle sert plusieurs référentiels.** La bibliothèque de contrôles est commune ; chaque
  référentiel s'y relie. Une sauvegarde testée une fois vaut pour tous ceux qui la demandent.
- **Tout a une portée** dans la structure de l'entreprise (entité, pays, unité, projet, processus,
  app) : un référentiel ne s'applique pas uniformément.
- **Une preuve est un enregistrement** : sa source, sa date, qui l'a collectée, son empreinte, sa
  durée de validité, son contrôle. Les preuves automatiques viennent des journaux (commandes,
  décisions sur les brouillons, événements) ; les autres sont des attestations humaines. Une
  preuve ne vaut que ce que vaut sa source (principe 2).
- **Les textes des normes ne sont jamais livrés.** Kete livre le moteur et des contrôles rédigés
  avec ses propres mots, reliés aux numéros de clause ; l'entreprise installe les référentiels pour
  lesquels elle a les droits. L'édition de chaque norme se vérifie quand son référentiel est écrit.
- **On montre des contrôles et leurs preuves**, jamais un pourcentage de conformité.
- **Où ça vit.** Le moteur est dans `kete-enterprise` (D-028). `kete-core` fournit la matière des
  preuves (journal des commandes, décisions sur les brouillons, événements) et la carte d'identité
  des apps.
- **Un référentiel pilote d'abord** : celui qui a une échéance réelle chez KYA, avec quelques
  contrôles réels, avant tout catalogue.

**Pourquoi.** Huit normes traitées séparément font huit systèmes de conformité, et autant de fois
la même preuve. Une conformité déduite du contrat et des journaux se construit en travaillant, pas
avant l'audit.

**Ce que ça coûte.** Écrire des contrôles avec ses propres mots et les relier aux clauses demande
un travail d'expert par référentiel ; c'est ce travail que vend Kete Consulting.

## D-041 — Le moteur parle d'organisations ; l'offre parle d'entreprises

**Tranché le 2026-10-01** par l'auteur (« Ecrire D-041 »), sur l'analyse de sa discussion : « le
concept d'entreprise peut gérer tout, un couple, une communauté, un groupe, une famille ». Précise
D-028 et D-039. Réflexion : `journal/2026-10-01-agents-et-conformite.md`.

**Tranché ainsi.**
- **Les primitives restent génériques.** Une *organisation* (la frontière RLS, partout dans Kete),
  ses *unités* aux types configurables, ses *postes*, ses *affectations* datées, ses *relations*.
  Aucune table ne s'appelle « employé », « société » ou « département » : ce sont des types d'unité,
  d'affectation ou de relation, que chaque organisation nomme.
- **Une personne appartient à plusieurs organisations** (le Compte Kete le permet déjà), avec des
  droits distincts dans chacune ; ses agents ne franchissent jamais la frontière d'une organisation
  (D-039).
- **L'offre reste celle des entreprises**, d'abord africaines. Aucun produit pour les familles, les
  couples, les communautés ou les associations n'est construit avant un client réel (principe 7).
- **Ce que le générique ne couvre pas**, et qui attendra ce client : les décisions conjointes ou à
  l'unanimité sans hiérarchie, la tutelle des mineurs et leur consentement, l'intimité entre
  membres d'un même foyer, et un mode d'installation qui ne soit pas une instance par entreprise.

**Pourquoi.** Nommer le moteur par ce qu'il est ne coûte rien et évite de le refaire ; construire
pour chaque collectif possible referait l'erreur de kya-platform : beaucoup de code, aucun usage.

**Ce que ça coûte.** Des noms un peu plus abstraits dans le modèle de données ; les écrans, eux,
parlent la langue de chaque organisation.

## D-042 — Le centre a trois endroits ; un outil métier est une app

**Tranché le 2026-10-13** par l'auteur (« D'accord, merci », sur la structure finale proposée par
l'agent ; puis « Super, modifies les documentations, fais le plan et vas au bout correctement »).
Précise D-028 et D-037. Réflexion : `journal/2026-10-13-le-centre-la-confiance-les-collegues.md`.

**Tranché ainsi.**
- **Kete se lit en cinq étages** : `kete-core` (le socle), la couche de confiance (dans le socle,
  D-043), Kete Enterprise (le centre), les apps (derrière le centre), Kete Cockpit (pour Kete).
- **Le centre a trois endroits, nommés par ce qu'on y fait** :
  - **Décider** — ce qui attend la personne, une décision à la fois avec ses preuves ; « À faire » ;
    les demandes reçues ; ce que les agents font pendant ce temps. « Aujourd'hui » et « À faire » y
    fusionnent.
  - **Demander** — l'assistant, dont une réponse peut être un outil (un tableau, un formulaire) ;
    les fils rangés par projet ; les fichiers et les pièces ouverts sur place.
  - **Déléguer** — ses agents, leurs états, leur exécution en direct, leurs routines, « Mon
    accueil » (D-044).
- **Derrière** : les Apps et l'Administration (organisation, droits, règles, registre, preuves,
  offre et limites). Le téléphone et les messageries portent Décider et Demander.
- **Un outil métier est une app, jamais un module du centre.** Performance, enquêtes, réunions et
  conformité, logés dans le centre pour KYA, en sortent et s'y relient par le contrat des apps.
- **Brancher avant de remplacer** : un outil existant d'un client (son ERP) entre d'abord comme une
  app derrière le centre, par un connecteur ; on ne refait que ce qui fait mal.

**Pourquoi.** Le centre comptait une vingtaine d'endroits et quatre outils taillés pour un seul
client : il ne se vendait pas seul, et la personne qui doit décider en quelques secondes s'y
perdait. Trois verbes disent ce que le produit fait.

**Ce que ça coûte.** Une refonte des écrans de Kete Enterprise sur le code existant (sa feuille de
route, étapes C1 à C11), et le travail de sortir quatre domaines du centre.

## D-043 — La confiance est le cœur ; le moteur des agents s'appuie sur une bibliothèque éprouvée

**Tranché le 2026-10-13** par l'auteur (« Super, modifies les documentations, fais le plan et vas
au bout correctement », sur le point complet de l'agent). Précise D-028, D-030, D-039 et D-040.

**Tranché ainsi.**
- **Ce qui distingue Kete est la couche de confiance**, écrite une fois dans `kete-core` : le
  mandat (« l'agent X pour la personne Y, jamais plus qu'elle »), le brouillon décidé par une
  personne, l'autonomie par type de tâche, les **règles** de l'organisation, le **registre** des
  agents, des modèles et des connecteurs, la mémoire gouvernée, et « Comment ? » sur tout ce qu'un
  agent a fait.
- **Les règles** s'écrivent en une phrase, s'appliquent à un seul point de passage, et chaque refus
  est journalisé avec la règle qui a refusé. Huit familles : données, modèles, outils et
  connecteurs, autonomie, conservation, transparence, budgets, sortie. Une règle s'essaie sur le
  mois passé avant d'être activée.
- **Le registre** donne à chaque agent un propriétaire, une autonomie maximale et une date de
  revue ; un agent sans propriétaire est mis en pause ; le registre repère les doublons, et les
  agents d'une personne qui part changent de propriétaire.
- **Le moteur des agents** (boucle, étapes, pause et reprise, mémoire, évaluations) est pris d'une
  bibliothèque éprouvée — Mastra, essayée une journée avant d'être retenue — et non réécrit.
  L'écran reste sur assistant-ui, les outils sur MCP. Pas de seconde pile d'interface.
- **Positionnement** : le centre de travail des entreprises africaines, où les agents préparent,
  où les personnes décident et où tout est traçable ; **souverain et réversible** (standards
  ouverts, tout s'exporte, s'installe chez le client sans appeler Kete).
- **La couche de confiance n'est pas vendue à d'autres éditeurs pour l'instant.**

**Pourquoi.** L'assistant, les agents et les routines avaient été écrits à la main dans Kete
Enterprise et réécrits dans Nettio, alors que la feuille de route nommait déjà une bibliothèque. Ce
qu'aucune bibliothèque ne fournit — les droits, le brouillon, le mandat, le journal, les règles —
est précisément ce qui a de la valeur partout.

**Ce que ça coûte.** Une dépendance de plus à suivre ; une migration des agents existants, morceau
par morceau ; l'isolation par organisation à prouver sur les tables du moteur.

## D-044 — On s'adresse à une personne ; ses agents sont privés ou partagés

**Tranché le 2026-10-13** par l'auteur, qui a posé le concept (« une personne peut avoir ses agents
visibles uniquement pour lui et l'admin ; pour les agents qu'il rend visibles aux autres, ils
peuvent l'appeler ; pour ses agents propres, les autres sont obligés de l'indexer lui pour la tâche
et sa propre configuration interne permet de savoir qui fait quoi ») puis l'a confirmé (« Je veux
tout. Ok ! »). Précise D-039.

**Tranché ainsi.**
- **On demande un travail à une personne**, jamais à ses agents privés. La demande a ses états :
  reçue, prise en charge, « vous attend », rendue. Celui qui demande voit un état, pas
  l'organisation interne de l'autre.
- **Un agent est privé ou partagé.** Privé : son propriétaire et l'administrateur — privé ne veut
  pas dire hors contrôle, il est au registre. Partagé : on le mentionne dans un fil ; son
  propriétaire choisit à qui il l'ouvre.
- **« Mon accueil »** dit, pour chaque personne, ce qui arrive chez elle et qui s'en occupe. Il
  fonctionne sans réglage (tout arrive à la personne) ; le système propose des règles à partir de
  ce qu'elle fait.
- **Garde-fous.**
  - La responsabilité reste à la personne : un travail fait par son agent est le sien.
  - Rien ne revient au demandeur sans contrôle, sauf des données qu'il peut déjà lire.
  - Un agent partagé agit avec les droits de celui qui l'appelle, réduits à ce que l'agent sait
    faire — jamais avec ceux de son propriétaire.
  - Le journal garde les deux noms : « l'agent, pour sa personne, à la demande de telle autre ».
  - Les règles de l'organisation passent au-dessus des réglages personnels.
  - Chaque retour dit si une personne a validé ou si un agent a répondu seul.
  - L'intérim prend le relais d'un absent.

**Pourquoi.** C'est ainsi qu'une entreprise marche déjà : on demande à quelqu'un, et comment il
s'organise le regarde. Les agents deviennent le levier d'une personne, pas un second organigramme.

**Ce que ça coûte.** Un modèle trop lourd pour une organisation de dix personnes : il doit rester
invisible tant qu'on ne s'en sert pas. Un risque de goulot sur la personne, que l'intérim et le
partage des agents utiles doivent lever.

## D-045 — La signature Kete : sept règles de comportement, et la façon de montrer un agent

**Tranché le 2026-10-13** par l'auteur (« Il faudrait que j'aie aussi une identité dans la manière
dont les produits sont faits, UX aussi » ; puis « Super, modifies les documentations », sur le point
complet). Précise D-035 et D-038 : les couleurs changent par app et par client, la signature reste.

**Tranché ainsi.** Un produit Kete se reconnaît à son comportement :
1. Il s'ouvre sur ce qui attend la personne, pas sur un menu.
2. Un geste principal par écran.
3. L'agent prépare, la personne décide — avec la même carte de vérification partout.
4. Chaque chiffre a son unité, sa période et sa source ; « Comment ? » est à côté.
5. Des phrases, pas des réglages — sauf pour les droits, où un tableau à cocher est plus sûr.
6. Tout se défait.
7. La même chose par WhatsApp et Telegram.

Et un agent se montre toujours de la même façon : six états (en veille, travaille, vous attend,
bloqué, en pause, arrêté) ; trois niveaux de détail (une ligne, les étapes, l'exécution) ; toujours
interruptible ; le même objet pendant et après ; l'échec se dit ; jamais déguisé en humain.

Chaque règle est portée par un composant de `@kete/design` et vérifiée, pas par un guide de style.

**Pourquoi.** Une identité visuelle se copie et change d'un client à l'autre ; une manière de se
comporter se reconnaît quel que soit l'habillage.

**Ce que ça coûte.** Une discipline : un écran qui enfreint une règle n'est pas livré.

## D-046 — S'enrôler sur l'instance partagée : des offres avec limites, la Flotte, un essai

**Tranché le 2026-10-13** par l'auteur (« je devrais avoir un centre pour créer les comptes pour
chaque entreprise et leur permettre d'avoir leurs espaces » ; puis « Super, modifies les
documentations », sur le point complet). Précise D-026 et D-027.

**Tranché ainsi.**
- **Enrôler une entreprise ne crée aucune machine.** Sur l'instance partagée, on crée une
  organisation, son premier administrateur, son offre, ses modules et ses limites.
- **Des offres avec limites**, portées par le Compte Kete et lues par toutes les apps : personnes,
  budget d'IA, stockage, apps connectées, agents. Au-delà, l'espace reste lisible et les gestes
  coûteux attendent. Les chiffres des offres restent à fixer par l'auteur.
- **Un essai** : une entreprise s'inscrit seule et obtient son espace, avec des données d'exemple.
- **La Flotte** du Cockpit (D-027) crée, suspend et suit les espaces ; elle voit des compteurs,
  jamais les données d'un client. Un espace s'exporte entier.
- **Hébergement de l'instance partagée** : un serveur à Kete, dans la même région que la base de
  données ; l'instance de KYA reste sur les serveurs de KYA (D-025). Tout transfert de données
  personnelles hors du Togo passe par l'autorité de protection des données.

**Pourquoi.** Les fondations étaient là (isolation par organisation, Compte Kete, abonnements) ;
le parcours ne l'était pas : ni console, ni limites, ni essai, ni export.

**Ce que ça coûte.** L'isolation entre espaces reste la garantie la plus critique. Les offres et
leurs plafonds, le compte d'hébergement et la démarche auprès de l'autorité dépendent de l'auteur.

## D-047 — Le centre tient les références : les personnes, les tiers, les projets

**Tranché le 2026-10-13** par l'auteur (« projets peut être un modèle puissant sur lequel s'appuient
plein d'éléments » ; puis « Allez, actualise les docs, fais le plan et va au bout du core, projets,
tiers, 4 apps »). Précise D-042.

**Tranché ainsi.**
- **Le centre tient trois références** que toutes les apps citent, par leur identifiant : les
  personnes (la structure), les **tiers** (avec qui l'on travaille) et les **projets** (sur quoi).
  Les apps tiennent les faits ; aucune ne recopie une référence.
- **Le projet est un seul objet.** L'endroit où l'on discute d'un chantier — ses fils, ses
  fichiers, ses consignes, sa mémoire — est celui où l'on voit son argent, son équipe, ses
  échéances, son contrat et ses tickets. Il naît d'une phrase ou d'un devis gagné, dont les lignes
  deviennent les postes de son budget.
- **Le projet est un second axe de droits**, à côté de la structure : on voit ce qui touche ses
  unités et ses projets. Un circuit peut passer par le responsable du projet.
- **Le tiers est unique** : la même entreprise peut être cliente, fournisseur et bailleur. Les
  doublons se fusionnent ; chaque app dit ce qu'elle sait de lui, le centre le rassemble.
- **Sans projet, tout va dans « Fonctionnement ».** Le modèle reste invisible pour qui ne s'en
  sert pas.

**Pourquoi.** Chaque app avait son client, son fournisseur, son chantier, sans lien entre eux. Ce
qu'un dirigeant demande — où en est ce projet, que sait-on de ce client — traverse toutes les apps.

**Ce que ça coûte.** Le centre devient nécessaire à ces apps. Un modèle de projet trop riche
découragerait une entreprise de dix personnes : il doit se créer sans formulaire.

## D-048 — Quatre apps pour toute entreprise : Kete Finance, Kete Team, Kete Commitments, Support

**Tranché le 2026-10-13** par l'auteur (« je préfère qu'on se concentre sur les nœuds génériques » ;
puis « va au bout du core, projets, tiers, 4 apps »). Précise D-042 ; ne concerne ni Firmo ni Nettio,
dont le besoin est différent.

**Tranché ainsi.**
- **Kete Finance** — une seule app pour l'argent, en trois parties : ventes, achats et dépenses,
  trésorerie. Un seul registre : le disponible d'un projet doit être exact à la seconde où l'on
  approuve une dépense.
- **Kete Team** — congés et absences, dossiers, habilitations, temps par projet, avances, éléments de
  paie.
- **Kete Commitments** — contrats, obligations, échéances, retenues et cautions, preuves. La conformité
  y entre.
- **Support** — tickets et délais ; le ticket sait ce que le client a acheté et qui paie.
- **Les produits portent un nom anglais**, comme Kete Enterprise et Kete Cockpit ; leurs écrans
  parlent la langue de qui les lit.
- **Ces apps supposent le centre** : elles ne se vendent pas seules. Si le centre ne répond pas,
  elles continuent sur ce qu'elles savent.
- **Elles ne font pas** la comptabilité générale, le calcul de la paie, le stock : on exporte vers
  l'outil du comptable, ou on le branche par un connecteur.
- **Enquêtes** rejoint les formulaires du centre ; **Réunions** devient un fil à plusieurs ;
  **Performance** reste un outil de pilotage à part.

**Pourquoi.** Ce sont les quatre questions que tout dirigeant se pose : ai-je l'argent, qui est là,
qu'ai-je signé, quel client attend. Trois apps séparées pour l'argent auraient donné trois chiffres.

**Ce que ça coûte.** Kete Finance est le noyau commercial et financier d'un progiciel : il faut le
garder petit. La lecture des relevés et des reçus par un modèle n'est pas prouvée.

## D-049 — L'argent : trois états, par projet, avec sa preuve

**Tranché le 2026-10-13** par l'auteur (« il faut qu'on suive les fonds disponibles pour chaque
projet afin de pouvoir séparer clairement et savoir ce qui avantage et si les fonds sont utilisés
pour ce qu'il faut »). Précise D-048.

**Tranché ainsi.**
- **Chaque fait d'argent porte un projet** — ou « Fonctionnement » — et, pour une dépense, un poste
  du budget. Les apps l'envoient au centre dans un contrat commun.
- **Trois états** : ce qui est en caisse et en banque, ce qui est **réservé** aux projets (un
  acompte reçu n'est pas encore à soi), ce qui est **engagé** (une commande passée, une paie due).
  Le « vraiment disponible » est le reste.
- **Par projet** : reçu, engagé, dépensé, disponible ; ce qu'il rapporte ; et si ses fonds ont payé
  ce pour quoi ils ont été reçus. La convention d'un bailleur devient des règles de dépense.
- **La séparation des rôles** : qui demande n'approuve pas, qui approuve ne paie pas.
- **La preuve** : chaque geste d'argent porte sa pièce. Un brouillon lu sur une photo montre d'où
  vient chaque champ.
- **Kete n'exécute aucun paiement** et ne tient pas la comptabilité générale. Les montants sont
  calculés par le code.

**Pourquoi.** L'argent d'un projet qui paie un autre projet est l'erreur la plus courante et la
moins visible ; un bailleur ou un client la demande en premier.

**Ce que ça coûte.** Ajouter le projet après coup obligerait à reclasser l'historique : il doit
être là dès le premier fait. Les coûts partagés (salaires, loyer) restent d'abord dans
« Fonctionnement ».

## D-050 — Planifier : le temps est le quatrième endroit du centre

**Tranché le 2026-10-13** par l'auteur (« La vue calendrier pourrait être une vue capitale […] on
peut distinguer sa vue personnelle et la vue complète qui montre jusqu'aux personnes en congés » ;
puis « fais et toi même fusionnes », sur la maquette 3.1). Précise D-042 : le centre a désormais
quatre endroits, toujours nommés par ce qu'on y fait.

**Tranché ainsi.**
- **Planifier** rejoint Décider, Demander et Déléguer. Ce n'est pas une app : c'est la vue du temps
  du centre, qui rassemble les faits datés que les apps lui envoient — réunions, échéances
  (factures, contrats), congés, tâches avec leur durée, passages des agents et des routines — et
  l'agenda externe de la personne, par un connecteur.
- **Trois vues, selon les droits** : *ma vue* (sa semaine), *mon équipe* (une ligne par personne),
  *toute l'organisation* (par unité, avec les absents). On y voit qui est là et qui est absent,
  jamais le motif d'une absence ; des autres, seulement ce qu'ils partagent.
- **L'assistant signale les conflits de lui-même** (un responsable absent le jour d'une réception)
  et propose comment les régler, en un geste. Il **propose des blocs** dans les trous de la
  semaine, chacun avec sa raison ; la personne les garde ou les retire. Rien n'entre dans son
  agenda sans elle.
- Sur un téléphone, la semaine devient une liste de jours.

**Pourquoi.** Le temps est la ressource la plus rare d'une petite entreprise, et il est éparpillé :
les congés dans une app, les échéances dans une autre, les réunions ailleurs. Une décision
(approuver un congé, accepter une livraison) se prend mal sans voir la semaine.

**Ce que ça coûte.** Un connecteur d'agenda par fournisseur, à brancher plutôt qu'à écrire. Une
discipline sur la vie privée : la vue d'équipe ne doit jamais devenir une surveillance.

## D-051 — La méthode : un rythme de travail que les agents tiennent avec la personne

**Tranché le 2026-10-13** par l'auteur (« le système va au delà de la centralisation, on arrive à
une méthodologie de travail qui aide vraiment les employés à s'organiser mieux […] les agents
fournissent ou leur disent ce qu'ils doivent faire »). Précise D-042 et D-045.

**Tranché ainsi.** Kete n'est pas seulement l'endroit où tout se trouve ; c'est une façon de
travailler, en quatre moments :
- **Le matin** — Décider : une décision à la fois, avec ses preuves, jusqu'à « tout est réglé » ;
  puis la journée proposée dans Planifier.
- **La journée** — Demander et Déléguer ; les agents travaillent sur le serveur de l'organisation,
  même téléphone éteint ; « Pendant ce temps » dit qui fait quoi.
- **Le soir** — la clôture, en deux minutes : une note en cinq cases (fait, pas fait, bloqué,
  demain, appris), écrite ou dite, dans Kete ou par une note vocale sur WhatsApp. Kete en tire des
  **rangements proposés** — reporter, clore, bloquer un créneau, confier, corriger une fiche,
  proposer une leçon — que la personne coche ; rien ne change sans ce geste, et tout se défait.
- **La semaine** — la revue : le résumé de la semaine, le plan de la suivante, ce qui a été appris,
  ce que les agents ont fait.

**Les agents proposent ce qu'il faut faire ; ils ne commandent pas.** Le plan est une proposition,
la personne reste maîtresse de sa journée. Un responsable voit les engagements et les blocages de
son équipe, jamais le détail d'un agenda ni le temps passé minute par minute.

**Pourquoi.** Centraliser ne suffit pas : une personne bien informée peut rester débordée. Ce qui
aide vraiment, c'est un rythme simple, tenu chaque jour, où l'IA fait le travail de rangement.

**Ce que ça coûte.** Une habitude à faire prendre — elle n'est prouvée qu'à l'usage. Les rangements
du soir touchent des objets de plusieurs apps : chacun passe par le geste de l'app, avec son niveau.

## D-052 — Le tableau, la routine et le résumé sont un seul objet ; indexer est un choix

**Tranché le 2026-10-13** par l'auteur (« un système de résumé quotidien, hebdomadaire que la
personne peut créer et décider d'indexer depuis une page centrale de widgets » ; « à la fin d'une
journée, la personne peut aussi noter au-delà, ce qui aide l'IA à restructurer certains
éléments »). Précise les tableaux de bord, les routines et les notes de Kete Enterprise.

**Tranché ainsi.**
- **Un résumé n'est pas un rapport : c'est le passage entre le travail et la mémoire.** Il clôt (ce
  qui est fait, ce qui reste, ce qui bloque), il transmet (au responsable, à l'équipe, à qui
  remplace pendant un congé, à un bailleur) et il se souvient.
- **Un même objet, trois moments** : composé une fois dans « Mon tableau », il est *regardé* en
  direct, *envoyé* à heure fixe (le soir, le vendredi), *gardé* comme résumé. Ses chiffres sont
  calculés par le code et figés au moment du résumé ; son texte est écrit par l'agent avec ses
  sources ; la note de la personne s'y ajoute.
- **Indexer est le choix de la personne** : dans son espace, dans un projet, pour une équipe.
  Indexé, le résumé devient une mémoire datée que l'assistant cite et que l'équipe retrouve ; non
  indexé, il reste à elle. Elle peut retirer un résumé de l'index à tout moment.
- **« Mon tableau » est une seule entrée**, en trois onglets : En direct, Résumés, Carnet.
  **Noter** se fait depuis n'importe quelle page ; Kete comprend la note — un moment devient un
  rappel, un savoir devient une leçon proposée, un fait devient une correction à valider.

**Pourquoi.** Trois mécanismes séparés (tableau, routine, résumé) auraient donné trois écrans à
apprendre pour une seule idée : ce que je suis, ce que j'envoie, ce que je garde.

**Ce que ça coûte.** Un résumé indexé est une donnée de l'organisation : il suit les droits du
projet ou de l'équipe où il est rangé, et sa durée de conservation.

## D-053 — Tout ce qui capitalise suit un seul cycle : créer, utiliser, apprendre, évaluer, promouvoir

**Tranché le 2026-10-13** par l'auteur (« le concept de skills avec lessons qui capitalise la
connaissance de chaque personne afin qu'une personne autre que le designer puisse utiliser un agent
et que le design respecte tout […] Pareil pour les apps ? »). Précise les principes 1 et 5 et le
registre des ressources.

**Tranché ainsi.**
- **Un skill porte le savoir-faire d'une personne** — la designer, la comptable, le chef de
  chantier. Quelqu'un d'autre l'utilise par un agent, et le résultat le respecte sans qu'il ait à
  le connaître.
- **L'usage produit des leçons** : une correction, une remarque, un écart relevé par un agent.
  Recueillies avec consentement, elles sont des données, jamais des consignes, et arrivent chez la
  propriétaire du skill.
- **La propriétaire essaie, garde ou écarte** chaque leçon. Une leçon gardée devient un cas de
  test ; une nouvelle version doit réussir tous les cas précédents avant d'être publiée.
- **La promotion passe un palier à la fois** — moi, l'équipe, l'unité, l'organisation — avec une
  revue selon le risque.
- **Le même cycle vaut pour les agents** (l'autonomie se gagne par les preuves et se retire) **et
  pour les apps** (née dans la fabrique pour une personne ou une équipe, améliorée par ses retours,
  ses scénarios de test réussis, revue par l'informatique avant chaque palier).

**Pourquoi.** Le savoir d'une entreprise est dans la tête de quelques personnes et part avec elles.
Un seul cycle, visible, le fait passer de la personne à l'organisation sans le figer.

**Ce que ça coûte.** Une revue humaine à chaque version et à chaque palier ; une propriétaire par
skill, à remplacer quand elle part.

## D-054 — Le téléphone est natif : la pile du matin, la voix du soir, le terrain

**Tranché le 2026-10-13** par l'auteur (« fais et toi même fusionnes », sur la proposition : pour
beaucoup, le téléphone est l'outil principal). Précise D-045, règle 7.

**Tranché ainsi.** Sur un téléphone, Kete n'est pas l'écran d'ordinateur rétréci :
- **Le matin, la pile en plein écran** : une décision par écran, ses preuves en une ligne, Oui ou
  Non au pouce, jusqu'à « tout est réglé ».
- **Le soir, la voix** : la clôture se dit, dans Kete ou par une note vocale sur WhatsApp ; Kete
  répond par les rangements proposés, à valider d'un geste.
- **Le terrain** : la prochaine chose de la journée en grand, un rapport dicté puis relu à voix
  haute avant d'être validé, de grandes cibles, et « Plein soleil » pour lire dehors.

**Pourquoi.** Les gens qui font tourner une petite entreprise africaine décident entre deux
rendez-vous et rendent compte depuis un chantier. Ce qui se fait mal au pouce ne se fait pas.

**Ce que ça coûte.** Des écrans propres au téléphone, pas seulement des règles de mise en page ; la
voix suppose une transcription fiable en français parlé, à prouver avec de vraies notes.

## D-055 — Nettio est repris de zéro, dans un nouveau dépôt `kete-africa/nettio`

**Tranché le 2026-10-08** par l'auteur (« On va reprendre Nettio complètement de zéro », « une app
métier à commercialiser seule », « Il faut toujours penser WhatsApp et Telegram »). Précise
`ARCHITECTURE_APP.md` §10 pour Nettio, comme D-023 l'a fait pour Firmo.

**Tranché ainsi.** Nettio est réécrit comme une app Kete (D-015, D-016, D-034), né du gabarit de
`kete-core`, avec sa base Neon, dans un dépôt neuf `kete-africa/nettio`. À la différence de Firmo
(D-023), **la version de juillet 2026 n'est pas une source** : ni ses règles, ni ses écrans, ni sa
charte ne servent de référence. Les sources sont la discussion de l'auteur, cette doctrine et les
projets Kete en cours ; la vérité du produit est écrite dans `nettio/docs/product/`.

- **La douleur** : le patron d'un pressing ne sait pas s'il gagne réellement de l'argent — il vend
  au forfait, or ce que coûte un forfait dépend de son contenu réel. Nettio lui rend ce chiffre :
  tout l'argent, le contenu réel de chaque dépôt même sous forfait, une fiche de coût par pièce et
  par service.
- **Un outil complet par rôle, vendu seul** : abonnement par le Compte Kete, sans Kete Enterprise.
  Les rôles métier et leurs droits sont cochés par le patron ; les attributions du centre décident
  quand l'organisation les y gère.
- **Le design** est `@kete/design`, design `kete`, tel qu'il existe (pas de design propre, D-038
  non exercé).
- **Les chiffres sont calculés par le code, jamais par un modèle** ; Nettio ne fixe ni ne conseille
  un prix ; un agent prépare, une personne valide.
- **Les canaux** sont toujours WhatsApp et Telegram, derrière le port des canaux ; les adaptateurs
  écrits dans Nettio remontent au châssis par une issue (`kete-core#86`).

**Ce qui n'est pas encore su** : aucune parole du gérant pilote n'est consignée, et la preuve de la
douleur (la marge de ses forfaits, calculée à la main sur un mois) n'est pas faite. Tant qu'elle ne
l'est pas, la douleur reste une hypothèse.

## D-056 — Un seul modèle vivant : le journal, le fil, la tenue, le geste, la politique

**Tranché le 2026-10-15** par l'auteur (« quel est ton plan pour aller au bout en commençant par
l'unification ? », puis « Super, actualise la doc »), sur l'inventaire de `kete-core` et de
`kete-enterprise` : 32 paquets et 43 fonctions bien faits un à un, mais sans forme d'ensemble.
Précise D-042, D-047 et D-049.

**Tranché ainsi.** Toute l'entreprise tient en cinq objets vivants, au-dessus des trois références
du centre (structure, tiers, projets) et des objets des apps :
- **Le journal** : tout ce qui arrive — un message, un paiement, une décision, un fait d'une app —
  devient un événement daté, signé, jamais réécrit.
- **Le fil** : la conversation d'un objet (un projet, un tiers, un devis, un dossier, un ticket),
  qui naît avec lui et se range à sa clôture ; quelques fils libres et le fil de chacun avec Kete.
  Ses membres sont des personnes, des agents, et les contacts extérieurs par leur canal.
- **La tenue** : chaque chose en cours — qui la tient, ce qu'elle attend et de qui, depuis quand.
  **Aucun état ne permet « personne »** : ce qui vieillit est relancé, ce qu'un absent tient passe
  à son suppléant puis à son responsable.
- **Le geste** : chaque action proposée. Fait seul dans le mandat d'un agent, sinon une carte à
  décider, la même dans le fil, dans « Pour moi » et sur WhatsApp — réglée à un endroit, réglée
  partout.
- **La politique** (D-058) : ce qui décide si un geste se fait, avec quel accord, ou pas.

**Un routeur** rattache chaque événement à son objet, son fil et sa tenue ; quand il n'est pas sûr,
il le dit par une carte « à classer » plutôt que de deviner.

**Ce qui se fond dedans**, dans `kete-enterprise` : les six façons de dire « une chose en cours »
(demandes, à faire, actions de réunion, étapes de circuit, brouillons, tâches d'agents) deviennent
des tenues ; les cinq façons de se parler (assistant, échanges entre assistants, téléphone,
notifications, mail) deviennent des fils et des canaux ; la bibliothèque, les documents, les
dossiers, les savoir-faire et la mémoire deviennent un seul savoir. Les primitives communes vont
dans `kete-core` quand une deuxième app en a besoin.

**Quatre références rejoignent le centre** : les lieux, les actifs et le parc installé, le
catalogue, le groupe (plusieurs sociétés). Les fonds et les bailleurs restent des contrats de Kete
Commitments avec l'argent par projet ; les risques sont les constats de la conformité ; les
objectifs, la performance.

**Pourquoi.** Ce qui fluidifie une entreprise, c'est que rien n'attende entre deux personnes sans
que quelqu'un le sache. Six modèles de « chose en cours » sans vue commune rendent la question
« qui tient quoi ? » impossible à répondre ; c'est le travail sur le travail que Kete doit
supprimer.

**Ce que ça coûte.** Une reprise de fonctions qui marchent : chaque source branche sa tenue, puis
ses anciennes tables sont retirées une à une, sans tout réécrire d'un coup. Le routeur se
trompera ; il doit le dire, jamais le cacher.

## D-057 — L'écran : « Pour moi », la conversation au centre, l'état à côté

**Tranché le 2026-10-15** par l'auteur (« j'aimerais pouvoir avoir une démo complète […] c'est
après cela qu'on peut véritablement lancer le codage »), sur la discussion de l'interface de Buzz,
de Claude et de la maquette v4 « Kete par les fils ». Remplace l'accueil de D-045 (Décider) ;
précise D-050 et D-054.

**Tranché ainsi.** Chaque outil connu sert bien une de trois choses et mal les deux autres :
l'attention, la conversation, l'état. Kete les sépare et les relie par les mêmes objets.
- **On ouvre sur « Pour moi »** : à décider, à répondre, ce qui attend chez moi, à classer. Il
  remplace Décider et la cloche ; le matin, c'est la pile.
- **Le fil « Kete »** remplace la page Demander : le point du matin, ses questions, ses rappels.
- **La conversation est le moyen de se coordonner, pas la maison** : les fils de mes objets, peu
  dans la barre (les actifs, les épinglés), le reste par la recherche.
- **Les groupes sont normaux** (précisé le 2026-10-16, l'auteur : « les entreprises comme KYA
  utilisent beaucoup les mails […] avoir un Kete fil dans lequel on peut créer des groupes, faire
  des échanges avec des agents, ils acceptent ; ça évite trop de mails ») : ceux qui naissent de la
  structure (la direction, un service, l'équipe d'un projet) et ceux qu'on crée (un comité, un
  chantier, un appel d'offres), chacun avec un responsable. Le fil remplace le mail interne.
- **La trace au moins aussi bonne que le mail**, puisque c'est pour elle qu'on écrit des mails :
  chaque message est un événement daté, jamais réécrit (une modification garde l'original) ;
  « lu par » et sa date ; « pour action » devient une tenue, « pour info » un simple message ; les
  membres et abonnés disent qui savait et depuis quand ; les pièces gardées et versionnées ; la
  recherche ; la conservation fixée par une politique ; l'export d'un fil en preuve horodatée.
- **Le mail reste pour le dehors, branché sur les fils** : un mail reçu entre dans le fil de son
  dossier, une réponse part par mail depuis la boîte de la personne, un fil peut avoir son
  adresse. Qui préfère encore le mail reçoit le résumé de ses fils et y répond par mail.
- **Les agents sont membres des fils et parlent peu** : quand ils ont fini, ou besoin d'un geste.
- **L'état est à droite du fil** quand le fil porte un objet : qui tient quoi, ce qui attend et
  depuis quand, les chiffres, les dates.
- **Les cartes arrivent aussi sur WhatsApp et en notification** : on décide sans ouvrir Kete ; une
  réponse dictée devient des gestes. Le client, lui, reste sur WhatsApp.
- **Avant le code**, une simulation complète du système (HTML, CSS, JS) montre le flux de bout en
  bout ; l'auteur la valide, puis une maquette v5 valide les écrans.

**Pourquoi.** Slack et WhatsApp noient l'attention, les ERP n'ont pas la conversation, le mail
mélange tout. La ressource rare d'une personne, c'est son attention ; la première question du
matin est « qu'est-ce qui a besoin de moi ? ».

**Ce que ça coûte.** C'est un pari : que les équipes travaillent dans des fils Kete plutôt que
dans leurs mails et leurs groupes WhatsApp. Chez KYA, où le mail sert à tracer, les fils sont
acceptés s'ils tracent aussi bien. Il se juge à l'usage, à la fin. L'API WhatsApp Business a ses règles
(modèles approuvés, fenêtre de 24 h, restrictions de Meta sur les assistants d'IA généralistes) :
à vérifier avant de bâtir les cartes dessus ; Telegram et les notifications de l'app en relais.

## D-058 — La gouvernance : un seul moteur de politiques, appliqué au geste

**Tranché le 2026-10-15** par l'auteur (« Gouvernance, policies, doit-on compléter des éléments
centraux d'une entreprise ? », puis « Super, actualise la doc »). Précise D-028, D-040 et D-043.

**Tranché ainsi.**
- **Une politique est une phrase** avec son périmètre (unités, projets, montants, canal, tiers),
  son responsable, sa version et sa période d'essai. Elle s'évalue au seul endroit où tout passe :
  le geste, d'une personne ou d'un agent. Elle répond : autorisé ; autorisé avec l'accord d'un
  circuit ; refusé, en disant par quelle politique.
- **Les droits restent** ce qu'ils sont — qui tient quoi, où (D-028). Les circuits d'approbation
  et les règles des agents (D-043) deviennent des politiques : un seul moteur pour la même question,
  « qui peut faire quoi, jusqu'à combien, avec quel accord ». Les contrôles de conformité (D-040)
  pointent vers elles : une politique tenue devient une preuve.
- **Six politiques qu'on doit pouvoir écrire** : qui engage l'entreprise (pouvoirs de signature) ;
  qui parle au client en son nom, sur quel canal, avec quels modèles ; les limites de dépense par
  rôle et par projet ; la suppléance ; la conservation et la confidentialité ; le consentement des
  contacts extérieurs.

**Pourquoi.** Des agents vont écrire aux clients et engager des dépenses. La confiance tient à une
seule réponse, la même pour une personne et pour un agent, journalisée avec ce qui l'a décidée.

**Ce que ça coûte.** Reprendre deux moteurs qui marchent (circuits et règles) en un seul. Une
politique trop large bloque tout : chacune naît à l'essai, observée avant d'être appliquée.

## D-059 — kete.software, une démo publique et Kete Intelligence dans chaque app, généraliser

**Tranché le 2026-10-16** par l'auteur (« je deviens kete.software car mondial. Pour chacune des
apps, il faut la démo publique, ça doit faire partie des principes, comme le fait d'avoir Kete
Intelligence à l'intérieur des apps. Si tout est implémenté les tarifs viendront ; il faut, au fur
et à mesure, qu'on généralise beaucoup plus pour aller vite »). Précise D-001, D-045 et la règle 4
de la feuille de route.

**Tranché ainsi.**
- **Le domaine principal devient `kete.software`**, parce que Kete vise le monde : le site, le
  Compte Kete, le Cockpit et les apps s'y rangent. L'organisation GitHub reste `kete-africa` tant
  qu'aucune autre décision ne la change.
- **Chaque app a sa démo publique**, jouable sans compte : on la parcourt, on joue les rôles, on
  voit ce qu'elle fait vraiment, comme la simulation du système unifié. C'est un principe (le 8e).
- **Kete Intelligence est dans chaque app** : le même tiroir, le même fil, les mêmes règles —
  agir avec les droits de la personne, préparer, laisser décider. C'est un principe (le 9e).
- **Les tarifs viennent quand tout est implémenté** ; ils ne bloquent rien avant.
- **Généraliser à chaque pas** : un besoin manifestement commun est construit dès sa première
  occurrence comme un module autonome, réutilisable par le centre, les apps, le Cockpit et Pono.
  La règle « un module entre dans le socle quand deux produits en ont besoin » s'assouplit : quand
  le second usage est déjà connu, on n'attend pas qu'il arrive.

**Pourquoi.** Une démo qu'on joue vend mieux qu'une page qui promet, et elle prouve d'abord à
nous-mêmes que le flux tient. Kete Intelligence partout fait de chaque app une porte vers le même
système. Généraliser tôt évite d'écrire deux fois ce que le centre, les apps et Pono partagent.

**Ce que ça coûte.** Une démo par app à tenir à jour avec l'app. Généraliser trop tôt peut figer
un module avant de connaître son second usage : on ne généralise que ce dont le second usage est
déjà connu.

## D-060 — Le paramétrage commun, des fiches solides, la fabrication et des agents à niveau

**Tranché le 2026-10-17** par l'auteur (« Je valide, suis le plan et continue »), sur la discussion
du même jour : le rôle de chaque fiche, le groupe, la solidité du modèle, le paramétrage des apps,
la fabrication chez KYA (« KYA commercialise des systèmes électroniques fabriqués de bout en bout.
On peut faire l'essentiel et après ajouter »), et les agents face à Grok et Rakazo. Précise D-041,
D-047, D-056 et D-059.

**Tranché ainsi.**
- **Un paramétrage commun, présent partout comme Kete Intelligence.** Chaque réglage est déclaré une
  fois par son propriétaire — le socle ou une app, dans son manifeste — avec son schéma, son défaut,
  les couches où il se fixe, qui peut le changer, ses mots et sa sensibilité ; ses changements sont
  journalisés. Il se résout par couches, la plus précise l'emporte, et l'écran dit d'où vient la
  valeur : Kete (les défauts), l'organisation, l'app (pour toute l'organisation), l'entité
  juridique ou l'unité (une filiale, un site : plus précise que l'app), la personne, l'appareil. Les préférences de la personne (langue, thème, fuseau, heures calmes…) vivent dans le
  Compte Kete et la suivent dans toutes les apps ; aucune app ne lit plus sa devise ou sa langue
  dans une variable d'environnement. Le même panneau « Réglages » est dans le cadre de chaque app.
- **Le groupe n'est pas une fiche** : la structure souple (D-041) le représente déjà — des unités
  dont le type est marqué « entité juridique ». Ce qui manquait est **l'entité juridique portée par
  les documents et les faits** (qui facture, numérotation, consolidation) et sa fiche (NIF, RCCM,
  mentions, devise, séries), qui est une couche du paramétrage.
- **Toutes les fiches suivent les mêmes règles** : un identifiant stable et la fusion des doublons ;
  des dates de validité, l'historique gardé ; un responsable ; un fil et un journal ; une
  confidentialité ; des identifiants externes pour reprendre l'existant ; une seule source de
  vérité, citée et jamais recopiée.
- **Ce qui complète l'existant** : les contacts d'un tiers et les liens entre tiers ; les phases
  d'une affaire, de la demande au SAV (une opportunité est une affaire en phase « demande ») ; les
  axes de chaque fait d'argent (entité, unité, projet, poste) ; le calendrier de l'organisation
  (jours ouvrés, fériés par pays, heures ouvrées) ; les unités de mesure et leurs conversions.
- **Les nouvelles fiches** : les lieux ; le catalogue (articles, prestations, kits composés, prix
  datés) ; le stock et ses mouvements ; les actifs et le parc installé (une garantie est une
  obligation d'un contrat qui vise des actifs).
- **La fabrication, l'essentiel d'abord** : la nomenclature sur plusieurs niveaux, l'ordre de
  fabrication qui consomme le stock et produit des articles numérotés, la traçabilité des
  composants par numéro de série, le contrôle de sortie avec sa preuve. Les gammes, la
  planification des besoins et le coût de revient viennent après.
- **Un test de solidité avant de coder les fiches** : trois parcours réels de KYA (une fabrication,
  une vente avec pose, un SAV sous garantie) et une journée de pressing, déroulés champ par champ
  sur le modèle ; chaque case d'un document retrouve sa fiche ou son fait.
- **Des agents à niveau** (étape C4) : la recherche sur le web, la réponse à voix haute et l'appel,
  l'import d'outils (OpenAPI, serveurs MCP distants), un ordinateur pour l'agent dans le bac à sable,
  la délégation à des sous-agents — toujours sous les politiques, les gestes engageants en
  brouillon. Une bibliothèque d'abord, un service seulement sans équivalent de même qualité.
- **Hors du modèle, jusqu'à un client réel** : la paie, la comptabilité générale légale (un
  connecteur vers le logiciel comptable), la vente en ligne.
- **Les outils métier sont des compositions** : le socle, les fiches communes, des briques métier
  partagées (flux d'étapes, fiche de coût, caisse, documents légaux, périphériques, créneaux) et un
  petit cœur propre au métier. Une app vendue seule garde ses fiches et les fait promouvoir au centre
  quand elle le rejoint. Rien n'est élargi avant le test de KYA.

**Pourquoi.** Chaque app réglait sa langue, sa devise et son thème à sa manière, et le Compte Kete
avait des réglages que personne ne lisait : un paramétrage commun fait gagner chaque app et suit la
personne partout. Un modèle solide se prouve sur de vrais documents, pas sur une grille. Une
entreprise qui fabrique ne tient pas sans nomenclature ni traçabilité. Des agents en deçà des
assistants grand public seraient un recul, quelle que soit la qualité du reste.

**Ce que ça coûte.** Un module de plus à brancher dans toutes les apps et le Compte Kete. Le test de
solidité demande les vrais documents de KYA. La fabrication et le stock élargissent A6 ; le chemin
vers le compte autonome de KYA (paramétrage, A6 essentiel, B1, B3, B2, C4, E3 à E5) passe avant
tout le reste.

## D-061 — Les fils, lieu de l'entreprise ; Kete, sa porte ; les agents, ses délégués

**Tranché le 2026-10-21** par l'auteur, après une journée de discussion qui a suivi son test des fils,
puis sur les maquettes v6 à v6.2 (« C'est complet ? Si oui, rédige toutes les décisions et implémente
de bout en bout »). Précise D-056, D-057, D-058 et D-060. S'inspire de WhatsApp, Slack, Linear,
Grok Bot, Rakazo et Chatwoot, sans reprendre leur logiciel. La maquette de référence est
`kete-core/docs/brief-ui/canevas-v6.2.html`.

**Tranché ainsi.**

- **Kete est pour les gens de l'entreprise.** Les clients restent sur WhatsApp et le mail ; ce qu'ils
  écrivent entre dans le fil de leur objet. Pas de « relation client » à la Chatwoot. Une seule
  idée en reste : une conversation qui demande quelque chose a toujours un responsable, la tenue.
- **Quatre mots, un rôle chacun.**
  - **Les fils** sont le lieu : le canal interne de toute l'entreprise.
  - **Kete** est l'assistant de chacun. Il agit en tant que la personne, jamais au-delà de ses
    droits. Il est la porte d'entrée : il répond lui-même ou confie le travail aux bons agents, en
    parallèle.
  - **Les agents** sont des délégués : une fiche de poste, un responsable humain, un budget, des
    déclencheurs et leur propre fil.
  - **Kete Intelligence** est le moteur : le modèle, le tour d'agent, les droits, les politiques, la
    mesure. Le tiroir de chaque app n'est qu'un raccourci vers le fil Kete de la personne.
- **Une seule conversation.**
  - Parler à Kete se fait dans un fil privé. On peut y inviter un collègue ; il devient alors un
    groupe.
  - « @Kete » dans un fil lance le même tour visible que Kete Intelligence.
  - Dans un fil, Kete ne répond devant tous qu'avec ce que tous les membres peuvent lire. Sinon, sa
    réponse est « Seulement pour vous », et la personne peut la partager.
  - Ouvrir un objet, c'est ouvrir son fil.
- **Les modules.**
  - `@kete/threads` garde les données.
  - `@kete/conversation` est l'écran des fils, réutilisable par toute app.
  - Un seul champ de saisie, dans `@kete/design`, partagé avec Kete Intelligence.
- **Le confort d'une conversation d'aujourd'hui.**
  - Les vocaux sont transcrits ; le micro remplace la dictée.
  - Les notifications sur le téléphone se règlent par fil (toutes, mentions, aucune) et ne sonnent
    que si l'ordinateur n'a pas vu.
  - Les photos s'affichent en miniature et s'ouvrent en grand.
  - Les fichiers vont jusqu'à 100 Mo et sont stockés hors de la base.
  - Les messages se chargent par pages de cinquante ; un brouillon est gardé par fil.
  - Les réactions, « … écrit », les épingles et l'aperçu des liens.
  - Supprimer un message laisse « Message supprimé » ; l'original reste dans la preuve.
- **Le champ de saisie.**
  - Une ligne qui grandit ; 🎤 devient ➤ dès qu'on écrit.
  - ＋ ; « / » ; « @ » pour quelqu'un ; « # » pour quelque chose.
  - Deux bascules, qui reviennent par défaut après l'envoi :
    - « Interne / Au client » : le cadre passe en alerte et le canal est dit ;
    - « Pour info / Pour action » : à qui, pour quand, quelle priorité.
  - Sur un message, trois gestes visibles ; le reste sous « ⋯ ».
- **« Infos du fil »**, comme sur WhatsApp : chercher, les notifications, les épinglés, les photos et
  vidéos, les documents et leurs versions, les liens, les vocaux, les actions, les décisions, les
  membres.
- **Citer un objet avec « # ».**
  - On peut citer un projet, un tiers, un ticket, un devis, une facture, un contrat, un congé, un
    document, une décision, une action, une réunion ou un équipement.
  - L'étiquette dit l'état de maintenant et respecte les droits.
  - L'objet garde la liste des fils où il est cité (« Cité dans ») ; un fil peut se rattacher à
    plusieurs objets.
  - Kete suggère un lien, sans l'imposer.
- **Confier une tâche suit un seul chemin**, dans cet ordre :
  1. capter : un vocal, un message, un mail ;
  2. comprendre ;
  3. rattacher à l'objet ;
  4. proposer un lot de gestes ;
  5. la personne confirme ;
  6. exécuter : tenues, politiques, agents ;
  7. suivre : rappel, suppléant, puis manager ;
  8. rendre au responsable de l'étape suivante.

  Une consigne qui énonce une règle (« tout achat au-delà de 50 000 F passe par moi ») devient une
  politique, proposée et simulée. Le reste devient des tenues.
- **Les agents, comme des collègues.**
  - Chacun a son fil ; on lui confie un travail en lui parlant.
  - Son état se voit d'un coup d'œil : a besoin de vous, travaille, a fini, en veille.
  - Son travail se lit en plan et en étapes repliées. On peut l'arrêter, ou lui parler sans
    l'arrêter.
  - Ses demandes ne bloquent rien : « Autoriser une fois », « Toujours… » (qui propose une politique
    simulée) ou « Refuser ». Une demande venue d'une routine expire, et rien ne part.
  - Signer et payer reviennent toujours à la personne.
  - Un agent se crée en une phrase et commence en essai.
- **Un agent n'est jamais responsable d'une tenue**, seulement son délégué : la tenue a toujours une
  personne pour responsable.
  - **La prise en charge** se règle dans sa fiche, geste par geste : jamais, propose (par défaut), ou
    prend seul (gagné par les preuves).
  - **Chaque tenue dit à qui rendre** : à qui revient l'étape suivante selon la politique ou le
    circuit, sinon à qui l'a confiée. Le résultat est toujours posté dans le fil de l'objet. Si
    personne n'est désigné, l'agent demande.
- **Savoir-faire, routine, agent** : le comment, le quand, le qui. Une consigne qui revient est une
  routine. Un poste avec du jugement et un responsable est un agent.
- **L'ordinateur d'un agent** (le bac à sable) se règle agent par agent, avec un plafond de minutes.
  Il ne sert que pour un site sans API, un savoir-faire avec des scripts, un gros fichier ou la
  fabrication d'une app. Le reste passe par les capacités de Kete.
- **Les mails.**
  - Les boîtes communes sont lues en entier.
  - D'une boîte personnelle, Kete ne lit que les échanges avec un contact connu d'un objet, le
    dossier « Kete » et les mails qui mettent un fil en copie. Jamais le reste. Les Envoyés suivent
    la même règle.
  - Un mail trouve son fil dans cet ordre : ses en-têtes de réponse, l'adresse du fil, un contact
    connu, le modèle quand il est sûr ; sinon, il va « à classer ».
  - Il devient un message propre, l'original à un clic. Lu dans deux boîtes, il ne s'affiche qu'une
    fois. Ses pièces jointes rejoignent les fichiers du fil.
- **Les autres conversations.**
  - Les groupes WhatsApp personnels entrent par leur export, jamais par une bibliothèque non
    officielle. De même pour les exports Telegram et les mails en fichier.
  - Le compte rendu d'une réunion entre dans son fil, et ses actions deviennent des tenues.
  - Deux fils peuvent être fusionnés.
- **La fluidité.** Un objet, un seul endroit. On ne choisit jamais l'outil. Décidé là où l'on est,
  décidé partout. Rien n'est ressaisi. Les agents parlent peu. On n'est dérangé que si c'est
  nécessaire.
- **Le dessin.** Aucun composant ne porte de bordure colorée à gauche. L'état se dit par une
  étiquette, une icône ou une teinte.

**Pourquoi.** Le fil doit être l'environnement de discussion de l'entreprise. Sans le confort d'un
chat d'aujourd'hui, les équipes restent dans leurs groupes WhatsApp et leurs mails, et Kete ne voit
rien. Avoir deux conversations (les fils et Kete Intelligence), c'était avoir deux mémoires. Enfin,
les agents ne sont utiles que si l'on voit ce qu'ils font, s'ils ne bloquent personne et si une
personne en répond.

**Ce que ça coûte.**
- Un module d'écran de plus dans le noyau.
- Le stockage des fichiers hors de la base.
- Une migration : la tenue ne peut plus avoir un agent pour responsable.

Restent ouverts : le domaine des adresses de fil, à choisir par l'auteur, et la carte des flux de
chaque module, qui attend les chiffres réels de KYA.

## D-062 — L'objet au centre : vingt-deux règles pour un système complet par construction

**Tranché le 2026-10-23** par l'auteur, au terme de deux jours de discussion (« note les toutes […]
ces règles vont te guider après » ; « Ajuste ce que tu dois » ; « Rajoute et on continue » ; « Vas y
en actualisant d'abord les principes et décisions » ; « on raisonne au dessus de KYA »). Précise
D-047, D-052, D-056, D-058 et D-061, et les principes 2, 4 et 5, sans les réécrire. S'inspire de
NocoBase et de Microsoft Copilot Studio, lus en profondeur, sans reprendre leur logiciel. La
première entreprise qui éprouvera ces règles viendra après : elles sont écrites pour toute
organisation.

**Le constat.** En vérifiant le code, les modules se sont révélés bien faits un à un, mais
construits chacun pour son écran, sans contrat envers les autres. Les agents ne reçoivent pas les
outils des apps ; les tableaux de bord ignorent le projet ; quatre systèmes de chiffres coexistent
(les indicateurs de la performance, les tableaux sur jeux de données, `@kete/metrics`, les jeux de
données des apps) ; trois chemins séparés connectent un outil externe. Aucun n'est un défaut : ce
sont des liens qu'aucune règle n'exigeait.

**Tranché ainsi.**

*La structure*

- **R1 — L'objet au centre.** Tout ce qui compte est un objet — un projet, un tiers, un ticket, une
  facture, un contrat, un équipement. Un objet a un fil, une personne responsable, une équipe, et
  des axes. Rien n'existe à côté d'un objet.
- **R2 — Quatre axes, partout.** Le projet, le tiers, l'unité, la personne. Une tenue, une date, un
  fait d'argent, un mail, une ligne de données, un chiffre, un agent portent les axes de leur objet ;
  filtrer par projet marche partout sans code particulier. On n'ajoute pas d'axe pour un besoin : un
  site est une sorte d'unité.
- **R3 — Déclaré une fois, servi partout.** Une app déclare ses objets, ses outils, ses jeux de
  données, ses chiffres, ses surveillances, ses vues et ses raccourcis. Les écrans, Kete, les
  agents, les copilotes par MCP, les tableaux et les résumés lisent cette seule déclaration ; aucun
  ne tient sa propre liste.
- **R4 — Les mêmes droits partout** (principe 4, D-047). Ce qu'une personne voit à l'écran est
  exactement ce que voient son Kete, ses agents, ses tableaux et ses copilotes.
- **R5 — Un agent, c'est Kete réduit à une fiche.** Il reçoit les outils de sa personne, filtrés par
  sa fiche, ses niveaux, son budget et les politiques. Sa fiche choisit ses sources d'outils —
  telle app oui, telle autre non — pour qu'il choisisse mieux et coûte moins. Délégué, jamais
  responsable (D-061).
- **R6 — Un seul modèle d'acteur.** Une personne, un agent, Kete, un contact ont un nom, un avatar,
  une forme et une provenance, dessinés de la même façon partout. L'agent a un carré arrondi, la
  personne un rond : on ne confond jamais un agent avec un collègue.
- **R7 — Un chiffre est vivant et prouvé.** Il est lu à l'ouverture, avec les droits du lecteur et
  les filtres du tableau, et il montre d'où il vient. Il n'est figé que dans un résumé, par choix
  (D-052).
- **R8 — Une connexion, trois usages.** Un outil externe se connecte une seule fois ; il sert à lire
  (les tableaux, Kete), à agir (les agents, en brouillon) et à signaler (« Décider »). Lire, agir et
  signaler sont trois permissions distinctes ; agir n'est jamais accordé par défaut.
- **R9 — Ce qui engage passe par un brouillon** (« l'IA prépare, l'humain valide »).
- **R10 — Un module n'est fini que lorsqu'il sert les autres.** Il répond à sept questions : ses
  objets et leurs axes ; le fil de chaque objet ; ses droits sur les deux axes ; les outils qu'il
  donne à Kete, aux agents et aux copilotes ; les données et les chiffres qu'il fournit ; ses
  surveillances ; sa documentation, son diagramme, sa maquette. Une question peut recevoir « sans
  objet », avec sa raison.

*La vie dans le temps*

- **R11 — Les événements.** Un objet qui change le dit ; son fil, les agents, les tableaux et
  « Pour moi » l'apprennent. Dynamique veut dire « mis à jour sous les yeux », pas seulement
  « relu ». Bâti sur ce qui existe (la file sortante, le direct des fils), sans nouveau service ;
  un événement reçu deux fois n'agit qu'une fois.
- **R12 — La vie d'un objet.** Naître, changer d'état, se clore, s'archiver, se conserver,
  s'exporter, s'effacer — et ce que deviennent alors son fil, ses agents, ses tableaux. Les durées
  de conservation relèvent du droit et de l'auteur : Kete propose des valeurs, l'auteur tranche.
- **R13 — Une seule identité par objet, entre les apps.** Le client d'une app et le tiers du centre
  sont un seul tiers ; l'objet né d'une app garde d'où il vient. Kete propose la fusion de deux
  doublons ; une personne la confirme. Jamais de fusion automatique.
- **R14 — L'attention.** Un seul modèle décide qui est prévenu, de quoi, par quel canal, une seule
  fois : « Pour moi », le téléphone, WhatsApp, Telegram, le niveau choisi par fil.
- **R15 — Tout objet se cherche et se cite**, indexé avec ses droits, cité par « # », retrouvé par
  Kete et les agents.
- **R16 — La preuve.** Tout geste est journalisé — qui, pour qui, par quel canal, quand — et
  « Comment ? » a toujours une réponse, pour chaque module, les agents et les connexions compris.
- **R17 — Le mode dégradé.** Une app qui ne répond pas, une connexion expirée, un plafond atteint :
  l'écran le dit (absent, refusé, à reconnecter). Rien ne casse en silence. Une donnée absente se
  montre comme telle, jamais comme un zéro.
- **R18 — Le coût visible.** L'IA, les minutes d'ordinateur, les appels externes sont mesurés par
  organisation, par unité, par agent et par personne, avec des budgets ; une demande de rallonge
  arrive dans « Décider ».
- **R19 — Le terrain** (principe 7). Un téléphone en 3G, le français, le franc CFA, les fuseaux ; le
  hors-ligne plus tard.
- **R20 — Chaque module se démontre** (principe 8) : ses données de démonstration et ses captures
  face à la maquette font partie de « fini ».
- **R21 — Un agent se prouve** (principe 5). Kete et chaque agent ont un jeu de cas tiré de leurs
  vraies tâches et de cas écrits ; il est rejoué avant tout changement de fiche, de modèle ou
  d'outils, avec les droits d'une personne donnée, noté (le sens, la sécurité), et sa note paraît
  dans le bilan de l'agent.
- **R22 — Un composant, mille usages.** Quelques composants génériques — la fiche d'objet, la
  collection, le chiffre, le tableau de bord, le formulaire, la frise, avec le fil, le champ de
  saisie et la carte de brouillon — configurés à l'endroit où ils servent. La configuration est une
  donnée, versionnée et prouvée, jamais du code ni du SQL : l'app donne le réglage par défaut,
  l'organisation l'ajuste par poste, la personne fait sa version, et Kete peut la changer sur une
  phrase. La même configuration s'affiche dans Kete, sur le téléphone et chez les copilotes
  (D-037).

*Le poids des règles.* R1 et R2 d'abord, puisque tout en dépend ; puis R3, R5, R7 avec R11, et R8 :
ce sont elles qui créent les liens. R12 à R20 sont des garanties de qualité : elles empêchent un
module livré de se dégrader.

*Trois orientations de l'auteur*

- **Des agents disponibles pour tous, livrés avec le système.** Le cœur et chaque app livrent des
  agents prêts (D-039 en prévoit le type) : l'administrateur les active, chacun les reçoit selon son
  poste, et ils agissent pour la personne qui s'en sert, avec ses droits (R5), évalués (R21).
- **La manière d'évaluer les gens peut changer.** L'évaluation peut reposer sur ce qui s'est
  réellement passé dans les objets — les promesses tenues, les tenues closes à temps, l'aide
  apportée, les idées retenues — plutôt que sur ce qu'on déclare. Les garde-fous : la personne voit
  ses propres données d'abord et en continu ; seuls les indicateurs notifiés par écrit servent à
  l'évaluer ; le reste l'aide, jamais il ne la note ; l'IA prépare, une personne juge. Ce n'est pas
  de la surveillance : on mesure des résultats, jamais une activité.
- **Ce qui fait un bon agent**, à permissions égales, dans l'ordre : le contexte de l'objet, la
  qualité des outils et des données, les savoir-faire de la maison, la clarté de la fiche, la boucle
  de corrections, puis le modèle. Les procédures écrites d'une entreprise deviennent naturellement
  les savoir-faire de ses agents.

*Ce que l'on prend ailleurs, et ce que l'on ne prend pas*

- **Pris** : les évaluations d'agents (R21) ; les variables de contexte dans les tableaux (« ce
  projet », « moi », « mon unité ») et le filtre de page qui alimente toutes les cartes ; les
  déclencheurs d'événements pour les agents ; les raccourcis de tâches et les modèles d'agents
  déclarés par les apps ; une mémoire par personne, privée, qu'elle voit et efface, éteinte dans
  les fils de groupe ; les budgets de coût avec demande de rallonge ; l'inventaire des agents pour
  l'administrateur ; les versions de la fiche d'un agent ; des permissions au niveau du champ
  seulement quand un besoin réel le demande.
- **Pas pris** : le constructeur d'apps sans code (nos apps sont du code, déclaré une fois) ; le SQL
  et le JavaScript dans les graphiques ; les agents à scénarios figés ; l'agent qui parle
  directement aux clients avec renvoi à un humain (D-061 garde les clients sur WhatsApp et le mail,
  dans le fil de leur objet).
- **Ce qui reste propre à Kete** : le fil d'objet comme lieu de travail ; « Kete propose, la
  personne confirme », avec les politiques nées d'une phrase ; WhatsApp et Telegram en premier ; le
  terrain.

*Comment on prouve qu'un système est complet.* Les règles seules ne le prouvent pas. Deux épreuves
le font : un audit de chaque module et de chaque app contre R1 à R22, vérifié dans le code, dont le
tableau « fait / manque » devient le plan ; puis une journée réelle d'une entreprise, de bout en
bout. Là où elle casse, il manque un lien.

**Pourquoi.** Les trous trouvés en deux jours ont une seule cause : on a élargi plus vite qu'on n'a
relié. Avec ces règles, chaque spec devient un contrat entre modules ; on ne se demande plus
seulement ce que montre l'écran, mais ce que le module doit à Kete, aux agents, aux tableaux et aux
autres apps. Le système devient complet par construction, et non par rattrapage.

**Ce que ça coûte.**
- Chaque spec coche la définition de fini (R10), et les specs déjà livrées passent l'audit.
- Des reprises : un seul système de chiffres au lieu de quatre, une seule manière de connecter un
  outil au lieu de trois, des agents qui reçoivent enfin les outils des apps.
- Un passage technique en profondeur avant toute construction : ce qui est encore une proposition
  (le module de la Mesure, les types d'objets et leurs liens, la liste des composants et des
  graphiques, la place d'un ERP existant) est consigné dans
  `journal/2026-10-23-l-objet-au-centre.md` et sera tranché par ce passage.
