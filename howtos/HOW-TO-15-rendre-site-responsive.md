---
title:  Comment rendre un site responsive ?
summary: Si vous débarquez dans le monde du web design il faut savoir que la base des bases c'est d'avoir un site responsive.
date: 2020-01-30
author: Agathe
tags:
  - howto
  - site
  - web design
  - responsive
image: howto_15.png
---

![cockpit de vaisseau spatial qui se réduit](/static/img/howto_15.png)

Comment rendre un site responsive?
Si vous débarquez dans le monde du web design il faut savoir que la base des bases c'est d'avoir un site responsive.
C'est à dire un site qui s'adapte parfaitement sur n'importe quelle taille d'écran. À l'heure du numérique il est indispensable de rendre son site lisible sur tous les supports, que ce soit tablettes, smartphones ou ordinateurs.
On pourrait croire que le responsive design est difficile à réaliser mais en fait il y a des moyens plutôt simples pour y parvenir, vous savez ce que c'est une « div » ? Très bien, vous avez le niveau suffisant ! Commençons donc le cours…
## 1. Les media queries
Les Media Queries sont des spécifications de CSS3 qui permettent d'attribuer des propriétés CSS en fonction de conditions particulières (exemple : largeur de l'écran). Ces spécifications sont particulièrement connues pour leurs utilités dans la conception d'un responsive web design.
Pour utiliser cet outil il vous suffit de vous rendre dans votre CSS et d'ajouter une ligne de code, appelée « media query », pour commencer la série des instructions pour le format mobile.
![image du code](/static/img/howto_15-img01.jpeg)
Pour l'instant, cette ligne de code signifie que si l'écran utilisé par le visiteur est inférieur à 480 px (en gros si il utilise un smartphone), il va se passer telle ou telle chose. Nous allons ensuite voir quel type d'instruction mettre à l'intérieur de cette balise.
Dans le cas ou le visiteur utilise une tablette, il faut rajouter des instructions car pour le moment le site n'est pas adapté aux tablettes. On va donc rajouter deux types de taille d'écran :
![image du code](/static/img/howto_15-img02.jpeg)
Avec ces lignes de codes votre site sera adaptable à toutes les tailles écrans !
Maintenant on va s'intéresser à ce qu'on peut mettre comme instructions dans les balises. Bien sur, les commandes vont varier selon le nom que vous avez donné à vos divs, leur nombre, etc.
Il suffit de comprendre trois principes fondamentaux, et vous pourrez facilement les appliquer au cas particulier de votre site :

![image du code](/static/img/howto_15-img03.jpeg)

## 2. Les miracles du « float :none »
Il est fortement probable que votre site articule des divs (ex : une qui va contenir une image et l'autre qui va contenir un texte, à droite de l'image), en utilisant le classique « float :left » ou « float :right ».
Sur mobile, oubliez ça ! L'écran est trop petit pour aligner horizontalement des blocs, l'un à gauche, l'autre à droite. En général, donc, les divers éléments sont placés les uns en dessous des autres, et non plus à côté. Par exemple, le logo ne sera plus à gauche du menu, mais au-dessus.
Votre principal allié sera donc le « float :none ».
Supposons donc que vous ayez deux divs, l'une contenant le logo, et l'autre contenant le menu, à droite de celle-ci.
Et que votre code ressemble à ceci :

![image du code](/static/img/howto_15-img04.jpeg)

Avec en css :

![image du code](/static/img/howto_15-img05.jpeg)

Vous n'avez plus qu'à lire votre code source, repérer chaque div, et pour celles qui en ont besoin, les faire passer en « float :none »
Naturellement, vous devez ajuster le padding et le margin de ces divs, puisque leur place est modifiée. Sur ce point précis, attention aux éventuelles divs dont vous avez fixé la margin non pas dans le css, mais dans le code html lui-même
(ex : <div id= « logo » style= margin-left :600px ;»). En effet, sur mobile, cela va dépasser la taille de l'écran. Du coup cette div n'apparaîtra pas.
Il faut prendre l'habitude de préférer les classes css.
(ex : <div id = « logo » class= « logo »>. Vous pourrez dans la css fixer la margin "classique" (pour les ordinateurs portables), puis la margin pour les mobiles de cette classe "logo".

![image du code](/static/img/howto_15-img06.jpeg)

## 3. Changer la width
Le dernier point à connaître pour obtenir un beau site responsive design consiste à remplacer la largeur de vos divs, souvent fixées en pixels, par :
* la commande width : auto; (qui ajuste automatiquement la largeur de la div à la largeur du petit écran du mobile). C'est très utile, en général, je mets 80% des divs en auto.
* pour les divs qui ne doivent qu'occuper une petite largeur de l'écran : fixer la largeur en pixel, mais de manière à ce qu'elle soit plus petite, pour s'adapter à la taille de l'écran du téléphone portable.
* ou mieux : fixer la largeur en pourcentage : de cette manière, la div s'agrandira au fur et à mesure que l'écran s'agrandit !
Là encore, cela s'opère dans la media query appropriée, correspondante au mobile.
## 4. Utiliser le « display:none »
Un site pour mobile est la plupart du temps plus simple, plus épuré, que sa version desktop.
La raison en est simple : quand on a un petit écran, on n'a pas la place de mettre la même quantité d'information, même si celle-ci est bien agencée par une intégration réussie.
Il faut s'y résoudre : il y aura certainement quelques divs, quelques images, quelques blocs, qui vont disparaître sur la version pour smartphone.
Pour cela, rien de plus simple : repérez la div ou l'image que vous souhaitez supprimer, et donnez lui une classe, si ce n'est pas déjà fait.
Puis, dans la css, donnez lui l'attribut « display:none ». Par exemple, pour ne pas afficher une div nommée « bloc1 » :

![image du code](/static/img/howto_15-img07.jpeg)

A vous de voir ce que vous souhaitez conserver sur la version mobile. Pour moi, j'ai tendance à en conserver le plus possible, mais je sacrifie toujours au moins deux ou trois éléments sur un site.
## 5. Conclusion
Voici un petit exemple de ce à quoi devrait ressembler votre feuille css

![image du code](/static/img/howto_15-img08.jpeg)

Voilà, c'est plus ou moins tout ce qu'il y a à savoir concernant spécifiquement l'intégration sur mobile.
Pour vérifier votre travail, vous pouvez certes utiliser un outil en ligne comme celui-ci, mais pourquoi se compliquer ? Mieux vaut cliquer sur la case de « réduction » de votre navigateur (la case juste à côté de la croix "fermeture" de votre navigateur). Vous pouvez alors ajuster la taille de l'écran, en l'agrandissant ou en la réduisant à volonté, avec votre souris. Vous obtenez alors l'équivalent de ce que vous pouvez voir de votre site sur mobile et sur tablette. Profitez-en !
