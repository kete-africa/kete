# 2026-10-13 — Le centre, la confiance, les collègues

Réflexion avec l'agent, du 12 au 13 octobre, en revenant sur `kete-core` et `kete-enterprise` après
Nettio, jusqu'aux décisions D-042 à D-046.

## D'où l'on partait

- `kete-core` : 23 paquets publiés, mais plusieurs livraient un port sans adaptateur. Firmo puis
  Nettio portaient chacun leur copie de WhatsApp et de Telegram ; l'assistant était écrit dans Kete
  Enterprise et réécrit dans Nettio.
- `kete-enterprise` : 59 specs fusionnées en deux semaines, 35 domaines, 60 écrans, un menu d'une
  vingtaine d'entrées, quatre outils métier logés dans le centre, aucun usage réel.
- Aucune entreprise ne pouvait entrer seule : ni console, ni offres avec limites, ni essai.

## Ce qui a été examiné

- **Faire de « Kete Intelligence » un produit vendu à d'autres éditeurs.** Écarté pour l'instant :
  le terrain est occupé, et ce qui distingue Kete ne tient que sur son socle.
- **CopilotKit et Mastra.** Mastra retenu pour le moteur, à l'essai ; CopilotKit écarté (une
  seconde pile d'interface, et sa liaison avec Mastra ne gère pas la reprise dans un processus).
- **Se mettre « au niveau de ChatGPT, de Claude et de Codex ».** Leur structure a été étudiée (les
  fils rangés par projet, les fichiers ouverts sur place, la revue des changements, le panneau de
  tâche). L'agent a reconnu que les copier donnait un bon produit de 2025, pas ce qu'on voudrait
  utiliser : la matinée réglée en quelques décisions passe devant le fil de discussion.
- **Le regard d'une très grande entreprise.** Elle n'achèterait pas le produit (ni annuaire, ni
  certification, ni connecteurs), mais ce sont les idées de Kete qu'elle cherche : mandat,
  brouillon, autonomie par tâche, règles, registre. D'où la confiance comme cœur.
- **Les agents de chacun.** Le concept est venu de l'auteur : des agents privés, des agents
  partagés, et une demande adressée à la personne.

## Ce qui a été retenu

D-042 (trois endroits, un outil métier est une app), D-043 (la confiance, le moteur, le
positionnement), D-044 (les collègues et leurs agents), D-045 (la signature en sept règles), D-046
(s'enrôler). Le plan en vingt-quatre étapes vit dans les feuilles de route de `kete-core` (A1, B1 à
B7) et de `kete-enterprise` (A2, C1 à C11, D).

## Ce qui reste incertain

- Aucun écran n'a été utilisé par quelqu'un : seul un vrai responsable, chez KYA, validera.
- Les objectifs comme façon d'organiser le travail : pas d'écran pour l'instant.
- La voix en continu, et un système qui parle le premier : à doser à l'usage.
- La refonte visuelle de Nettio n'est pas dans le plan (design existant gardé).
