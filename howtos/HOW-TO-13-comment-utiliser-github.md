---
title: Comment et pourquoi? utiliser gitHub ?
summary: Nous sommes en 2020, pas moyen d'y couper, il faut savoir utiliser git, ou du moins comprendre son fonctionnement.
date: 2015-01-01
author: Arnaud
tags:
  - howto
  - outils
  - front-end
  - design methods
image: howto_13.png
---

![deux petits poulpes de Github qui touchent leurs tentacules](/static/img/howto_13.png)

Nous sommes en 2020 : pas moyen d'y couper, il faut savoir utiliser git, ou du moins comprendre son fonctionnement.
GitHub est une plateforme d'hébergement de code pour le contrôle de version et la collaboration. Il vous permet, ainsi qu'à d'autres, de travailler ensemble sur des projets depuis n'importe où. C'est un service conçu pour gérer tous les projets web, grands ou petits.
Voici comment réussir à dompter la bête, en quelques points:
## 1. Comprendre
Comprendre le fonctionnement de git est en toute logique le premier pas à faire lorsque vous voulez apprendre à l'utiliser.
L'un des principaux malentendus concernant GitHub vient du fait que c'est avant tout un outil de développement, faisant partie de la panoplie de tout programmeur, comme le sont les langages de programmation et les compilateurs. Cependant, GitHub en lui-même n'est rien de plus qu'un réseau social comme Facebook ou Flickr. Vous construisez un profil, vous y déposez des projets à partager et vous vous connectez avec d'autres utilisateurs en suivant leurs comptes. Même si la plupart des utilisateurs y déposent des projets de programmes ou de code, rien ne vous empêche d'y placer des textes ou tout type de fichier à présenter dans vos répertoires de projets.
## 2. Créer un repository
Un repository est généralement utilisé pour organiser un seul projet. Les repository peuvent contenir des dossiers et des fichiers, des images, des vidéos, des feuilles de calcul et des ensemble de données, en gros tout ce dont votre projet a besoin.
## 3. Créer une branche
La branche est la méthode qui permet de travailler simultanément sur différentes versions d'un référentiel.
Lorsque vous créez une branche à partir de la branche principale, vous effectuez une copie, ou un instantané de la branche principale tel qu'elle était à ce moment-là. Si quelqu'un d'autre a apporté des modifications à la branche principale pendant que vous travailliez sur votre branche, vous pouvez extraire ces mises à jour sans écraser votre travail.
Concrètement c'est similaire à créer un fichier « compo.ai » le dupliquer et renommer le second « compo2.ai ».
## 4. Les commits
Un commit n'est en réalité que la mise à jour que vous apportez au fichier principal depuis votre branche, vous écrasez le fichier principal avec le vôtre. Ce sont eux qui vont rythmer le projet.
Chaque commit a un message de validation associé, qui est une description expliquant pourquoi une modification particulière a été effectuée. Les messages de validation capturent l'historique de vos modifications, afin que les autres contributeurs puissent comprendre ce que vous avez fait et pourquoi.
Pour reprendre le même exemple, ces modifications seront apportées uniquement au fichier « compo2.ai » de votre branche, donc cette branche contient maintenant un contenu différent de « compo.ai ».
## 5. Le pull request
Les pull requests sont au cœur de la collaboration sur GitHub. Lorsque vous ouvrez une pull request, vous proposez vos modifications et demandez à quelqu'un d'examiner, d'extraire vos modifications et de les fusionner dans sa branche. Les pull requests affichent les différences du contenu des deux branches. Les modifications, ajouts et soustractions sont affichés en vert et en rouge.
## 6. Fusionnez vos pull requests au master
C'est bien sympa tout ça, mais le but reste de fusionner les modifications de l'équipe avec le fichier principal (dit « master »). Pour cela rien de plus simple il faut faire un « merge pull request » et donc fusionner votre travail avec le fichier principal.
Pour reprendre le même exemple, cela signifierait renommer le fichier « compo2.ai » de votre branche en  « compooi ».
## 7. Bière.
Pour tout créatif, c'est clairement la consécration de tout le projet. Si vous avez compris les points précédents et les mettez en application, alors maintenant détendez-vous et ouvrez une bière, vous le méritez.
## 7. Github desktop
Petit plus pouvant simplifier tout le processus, et votre vie : Github desktop. Il s'agit simplement d'un logiciel qui rassemble les 4 premiers points, après ça vous n'aurez plus qu'à finaliser en ligne. Croyez-moi sur parole, c'est un outil non-négligeable.
