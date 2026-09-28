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
