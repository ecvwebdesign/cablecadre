---
title:  Comment choisir les media queries ?
summary: Les media queries permettent de définir des points de rupture dans sa feuille de style CSS.
date: 2020-02-06
author: Laurie
tags:
  - howto
  - responsive
  - css
  - résolution
image: howto_08.png
---

![schéma branche github](/static/img/howto_08.png)

Les media queries permettent de définir des points de rupture dans sa feuille de style CSS. Ainsi on peut définir différents affichages en fonction de la résolution de l'écran utilisé pour visualiser le site. Comment les utilise-t-on ?
## 1. Comprendre la syntaxe
On combine un type de média (screen, all…) et une expression, suivie de « and », qui va donner la résolution d'écran à laquelle va correspondre le contenu de la media querie.
L'expression peut contenir min-width ou max-width ou bien les deux pour exprimer une résolution comprise entre deux valeurs.
![schéma branche github](/static/img/howto_08-img01.png)
## 2. Choisir les résolutions « points de rupture »
La meilleure solution pour choisir les bons points de rupture est de faire des tests en réduisant la taille de son navigateur. Ainsi on peut observer les résolutions à partir desquelles la mise en page « se casse ».
Cependant il existe des résolutions « standard » que l'on peut utiliser, tout en gardant en tête que de nouvelles résolutions d'écran sont mises sur le marché.
![schéma branche github](/static/img/howto_08-img02.png)
## 3. Définir les fonctionnalités
Maintenant il est possible de spécifier les fonctionnalités qui vont changer en fonction de la taille de l'écran, voici quelques exemples :
![schéma branche github](/static/img/howto_08-img03.png)
