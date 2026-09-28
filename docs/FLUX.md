# Le flux de travail

> Comment une idée devient du code en production, dans tous les dépôts Kete. Git, Neon, Coolify,
> Spec Kit et Pono avancent ensemble, étape par étape.

## 1. Les branches et leurs environnements

| Branche Git | Rôle | Branche Neon | Déploiement Coolify | Qui y entre |
|---|---|---|---|---|
| `main` | La production | `main` | Production | **Le geste humain seul**, par pull request depuis `dev`, après les garde-fous de Pono |
| `dev` | L'intégration | `dev` | Préproduction (staging) | Les features, par pull request, **CI verte obligatoire** |
| `NNN-slug` | Une feature Spec Kit | `preview/pr-N`, créée depuis `dev` | Préversion de la pull request | L'agent et l'auteur |

- Une branche de feature part **toujours de `dev`** et y revient par pull request.
- `dev` → `main` se fait **uniquement quand l'auteur le demande**.
- Jamais de push direct sur `main` ni sur `dev`.
- Tant que l'organisation est sur l'offre GitHub gratuite, ces règles tiennent par discipline et par
  Pono ; **passer à GitHub Team** dès qu'un dépôt privé est en production, pour les rendre mécaniques.

## 2. Le cycle d'une feature, avec Spec Kit

```
constitution → specify → clarify → plan → tasks → analyze → implement → converge
```

1. `specify` crée la branche `NNN-slug` et le dossier `specs/NNN-slug/`.
2. `clarify` pose les questions ouvertes ; les réponses de l'auteur sont écrites dans la spec.
3. `plan`, `tasks`, `analyze` : le plan, les tâches ordonnées, la cohérence vérifiée.
4. `implement` : le code, tâche par tâche, avec la doc et les schémas dans la même pull request.
5. `converge` : si le code a dérivé de la spec, les tâches manquantes sont ajoutées.
6. La feature n'est **finie** que lorsque sa preuve est obtenue (écrite dans la spec).

## 3. Les bases de données (Neon)

- **Un projet Neon par service** (Compte Kete, Kete Cockpit, chaque app), région Francfort.
- **Branches** : `main` (production), `dev` (préproduction), `preview/pr-N` (une par pull request,
  créée depuis `dev`, supprimée à la fusion), `test` (la CI, remise à zéro à chaque passage).
- **Migrations** : générées par Drizzle, versionnées, appliquées **automatiquement** sur la branche
  de la préversion, puis sur `dev`, puis sur `main` au déploiement. Jamais à la main en production.
- **Migrations additives** : une suppression ou un renommage passe en deux temps et doit être déclaré
  (garde-fou Pono).
- **Chaque table naît avec sa politique RLS.** Deux rôles : un propriétaire pour les migrations, un
  applicatif sans contournement de RLS.
- **Données** : des données d'exemple synthétiques pour les préversions ; jamais de données
  personnelles de production copiées telles quelles.

## 4. La CI, à chaque pull request

1. Lint, vérification des types, formatage.
2. Contrôle des frontières entre features.
3. Tests : domaine, commandes, **isolation RLS entre deux organisations** (sur la branche Neon
   `test`), contrats, bout en bout, évaluations des capacités de l'agent.
4. Documentation : chaque feature a son `README.md` ; les documents générés correspondent au code.
5. Construction de l'image ; préversion déployée avec sa branche Neon.

Une pull request n'est fusionnée dans `dev` que si **toute** la CI est verte.

## 5. La mise en production

1. Pull request `dev` → `main`, ouverte à la demande de l'auteur.
2. Garde-fous de Pono : aucun secret, préversion vérifiée, migrations additives.
3. Validation humaine dans Pono.
4. Fusion par l'auteur ; Coolify déploie ; les migrations s'appliquent sur la branche Neon `main`.
5. Un tag de version sémantique (`v1.4.0`) marque chaque mise en production.
6. En cas de problème : retour arrière depuis Pono.

## 6. Les conventions

- **Code en anglais**, documentation en français, écrans en français (et en anglais par les
  traductions).
- **Messages de commit** en anglais, à l'impératif, courts ; le corps explique le pourquoi.
- **Secrets** : jamais dans le dépôt ; `.env.example` documente chaque variable ; les valeurs vivent
  dans Coolify, puis Infisical.
- **Chaque dépôt** a son `CLAUDE.md`, qui renvoie à la doctrine du dépôt `kete`.
