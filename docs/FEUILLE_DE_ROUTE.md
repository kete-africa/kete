# Feuille de route

> Des étapes ordonnées par dépendances et par preuves, jamais par dates. Une étape se ferme sur sa
> preuve, pas sur une impression.

## Règles

1. **Kete Apps et Kete Consulting rapportent d'abord.** Kete Enterprise avance en parallèle depuis
   le 2026-09-30, avec KYA comme premier client autonome (D-025) ; son offre ne se vend qu'après la
   preuve de l'étape 4.
2. **Un métier à la fois** dans Kete Apps.
3. **La doctrine avant le code** : chaque produit renvoie à ce dépôt.
4. **On ne construit que ce qui a déjà fait mal.** Mais ce qui est manifestement commun se
   construit dès la première fois comme un module autonome, réutilisable partout (D-059).
5. **Chaque app livrée a sa démo publique et Kete Intelligence** (D-059) ; les tarifs viennent
   quand tout est implémenté.

## Étape 0 — La maison posée

- [x] Organisation GitHub `kete-africa`, dépôt `kete`, logo importé.
- [ ] Nom sécurisé : kete.software (D-059), dépôt OAPI, comptes sur les réseaux.
- [ ] Société : Vitatech → Kete (dénomination au RCCM ou nouvelle société), avec un comptable.
- [ ] Vision, mandat et horizons complétés par l'auteur (`FONDEMENT.md`, `VISION.md`, `MANDAT.md`).
- [x] Style visuel tranché : v1 rectangle (D-010) ; reste `@kete/design`.

**Preuve** : un client peut signer un contrat avec Kete, et chaque affirmation du site a sa ligne
dans le registre de vérité.

## Étape 1 — Kete Cockpit V0

- [ ] Contrats v1 : manifeste, événement, santé.
- [ ] SDK TypeScript et Python (outbox, envoi, signature, santé, manifeste).
- [ ] Registre, réception des événements, sondes, instantanés, brief Telegram, MCP en lecture.
- [ ] Une app réelle branchée (Nettio ou Firmo).

**Preuve** : un événement parti de l'app en production apparaît dans le brief du lendemain ; une
panne simulée déclenche une alerte ; l'agent répond sur l'état des apps.

## Étape 2 — Un métier gagné dans Kete Apps

- [ ] Choisir le métier (Nettio ou Firmo) et le tarif au rythme de la recette.
- [ ] Compte Kete (Better Auth, e-mail) et paiement par Chariow, via Mon espace Kete.
- [ ] La carte de vérification et les brouillons préparés par l'agent.

**Preuve** : des clients payants l'utilisent encore après 90 jours.

## Étape 3 — Kete Consulting

- [ ] L'offre Kete Diagnostic, son livrable type et son prix.
- [ ] Un premier diagnostic réel.

**Preuve** : un diagnostic livré, compris sans explication, et une décision prise grâce à lui.

## Étape 4 — Kete Enterprise · _commencée le 2026-09-30 (D-025)_

- [ ] Propriété de KYA-Platform clarifiée par écrit, avant la mise en production chez KYA.
- [ ] Dépôt `kete-africa/kete-enterprise` : la chaîne d'une entreprise (D-028), avec sa propre
      feuille de route par phases (D-021).
- [ ] KYA-Platform : une instance autonome sur les serveurs de KYA, sa configuration et ses apps
      dans les dépôts de KYA, jamais un fork (D-025).
- [ ] L'instance partagée et ses tenants, administrés par la flotte du Cockpit (D-026, D-027).
- [ ] Catalogue de capacités et d'outils open source validés.
- [ ] **L'unification (D-056 à D-058)**, dans cet ordre : décider ; une simulation complète du
      flux, validée par l'auteur ; les tenues et le relais ; le moteur de politiques ; les fils et
      les canaux ; les écrans d'après une maquette v5 validée ; les références (lieux, actifs,
      catalogue, groupe) et le savoir ; les quatre apps sur le modèle unifié ; le parcours complet
      dans la démo ; les vrais comptes branchés. L'auteur puis KYA testent à la fin.

**Preuve** : des gains mesurés chez le pilote, publiés avec leur preuve.

## Plus tard

Agent WhatsApp et guichet Kete pour les commerçants · voix et langues locales · couche parc sur
toutes les instances · rapports mensuels clients · Kete Cockpit ouvert aux autres porteurs de
produits.
