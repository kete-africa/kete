# Kete — contexte

> Le dépôt de la maison : **pourquoi** Kete existe et **où** elle va. Le *comment* vit dans les
> dépôts des produits. Des pointeurs, pas du savoir dupliqué.

## Ordre de lecture, avant toute action

1. `docs/FONDEMENT.md` — ce que l'auteur a reçu. Il prime sur tout le reste.
2. `docs/VISION.md` — ce que Kete voit et vers quoi elle marche.
3. `docs/MANDAT.md` — pour qui, quel bien, à quel prix moral.
4. `docs/PRINCIPES.md` — les invariants. Une décision qui les contredit est refusée.
5. `docs/DECISIONS.md` — ce qui est tranché. **Ne pas retrancher ce qui l'est.**
6. `docs/VERITE_ET_PREUVES.md` — avant toute affirmation publique.

Ensuite, selon le sujet : `POSITIONNEMENT.md`, `OFFRES.md`, `MARQUE.md`, `ARCHITECTURE.md`,
`FEUILLE_DE_ROUTE.md`, et le `journal/` pour le chemin de la réflexion.

## Kete, en une phrase

Kete tisse des organisations où l'humain décide et où l'IA travaille, du comptoir au siège.
Signature : **« Outils de demain pour une meilleure productivité »**.

## Règles pour tout agent qui travaille ici

- **Ne jamais inventer de contenu spirituel.** Le fondement vient de l'auteur ; l'agent reformule,
  signale ce qui est flou, et ne rédige rien comme reçu qui ne l'a pas été.
- **Ne jamais présenter une proposition comme une décision.** Une proposition porte le statut
  `proposition` jusqu'à validation écrite de l'auteur dans `DECISIONS.md`.
- **Aucun chiffre ni témoignage inventé**, ici comme sur le site (`VERITE_ET_PREUVES.md`).
- **Aucun secret** dans ce dépôt : ni clé, ni mot de passe, ni donnée de client.
- Une réflexion nouvelle va dans `journal/` (un fichier daté par sujet). Quand elle aboutit, elle
  devient une entrée de `DECISIONS.md`, et le document concerné est mis à jour.

## Les dépôts de Kete

| Dépôt | Rôle |
|---|---|
| `kete-africa/kete` | Ce dépôt : la doctrine |
| `kete-core` | L'atelier : contrats, SDK et briques `@kete/*`, Compte Kete, Mon espace Kete, modèle d'app (D-028, D-030) |
| `kete-cockpit` | Kete Cockpit et sa flotte ; vit dans `kete-core` jusqu'à sa sortie (D-022, D-027, D-033) |
| `kete-enterprise` | Kete Enterprise, la chaîne d'une entreprise (D-025, D-028) |
| `firmo`, `nettio`, `nyatefe` | Les apps du quotidien |
| `pono` | Le chemin sûr des changements de code, produit « par Kete » |

Chaque dépôt produit renvoie ici pour la doctrine, dans son propre `CLAUDE.md`.
