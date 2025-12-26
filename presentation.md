---
toplevel-attributes: slip enter=~duration:0 center="~duration:0 start"
---

{#start }
# Planning: de nouveaux outils

{pause up="start"}

## Le planning c'est long et difficile

40 tâches pour deux bénévoles et 35 bénévoles = plus de $10^{29}$ combinaisons possibles

{pause}
- Beaucoup sont évidemment mauvaises:
  - Un bénévole ne peux pas faire deux tâches en même temps.
  - Tout le monde ne peut pas faire toutes les tâches.
  - Il faut préserver du temps pour les repas.
  - etc.
{pause}
- Et toutes les solutions correctes ne se valent pas:
  - Respect des préférences individuelles d'horaire et de type de tâche.
  - Équilibre des temps de travail.
  - Permettre tout le monde d'assister à un maximum de spectacles.
  - etc.

{.block pause center}
Il est facile de trouver une solution... Mais très difficile de trouver la meilleure, tout du moins dans une temps raisonnable.

{pause}
 🐵 Les humains sont plutôt doués pour cette tâche, et l'intuition permet d'arriver à des solutions convenables. Mais c'est très chronophage et rarement optimal.

{pause}
🤖 Les problèmes de planning sont aussi très adaptés aux solutions automatiques: il est possible de les traduire en formules logiques pour lesquelles il existe de nombreux solveurs.

{pause up="~margin:45"}
## Deux outils en cours de développement par des membres de l'AFJ

- Un outil polyvalent de gestion des conventions: **Juggling Convention par Pierre**
- Un outil spécialisé dans la génération de planning: **Toubénev par Ulysse et Émile**

{pause up="~margin:45"}
### Juggling Convention [https://juggling-convention.com](https://juggling-convention.com)
Un site internet offrant une interface combinée pour gérer de nombreux aspect d'une convention, en amont et pendant l'évènement:

![](jc_admin.png){width=100%}

{#this pause up="~margin:45"}
Et une chouette interface pour faire la promo et donner les infos:

![](jc_promo.png){width=100%}

{#this pause up="~margin:45"}
Juggling Convention propose également un outil de génération automatique de planning:

![](jc_planning.png){width=100%}

{pause} Un très bon moyen de faire un premier jet !

{pause}
Mais l'algorithme glouton
utilisé par Juggling Convention ne permet pas d'atteindre une solution optimale.


{pause up="~margin:45"}
### Toubénev

- Un projet initié au sein des Bras Croisés pour Aurillac 2024: 90 bénévoles, 420 créneaux à remplir, de quoi donner la migraine 🤯

{pause}
- L'idée: traduire les contraintes sous forme de formules logiques et utiliser un solveur-optimiseur existant. Ces outils, tels que Z3 ou CP-Sat sont très performants pour trouver des solutions à des problèmes compliqués.

{pause center}
- Exemples de contraintes et préférences prises en charge:
  - Disponibilités des bénévoles
  - Préférences horaires des bénévoles
  - Quêtes préférées
  - Quêtes réservées
  - Bénévoles pré-assignés
  - Tâches obligatoires au moins une fois: le nettoyage par exemple
  - Quêtes suivies
  - Pas deux fois le même spectacle
  - Bénévoles amis / ennemis
  - Pause quotidienne d'une certaine durée
  - Maximisation de la diversité des tâches pour chaque bénévole
  - Minimisation des écarts de temps de travail quotidiens et sur la semaine
  - Minimisation de l'amplitude horaire quotidienne
  - Etc.

{pause center .block}
L'outil va proposer des solutions respectant toutes les contraintes jusqu'à en trouver une qui soit optimale, ou s'arrêter au bout d'un temps donné.

{pause}
Au contraire de Juggling Convention, il n'y a pas encore d'interface aboutie pour utiliser cet outil. Ulysse et Emile accompagnent les conventions qui souhaitent l'utiliser au cas par cas.

{pause center .block}
N'hésitez pas à en faire la demande, c'est en expérimentant sur un maximum d'évènements que l'on pourra aboutir à l'outil le plus utile possible !

