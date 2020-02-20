---
title:  Comment bien hiérarchiser mon code HTML/CSS?
summary: Rédiger du code HTML/CSS est simple, on peut même apprendre tout seul, et trouver des tas de tutoriels.
date: 2020-02-20
author: Wenyan
tags:
  - howto
  - planning
  - css
  - html
image: howto_14.png
---
![schéma branche github](/static/img/howto_14.png)

Rédiger du code HTML/CSS est simple, on peut même apprendre tout seul, et trouver des tas de tutoriels. Mais hiérarchiser du code HTML/CSS n'est pas aussi simple que ça en a l'air, surtout en travaillant sur un projet de longue durée, avec plusieurs développeurs de spécialités et de capacités différentes. Nous devons bien hiérarchiser et optimiser le code HTML afin d'éviter des problèmes inutiles.
-Maintenir une certaine harmonie de rédaction,
-Maintenir une feuille de style CSS claire et extensible,
-Garder le code transparent, hiérarchisé et lisible.
## 1. Utiliser BEM (Bloc-Element-Modifier)
BEM signifie Block - Element - Modifier. Trois entités qui vont permettre de découper et organiser tous les composants d'une page web. Une page peut contenir plusieurs blocs, chacun de ces blocs peuvent contenir un ou plusieurs éléments qui lui sont propres. Enfin chacun de ces éléments peut avoir un état qui est modifié selon un événement ou action de l'utilisateur, c'est le modifier.
Par exemple, une page web est composée de 4 blocs :
-Navigation
-Main Content
-Side Bar
-Footer
La side bar est composée de différents éléments :
-Titre
-Liste des derniers articles
-Liste des derniers commentaires
## 2. Diviser le fichier CSS par différentes fonctionnalités
Il est intéressant de diviser les code CSS en plusieurs fichiers chacun correspondant à un module, une fonctionnalité ou une page de votre interface. Cela nous permet de le retrouver facilement pour modifier et développer, surtout pour un grand projet de développement.
Par exemple, on peut découper par la feuille style de la typo, le footer, le header.
typo.css
footer.css
header.css
L'intérêt de découper le CSS en fichiers multiples et décupler surtout si vous utilisez un préprocesseur CSS (Sass ou Less).
## 3. Mise en hiérarchisation de balises H1, H2…
Pour éviter la problème d'optimisation de site et visibilité de site, on doit bien hiérarchiser le balises H1, H2, H3… Cela veut dire organiser les choses de manière à ce que chaque élément soit subordonné à un autre.
Par exemple:
H1 très très important
H2 très important
H3 important
…
Ces niveaux de titres servent à construire une page de manière hiérarchique et aussi à informer les moteurs de recherche des titres et sous-titres ainsi que de l'organisation générale de la page.
Google saura quel est le titre principal de la page (H1). Il peut ainsi définir le sujet principal de la page et savoir quelle est la thématique générale de cette page. Les mots présents dans la balise h1 définissent pour Google le sujet de la page. Il donne un poids fort à ces mots dans son algorithme de pertinence. Si on a un H1 correct, cela nous permet d'amener la visibilité de notre site.
## 4. DRY, don't repeat yourself
DRY est un des principes de base en informatique. Il s'agit d'un principe qui vise à réduire la quantité de code écrit et de regrouper les déclarations en doublon. Le principe DRY peut-être très utile lorsque l'on code en Less ou Sass.
Exemple:
.text-erreur{
     font-size: 15px;
     background-color: #ccc;
     color: red;
     border-color: red;
}
.text-optimisation{
     font-size: 15px;
     background-color: red;
}
On a gagné en lisibilité et refactorisé notre code pour éviter des répétitions.
En conclusion, pour mieux travailler dans un environnement de développement, c'est intéressant de hiérarchiser le code HTML/CSS. Cela permet de nous bien organiser le travail.
