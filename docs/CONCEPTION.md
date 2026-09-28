# Conception

> Comment on conçoit une app Kete à l'ère de l'IA. Ces règles s'appliquent à toutes les apps.
> Les rendre mécaniques (lint, génération, tests) plutôt que conseillées.

## A. Les données

1. **Un schéma unique par enregistrement.** Un dépôt, un devis, un congé est décrit une seule fois
   (Zod). En découlent : le formulaire, la validation serveur, l'entrée de l'outil MCP, l'API, les
   brouillons. Chaque champ porte ses métadonnées : libellé traduit, donnée personnelle, obligatoire,
   « à vérifier par un humain » quand l'agent le remplit.
2. **Un cycle de vie pour tout enregistrement qui engage** : brouillon → à vérifier → validé →
   (annulé | archivé). Deux sortes de brouillons :
   - le **brouillon d'enregistrement** (un devis pas encore validé) : un état de l'enregistrement ;
   - la **proposition de modification** (l'agent veut changer un prix) : un changement en attente,
     montré en avant / après, sans effet tant qu'il n'est pas validé.
   Un brouillon n'a aucun effet (calculs, notifications, statistiques) avant validation.
3. **La provenance de chaque champ** : saisie, système, message, photo, déduite par l'agent ; qui
   l'a mise ; avec quelle certitude.
4. **Des paramètres en couches** : Kete (Mon espace Kete) → organisation → app → agence →
   utilisateur. La valeur la plus proche l'emporte. Ce qui est générique se saisit une fois.
5. **L'argent, le temps, les numéros** : montants en entiers avec leur devise (le franc CFA n'a pas
   de centimes) ; dates en temps universel, affichées dans le fuseau de l'organisation ; factures et
   reçus numérotés sans trou.
6. **On n'efface pas, on archive.** Les données personnelles sont anonymisées pour le RGPD.

## B. Les gestes

7. **Des commandes nommées, jamais de modification générique** : `create-deposit`, `mark-ready`,
   `cancel-deposit`. Chaque commande porte une clé d'idempotence, l'acteur (personne, agent, canal),
   et déclare si elle est réversible, avec sa commande inverse. Ce qui fixe le niveau d'autonomie
   de l'agent : réversible → il agit, avec notification et « Annuler » ; irréversible → brouillon et
   confirmation humaine.
8. **Les features se parlent par leur porte d'entrée (`index.ts`) ou par événements.** Jamais
   d'import de l'intérieur d'une autre feature ; un outil le bloque en CI.
9. **Le hors ligne, ce sont des commandes en attente** dans une file locale, rejouées au retour du
   réseau ; le serveur tranche, avec une règle de conflit écrite par commande.

## C. L'humain et l'IA

10. **L'acteur est toujours explicite** : qui, au nom de qui, par quel canal.
11. **Tout est lisible par une IA** : identifiants préfixés et stables (`dep_`, `cli_`, `inv_`), un
    résumé court en français pour chaque enregistrement, des codes d'erreur stables qui disent quoi
    corriger.
12. **Les composants de la doctrine sont fournis d'office** : carte de vérification, états de
    l'agent, confirmation pour l'irréversible, notification avec « Annuler », page vide.
13. **Des choix volontairement différés** : pas de référentiel partagé entre apps (les clients d'un
    pressing restent dans chaque app) tant que le besoin n'est pas prouvé.

## D. Les écrans (D-015)

- Chaque écran est **conçu pour son métier**, jamais généré.
- Mobile d'abord, zones tactiles d'au moins 44 px, design system v1 rectangle (`@kete/design`).
- Chaque écran a ses états : chargement, vide, erreur, restreint, disponible.

## E. La documentation, au fil de l'eau

La documentation vit **dans le dépôt, à côté du code**, et se met à jour **dans la même pull request
que le code**. Les schémas sont écrits en **Mermaid** dans le Markdown : GitHub les affiche, et un
agent peut les modifier comme du texte.

| Où | Contenu | Schéma |
|---|---|---|
| `docs/ARCHITECTURE.md` de chaque dépôt | La vue d'ensemble de l'app | Conteneurs et flux principaux |
| `docs/decisions/` | Une décision par fichier (`0001-titre.md`) | — |
| `docs/flows/` | Les parcours importants : paiement, brouillon validé, hors ligne | Diagrammes de séquence |
| `src/features/<feature>/README.md` | Rôle, commandes, événements, capacités et autonomie | Cycle de vie (diagramme d'états) |
| `docs/generated/` | Base de données, capacités, événements, API | **Générés depuis le code** : ne pas éditer à la main |

Règles :
- Une feature sans `README.md` ne passe pas la CI.
- Les documents de `docs/generated/` sont regénérés en CI ; s'ils diffèrent de ceux du dépôt, la CI
  échoue.
- Un changement de comportement sans mise à jour de la doc et du schéma concernés n'est pas « fini ».
