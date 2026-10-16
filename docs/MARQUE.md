# Marque

## Le nom

**Kete** : dans la tradition éwée, le nom du tissu que le reste du monde appelle *kente* (sens à
valider avec des locuteurs et des tisserands). Le kente se tisse en bandes étroites assemblées en
un seul tissu : des capacités modulaires sur un même socle.

- Domaine : **kete.software** (D-059, parce que Kete vise le monde ; auparavant kete.africa).
  Organisation GitHub : **kete-africa** (`kete` était pris).
- Risque connu : **Kete Inc.** (getkete.com, IA pour la gestion de patrimoine, États-Unis) a déposé
  la marque KETE aux États-Unis le 28 avril 2026. Voir D-001.

## Architecture de marque

| Niveau | Nom |
|---|---|
| Maison | Kete |
| Parties | Kete Apps · Kete Consulting · Kete Enterprise |
| Apps | Firmo, Nettio, Nyatefe, Kete Cockpit |
| Produit endossé | Pono, « par Kete » |

Règles : les noms des parties sont en anglais, le contenu en français (marché francophone d'abord).
Chaque app garde son nom, avec ce qu'elle fait à côté.

## Signature

**« Outils de demain pour une meilleure productivité »** (reçue, `FONDEMENT.md`).
Seconde phrase proposée pour la communication : **« L'IA prépare, vous décidez. »**

## Logo

- **Le K qui prend racine** : la jambe du K devient racine. Rouge chaud.
- Version actuelle **sans fil entrelacé** : avec le fil, le symbole se lisait comme un « A » sous le
  K. Le tissage passe par la bande kete (ci-dessous).
- Fichiers dans `brand/` : avatar (latérite, symbole sable), symbole seul en latérite et en sable.
- Concept à affiner par un designer : racines effilées, jonction plus douce en bas du K.

## Couleurs

| Nom | Valeur | Rôle |
|---|---|---|
| Latérite | `#B83A1B` | Marque, boutons, liens. Rare et forte (environ 10 % de la surface) |
| Braise | `#E2572D` | Accent, illustrations, jamais du texte |
| Ocre | `#C98A2B` | « À vérifier » |
| Racine | `#5A1E12` | Fonds sombres de marque |
| Terre | `#2A1610` | Texte principal |
| Écorce | `#6B4E43` | Texte secondaire |
| Argile | `#F4E6DA` | Surfaces |
| Sable | `#FBF6F0` | Fond de page |

États : validé `#2F7D4F`, à vérifier `#C98A2B` (texte `#7A4A0B`), erreur `#9B1C3C` (vin),
information `#2B5C8A`.

Règles du rouge :
- **Une erreur n'est jamais en latérite**, mais en vin, avec une icône et un mot.
- **Un chiffre négatif ou une dette n'est jamais en latérite** (« être dans le rouge »).
- Rester côté terre : ne pas « corriger » la latérite vers un rouge vif.
- Le rouge vif associé au noir évoque le deuil dans certaines traditions de la région : à valider
  localement pour les grands aplats sombres avec élément rouge.

## Style : v1 rectangle (D-010)

La rigueur de la forme, la chaleur de la matière. Inspirée de la rigueur de Porsche sans la copier,
rattachée à la géométrie du kete.

- **Formes** : rayon 0 pour les sections et les cartes, 2 px pour les boutons, champs et
  étiquettes, 22 % seulement pour l'icône d'app. Séparations par filets de 1 px, jamais par des
  ombres ni des cartes arrondies.
- **Grille** : 12 colonnes, gouttières de 16 px (24 px sur le site).
- **Titres** : Archivo élargie (`font-stretch` 118 %), 600 à 700. Petits titres de section en
  capitales espacées.
- **Texte** : Instrument Sans. **Chiffres** : JetBrains Mono, chasse fixe, alignés à droite.
- **Étiquettes** : rectangulaires, avec un petit carré de couleur (lisibles sans voir les couleurs).
- **La bande kete** : blocs rectangulaires latérite, ocre, terre, racine, braise. Fine (6 à 10 px)
  en tête de page et de carte importante, large sur les supports imprimés. Jamais derrière du texte.
- **Zones tactiles** d'au moins 44 px.
- **Kete Apps** : même système, avec plus de rouge, une voix chaleureuse et les racines dans les
  illustrations, pour rester accueillantes.

La v0 (angles arrondis, Bricolage Grotesque) est abandonnée.

Maquettes : toile de design « Kete — logo et design system »
(https://claude.ai/artifact/RuHZXFNH1jwLKLLUonQT7q, privée).

## Le composant signature

**La carte de vérification** : un brouillon préparé par l'agent, où chaque champ dit d'où il vient
(« tiré du message », « incertain », « tarif habituel »), avec Corriger et Valider. On la retrouve
dans tous les produits Kete.

**Les états de l'agent** : préparé (carré vide), corrigé, vérifié, refusé (carré plein : décidé par
un humain).

## La voix

- **Simple** : « Ton devis est prêt », pas « Le document a été généré avec succès ».
- **Vraie** : « L'agent a deviné ce prix, vérifie-le ».
- **Chaleureuse** : « Bonne journée, 3 clients t'attendent ».
- Proposition : « tu » avec les commerçants et dans les apps, « vous » avec les entreprises et sur
  le site.

## Reste à faire

Mode sombre, palette des graphiques, composants (confirmation, notification, page vide avec la
graine, erreur de formulaire), passage au code en `@kete/design` sur le modèle de `@pono/design`.
