# 2026-09-30 — Kete Enterprise : la chaîne d'une entreprise

Réflexion avec l'agent, du constat sur kya-platform jusqu'aux décisions D-025 à D-028.

## Le point de départ

- **kya-platform**, écrit pour KYA en septembre 2026 : un plan de contrôle très gouverné (Python,
  FastAPI, OpenFGA), environ 100 000 lignes en quatre semaines, mais presque aucun usage réel. Le
  catalogue gouverné ne contenait qu'une app témoin, un skill et un MCP. Ce n'est pas la
  technologie qui a manqué, ce sont des règles de coupe : celles que `kete-core` applique déjà
  (« ne construire que ce qui a fait mal », règle des trois heures).
- **Microsoft**, le 25 septembre 2026, présente le nouveau Copilot comme « un OS pour le travail » :
  Home, Code (des apps créées par des non-développeurs, hébergées et gouvernées), Autopilot (des
  agents persistants avec identité et droits), Microsoft IQ (le contexte de l'entreprise), un
  registre de plugins validés par l'IT, et le FinOps de l'IA. La thèse est la bonne ; les briques
  génériques deviennent gratuites ailleurs. La différence de Kete tient dans la chaîne propre à
  chaque entreprise, sur laquelle n'importe quelle IA se branche.
- **La discussion avec GPT** : bonnes intuitions (graphe organisationnel, portée, contrôles, Inbox,
  passerelle de modèles), mais chaque réponse élargissait le périmètre. Un agent à qui l'on demande
  plus de recul ajoute ; il faut une doctrine pour couper.

## Ce qui a été compris

**Ce qui coûte le plus dans une entreprise qui grandit n'est pas dans ses outils, mais entre eux** :

1. qui est qui, où, et qui peut quoi, sans recopier la structure dans chaque outil ;
2. les décisions qui traversent les outils (une dépense dépend de la finance et des absences) ;
3. l'IA qui multiplie les créations (skills, apps, MCP, agents) sans lieu gouverné ;
4. un agent qui ne doit voir que ce que voit la personne, partout ;
5. un savoir-faire qui doit appartenir à l'entreprise ;
6. une attention humaine dispersée entre dix outils.

`kete-enterprise` est ce qui existe entre les outils. Dans l'image du métier à tisser : `kete-core`
est le métier, `kete-enterprise` est la chaîne d'une entreprise, les apps, agents, skills et MCP
sont la trame, et les humains tissent.

## Le concept de soumission, gardé de kya-platform

Toute ressource (skill, app, MCP, agent) naît dans un espace personnel ou d'équipe. L'auteur n'est
pas le propriétaire. Être trouvable n'est pas être accessible. On soumet depuis Claude ou ChatGPT,
sans Git. La portée monte l'organigramme par paliers, chacun avec son approbateur. La revue est
proportionnée au risque : du texte pour un skill, de l'exécution et des données pour une app ou un
MCP. Un même moteur d'approbation sert la promotion d'un skill, une note de frais et un congé.

## Les cas d'exploitation

Entreprises avec Kete sur l'instance partagée (tenants), certaines avec des ressources clés sur
leurs serveurs, et entreprises à part comme KYA, avec leur propre instance. Jamais de fork : un seul
logiciel, des versions, de la configuration et des apps connectées.

## Restées en proposition, puis validées le jour même (D-029 à D-035)

- L'API de `kete-enterprise` comme service séparé (Hono sur Node LTS), les écrans en TanStack
  Start ; pas de Bun tant que tout l'écosystème ne migre pas ensemble.
- Une instance dédiée hébergée par Kete pour une grande entreprise, et une instance chez le client
  administrée à distance par Kete.
- Le relais sortant pour les ressources gardées chez le client.
- Le chat interne derrière un port de modèle compatible OpenAI (DeepSeek d'abord), le fournisseur
  choisi selon la sensibilité des données : l'API de DeepSeek traite les données en Chine.
- La première démonstration de KYA-Platform : structure réelle avec des personnes fictives, droits
  selon la portée, soumission et validation d'un skill, catalogue d'apps et de MCP, chat interne et
  Claude sur les mêmes capacités.
