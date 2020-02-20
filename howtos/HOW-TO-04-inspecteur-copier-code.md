---
title:  Comment utiliser l'inspecteur pour copier du code ?
summary: L'inspecteur est une façon rapide de pouvoir faire des expériences avec le code, ou récupérer le code d'un site qui nous plait.
date: 2020-02-20
author: Gaëlle
tags:
  - howto
  - code
  - web design
  - entourloupe
image: howto_04.png
---

![image loupe pour observer du code](/static/img/howto_04.png)

L'inspecteur est une façon rapide de pouvoir faire des expériences avec le code, ou récupérer le code d'un site qui nous plait. Voici quelques astuces pour maîtriser l'outil :
## 1. Ouvrir l'inspecteur
Pour utiliser l'inspecteur, faites un clic droit dans une page internet et sélectionnez "inspecter l'élément". Cette action devrait ouvrir la fenêtre de l'inspecteur, vous pouvez maintenant accéder au code de la page. L'intérêt de cette fonction est que vous pouvez copier le code, mais aussi le modifier sans altérer la page de façon définitive.
Quelques élément à connaître dans le panneau l'inspecteur. En bas du panneau HTML, se trouve un fil d'Ariane.
Ce fil affiche la hiérarchie complète de l'élément sélectionné dans la page :
![image du code](/static/img/howto_04_img01.png)
Survoler un élément du fil mettra celui-ci en surbrillance dans la page.
## 2. La recherche
À partir de Firefox 45, la boîte de recherche de l'Inspecteur trouve les correspondances dans tout le markup du document ouvert, ainsi que dans toutes les frames.
Pour commencer une recherche, il suffit de cliquer sur la boîte de recherche pour l'agrandir ou bien d'utiliser les raccourcis clavier Ctrl + F , ou Cmd + F sous Mac. Lors de la saisie, une pop-up d'autocomplétion affiche toutes les classes ou ID qui correspondent à la recherche en cours :
![image du code](/static/img/howto_04_img02.png)
Pour itérer parmi les suggestions, il faut utiliser Flèche Haut et Flèche Bas. Tab permet de choisir la suggestion sélectionnée. Entrée permet alors de sélectionner le premier noeud correspondant.
Si la recherche est faite sans utiliser de valeur d'autocomplétion, alors la recherche sera effectuée sur tout le texte du document, incluant les balises, les attributs, et le contenu textuel des noeuds.
Pour parcourir les résultats, il faut utiliser Enter. Depuis Firefox 48, il est possible d'itérer à l'envers avec  Maj + Enter.
## 3. Arbre HTML
Le reste du panneau affiche le HTML de la page sous forme d'arbre (cette interface est également appelée Markup View). À la gauche de chaque nœud se trouve une flèche, cliquer sur celle-ci développera le nœud. Appuyer sur la touche "Alt" développera tous les nœuds inclus dans l'élément.
![image du code](/static/img/howto_04_img03.png)
Survoler un élément dans l'arbre mettra celui-ci en surbrillance dans la page.
Les nœuds qui ne sont pas visibles sont affichés en transparence dans l'arbre.
Depuis Firefox 53, une ellipse est affichée entre la balise ouvrante et fermante d'un élément réduit à cause d'un contenu trop long.
Avant Firefox 53, il était impossible de déterminer si noeud réduit avait des enfants. Maintenant, ce cas est indiqué par une icône de points de suspension.
## 4. Noeuds ne contenant que des espaces
Les développeurs web n'écrivent (généralement) pas tout leur code en une seule ligne. Ils utilisent des espaces, des retours à la ligne, ou des tabulations dans leur HTML pour le rendre plus lisible.en une seule ligne. Ils utilisent des espaces, des retours à la ligne, ou des tabulations dans leur HTML pour le rendre plus lisible.
Normalement, ces espaces n'ont aucun effet sur le visuel de la page. Mais en réalité, lorsqu'un navigateur analyse l'HTML, il génère automatiquement des noeuds de texte anonymes pour les éléments qui ne sont pas contenus dans des balises. Cela inclut les espaces (qui après tout, sont un type de texte).
Si ces noeuds autogénérés sont des éléments "en ligne", alors les navigateurs leur donneront une hauteur et largeur non nulle. Des espaces étranges entre les éléments apparaîtront alors, même si aucun margin ou padding n'est appliqué sur ces éléments.
Depuis Firefox 52, l'Inspecteur affiche ces noeuds d'espaces, afin de pouvoir savoir d'où viennent les espaces dans la mise en page. Ces noeuds sont représentés par un point, et affichent une infobulle explicative au survol :
![image du code](/static/img/howto_04_img04.png)
## 5. Shadow roots
Tous les noeuds shadow roots présents dans le DOM sont exposés par la page HTML, de la même manière que le DOM normal. Le shadow root est représenté par un noeud nommé #shadow-root — il est possible de cliquer sur la flèche d'expansion pour voir le contenu complet du shadow DOM, et le manipuler, exactement comme avec les noeuds DOM normaux. Il existe cependant des limites, il n'est par exemple pas possible de glisser/déposer ou de supprimer des noeuds shadow DOM.
![image du code](/static/img/howto_04_img05.png)
Si un shadow DOM contient un élément avec attribut slot ayant été inspiré dans un élément <slot>. Cet élément sera affiché à l'intérieur de son élément <slot> correspondant, avec un lien à côté. Cliquer sur ce lien affichera l'élément avec l'attribut slot tel qu'il existe en dehors du shadow DOM.
Cette fonctionnalité est utile pour trouver la source du contenu d'un élément <slot>.
![image du code](/static/img/howto_04_img06.png)
## 6. Menu contextuel
Il est possible d'effectuer des tâches courantes sur un élément spécifique grâce au menu contextuel. Pour ouvrir celui-ci, il suffit de faire un clic droit sur l'élément :
![image du code](/static/img/howto_04_img07.png)
Pour plus de détails, voir les références du menu contextuel.
## 7. Éditer le code HTML
Il est possible d'éditer les éléments HTML directement dans le panneau HTML. Il suffit de double cliquer sur le texte voulu, de le modifier puis d'appuyer sur Entrée. Les modifications sont immédiatement effectives.Pour éditer le outerHTML, il faut ouvrir le menu contextuel et sélectionner "Modifier comme HTML" . Une boîte apparaîtra alors dans le panneau HTML :
![image du code](/static/img/howto_04_img08.png)
N'importe quel fragment HTML peut être ajouté ici. Il est par exemple possible de changer les balises de l'élément, d'ajouter de nouvelles balises, de modifier des éléments existants, etc. Les modifications sont effectives dès que vous cliquez en-dehors de la boîte
le menu contextuel est le même que pour le texte modifiable normal :
-Il est possible d'utiliser le menu popup (clic droit) )pour copier des noeuds dans l'arbre HTML.
-Il est possible de modifier l'HTML en déplaçant les noeuds dans l'arbre HTML. Il suffit de rester cliqué sur un élément et de le glisser vers le haut ou vers le bas. Lorsque le clic est relâché, l'élément sera inséré à la position voulue.
-Cliquer sur cette icône insère une balise <div> dans le document en tant que dernier enfant de l'élément sélectionné. Il est alors possible de modifier le contenu et le style du noeud, exactement comme n'importe quel autre élément.
Voilà, vous avez maintenant des bases pour pouvoir expérimenter avec le code et l'inspecteur.
