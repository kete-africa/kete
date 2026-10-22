# 2026-10-22 et 23 — L'objet au centre

Réflexion avec l'agent, après la livraison de D-061, jusqu'à la décision D-062. Ce qui suit la
décision est au statut **proposition** : le passage technique en profondeur le tranchera.

## D'où l'on partait

Les fils, Kete et les agents étaient livrés. En cherchant ce qu'on pourrait brancher sur un agent,
puis comment les tableaux de bord lisent les chiffres, l'agent a trouvé des îlots : des agents sans
les outils des apps, des tableaux sans projet, quatre systèmes de chiffres, trois chemins pour
connecter un outil.

## Ce que l'auteur a ajouté

- « Il y a plein d'aspects qui devraient être naturels depuis le début » : d'où des règles plutôt
  que des correctifs.
- Lire NocoBase et Copilot Studio en profondeur, et ne prendre que ce qui apporte de la valeur.
- Un tableau de bord est dynamique.
- Des composants génériques, configurés là où ils servent.
- Des agents disponibles pour tous, livrés avec le système.
- La conception peut changer la manière d'évaluer les gens.
- « On raisonne au dessus de KYA » : la première entreprise viendra après.

## Ce qui a été trouvé en chemin

- **Les règles R1 à R22** (D-062), puis leur poids : R1 et R2 d'abord.
- **Ce qui fait un bon agent** n'est pas d'abord le modèle : c'est le contexte, les outils et les
  savoir-faire de la maison.
- **La trajectoire** : aucune fonction ne sera une révolution à elle seule. Le serait une personne
  qui n'a plus à apprendre un logiciel : elle parle, et le travail se range, se suit et se termine.
  Le risque principal est la largeur : relier avant d'élargir.

## Propositions à trancher par le passage technique

1. **Un seul module de la Mesure.** Le référentiel des indicateurs (formule, source, fréquence,
   cible, seuil, poids), leurs sources (les apps, les connexions, les registres de Kete, la saisie
   avec preuve), la lecture vivante, le trimestre figé, le rouge qui crée une tenue, la donnée
   absente montrée comme rouge. La performance, les tableaux, `@kete/metrics` et `@kete/boards`
   en deviennent les faces.
2. **Des types d'objets déclarés**, avec leurs champs, leurs états, leurs liens nommés (« produit »,
   « couvre », « concerne »), leur fil et leurs axes hérités. Un projet est un type parmi d'autres :
   on ne l'étire pas. Un projet (une affaire, qui a une fin) produit des équipements durables, qui
   vivent leur propre vie (maintenance, interventions, supervision). Chaque fait pointe vers son
   objet ; les axes servent à regrouper.
3. **Les données d'une app restent chez elle.** Pour un type d'objet, l'app déclare ses chiffres,
   ses jeux de données, ses événements et ses outils de lecture ; on les lit à la demande, sans
   copier les séries ; on ne fige que ce qui doit l'être.
4. **Kete au-dessus d'un ERP existant**, sans le refaire : une connexion complète (lire, recevoir ses
   événements, agir en brouillon), et ses clients et affaires deviennent des tiers et des projets du
   centre (R13).
5. **Les composants**, dans cet ordre : la fiche d'objet ; la collection (table, liste, colonnes par
   état, calendrier, frise, carte, planning de ressources) ; le chiffre ; le tableau de bord ; le
   formulaire et son préréglage « registre » ; la frise. Ensuite : le document (versions, « lu et
   compris ») et le sélecteur d'objet.
6. **Les dispositions d'un tableau** : la grille, les onglets, les sections, la forme téléphone, le
   mode réunion, le mode récit, le côte à côte, le résumé figé, le tableau d'objet.
7. **Les graphiques.** Aujourd'hui : nombre, barres, courbe, camembert, tableau, note. D'abord :
   la puce, le tableau d'indicateurs, les barres et courbe combinées, le cumul face à la
   trajectoire, la cascade, la carte par région, le Pareto, le radar, la boîte à moustaches.
   Ensuite : barres groupées, empilées et d'écart, jauge, mini-courbe, aire, histogramme, nuage et
   bulles, entonnoir, calendrier et matrice en carte de chaleur, tableau croisé. Plus tard : la
   mosaïque, le Sankey, la carte de contrôle. Utiles seulement dans l'ordre : la source, puis le
   chiffre prouvé, puis l'affichage.
8. **L'ordre de construction** : la Mesure avec les axes et le contexte des tableaux ; les
   événements ; les outils, les modèles et le catalogue des agents ; la connexion unique ; la
   mémoire et les budgets ; les évaluations ; les avatars. Chaque étape part de sa maquette.

## Ce qui reste à prouver

Tout, encore : les règles se prouvent par l'audit des modules et par une journée réelle d'une
entreprise, de bout en bout.
