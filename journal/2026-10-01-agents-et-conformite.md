# 2026-10-01 — Agents permanents et conformité

Réflexion avec l'agent, sur trois idées venues d'une discussion avec GPT, jusqu'aux décisions D-039
et D-040.

## Ce qui était proposé

- **Une plateforme gouvernée « à la Microsoft »** : toutes les apps, quel que soit l'outil qui les
  crée, passent par un même runtime qui applique l'identité, l'accès aux données, la surveillance
  et l'inventaire.
- **Les normes ISO intégrées au processus** : une longue liste de normes, un moteur de conformité,
  un agent qui vérifie chaque nuit.
- **Des agents permanents pour chaque employé** (à la manière d'OpenAI Dots), qui se délèguent des
  tâches entre eux, avec Temporal, OpenFGA ou OPA, et d'autres briques.

## Ce qui a été retenu

- La doctrine avait déjà l'essentiel : fiche de poste, échelle d'autonomie, principe 4, registre
  des ressources avec soumission et promotion (D-028), et « plus tard les contrôles ».
- **Gouverner par le contrat, pas par l'hébergement.** Microsoft peut imposer son runtime parce
  qu'il possède son nuage ; Kete tourne chez le client (D-029).
- **Un moteur de contrôles**, pas un module par norme : un contrôle sert plusieurs référentiels, les
  preuves viennent des journaux, les textes des normes ne sont jamais livrés.
- **Des agents qui dorment et se réveillent**, des délégations qui ne font que rétrécir, une chaîne
  qui remonte toujours à un humain, jamais un agent qui valide pour un autre, un budget de
  brouillons.

## Ce qui a été coupé

- **Temporal, OpenFGA, OPA, Keycloak** : pg-boss porte déjà les attentes durables (D-029) ; les
  droits avec portée sont ceux de `kete-enterprise` ; Keycloak est écarté (D-009). kya-platform a
  montré ce que coûte un plan de contrôle très outillé sans usage réel.
- **Une liste de seize normes** : un référentiel pilote d'abord, celui qui a une échéance chez KYA.
- **Un pourcentage de conformité** : un auditeur demande des preuves.

## Ce qui va dans `kete-core`

Deux petites choses, utiles à toutes les apps : la chaîne de délégation dans l'acteur des commandes
(`@kete/commands`), et la carte d'identité de l'app dans `manifest.v1` (responsable, catégories de
données, usage de l'IA, criticité). Tout le reste vit dans `kete-enterprise`.

## Non vérifié

Trois affirmations de la discussion n'ont pas été vérifiées : le nom « Copilot Managed Runtime »,
« OpenAI Dots », et la publication d'ISO 9001:2026. Les décisions n'en dépendent pas ; l'édition de
chaque norme se vérifie quand son référentiel est écrit (D-040).
