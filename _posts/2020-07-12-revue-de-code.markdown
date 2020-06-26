---
layout: post
title: "Revue de code"
categories: [Méthodologie, Développement-Web]
published: true
image: "2020/07/code-review.jpg"
excerpt: "La revue de code est un indispensable des projets informatiques, quels sont réellement ses pouvoirs qui sont parfois sous estimées concernant la réussite projet"
---

Dans l’informatique, dans les projets en équipe, il y a un processus devenu quasi indispensable, c’est celui de la **revue de code** (**code review** en anglais). 

Cette dernière consiste en une simple relecture d’un morceau de code avant sa “fusion” au  code source global d’une application.

Cette procédure est utilisée dans tout type de projet, en partant des projets open source, en passant par ceux d’entreprises classiques, jusqu’aux projets plus ambitieux, de petits noms comme Google …

Décortiquons un peu ce qu’est et ce qu’apporte cette dernière. 

## Un avantage technique 

La revue de code est en premier lieu un outil de surveillance technique. 

Cette relecture vise à détecter (entres autres) le non-respect des **bonnes pratiques**, les erreurs de programmation, l'omission de “code mort”, etc.

Cette validation par un tiers apporte une vision extérieur sur le travail accompli.

{% include image.html img = "2020/07/code-review.jpg" title = "Image d'illustration de la revue de code" %}

La qualité du code est par ce fait améliorée, il en ressort plus maintenable, mieux architecturé et permet ainsi de réduire le nombre de bugs engendrés. 

C’est l’outil qui en moyenne permet de détecter le plus de bugs ou de vulnérabilités en amont, et qui plus est a des avantages plus profonds que simplement techniques. 

## Une propagation des connaissances 

En plus des apports non négligeables sur le produit final, la revue de code a également un avantage conséquent sur l’équipe projet. 

La communication et la collaboration sont renforcées par ce mécanisme. 
En effet, la **relecture de code** a un aspect formateur sur l’équipe, que cela soit dans un sens ou dans l’autre. 

Lors par exemple de l’arrivée d’une nouvelle recrue, la relecture par une personne plus séniore va permettre un partage de connaissance plus fluide, avoir des retours sur les méthodes pratiquées, mais aussi d’éventuelles nouveautés à apporter ou des approches à remettre en cause ou autre. 

Permettre la relecture par un junior lui permet également d’intégrer plus facilement le projet et les stratégies utilisées, d’être curieux et poser les bonnes questions pour avancer et l’acquisition des compétences plus rapidement. 

La compréhension et l’expérience projet sont plus facilement ventilées sur l’ensemble des collaborateurs.

## Des règles à respecter

Pour tirer, au mieux, tous les avantages que procure la revue de code, il existe bien entendu des bonnes pratiques.

Tout d’abord l’essentiel est de garder en tête que le succès d’une bonne review vient d’une **responsabilité partagée** entre le relecteur et le codeur. 

En tant que demandeur, il est tout d’abord important d’apporter du contexte au code proposé, il faut accompagner les travaux d’une description. 
La description d’une revue ne sert pas à dire ce qui a été modifié, mais l’intention derrière cette modification, et ce qu’elle apporte.
Il ne faut pas pour autant que cette dernière soit un roman de nombreuses lignes, soyez concis et explicite. 

Gardez également en tête que vous êtes responsable de ce que vous livrez, les excuses comme cette partie n’a pas été écrite par moi ne sont pas possibles, il est nécessaire d’effectuer une autorevue avant de l’assigner. 

Du côté du relecteur désormais, le premier mot d’ordre essentiel est **bienveillance** ! Le jugement n’apporte rien, l’**objectivité** est de mise.

Il ne faut pas chercher la petite bête mais viser une qualité homogène et se concentrer sur le fond. 

Il est nécessaire d’éviter au possible de donner des solutions toutes faites aux correctifs attendus mais plutôt inviter à une réflexion qui peut être orientée et permettre de comprendre facilement qu’elle est la problématique. 


