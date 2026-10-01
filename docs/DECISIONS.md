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
