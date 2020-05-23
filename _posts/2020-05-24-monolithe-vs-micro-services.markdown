---
layout: post
title: "Monolithe vs micro services"
categories: [Développement-Web]
published: true
image: "2020/05/architecture.jpg"
excerpt: "Les projets informatiques font souvent l’objet de guéguerres pour déterminer la bonne architecture à utiliser. Souvent choisie par affinité plus que par logique"
---

Dans les projets informatiques une des premières grandes étapes au niveau technique c’est de faire les choix architecturaux, quels sont les outils et langages à utiliser et comment organiser l’application.  

On a maintenant pu faire beaucoup de tests sur différents projets, il devrait maintenant y avoir une solution qui se distingue des autres.

Peut-être une organisation capable de s’adapter à toutes les situations et permettant d’être efficace ?

## L’exemple d’un framework populaire 

Il y a un temps eu une sorte de guerre entre la vision **monolithique** (c’est-à-dire un seul même et gros bloc) et la version **microservices** (tout découpé en petits morceaux indépendants).

{% include image.html img = "2020/05/architecture.jpg" title = "Illustration du monolithe et des micro-services" style = "w-1/2" %}

C’est une vision un peu raccourcie et simplifiée des grandes tendances que l’on a pu connaître et suivre.

À l’image du **framework Symfony** qui est passé par plusieurs tests de ces différentes stratégies. 

En effet, la version 4 du framework se voulait ultra light et morcelée le plus possible pour laisser la possibilité à l’utilisateur de bien choisir chacune de ces petites briques. Cette méthode a ses avantages, mais également ces inconvénients. 

Ce qui a notamment engendré le fait que dans sa version 5 Symfony est revenu sur une structure un peu plus monolithique avec un coeur plus complet au départ et moins fragmenté. 

## La solution miracle

Si un framework a fait un test et est revenu sur sa décision, on est dans la possibilité de se dire que la solution finale doit être la plus optimisée de toutes et être comme une solution miracle pour tout projet. 

On a tendance à voir des personnes qui demandent comment organiser un projet, quels langages choisir et voir des développeurs répondre : 
“C’est simple tu pars sur cette solution, c’est super pour les performances, tu vas pouvoir gérer ta base de données facilement comme ça, etc.”.

Et bien “let’s go” j’ai envie de dire, allons y le tour est joué, on a les clés en main, il suffit maintenant d’appliquer et d’avancer. 

Un problème ?

Cette réponse est souvent donnée sans même connaître le besoin du projet et le contexte autour. 

## Le besoin avant tout 

Partons d’un simple constat, architecte projet est un métier a part entière, plus que ça, c’est un des métiers les plus prisés de la branche du moins l’un des plus “prestigieux”. 

À partir de là, difficile de se dire qu’il existe une architecture idéale pour tout. Il peut y avoir quasiment autant d‘organisation qu’il y a de projets, et ce n’est pas pour rien, il est important de s’adapter. 

En effet un petit projet qui n’aura pas besoin de base de données ou de nombreuses connexions simultanées ne devra jamais être appréhendé comme un projet bien plus volumineux et grand public.

Je le répète assez souvent mais la prise de recul est souvent la clé. Dans ce cas, prendre le temps de bien analyser le besoin, l’environnement et plus généralement le **contexte** est une étape plus qu’importante avant de se lancer dans une solution non adaptée qui risque le plus souvent d’être surdimensionnée.

Évitez d’utiliser un rouleau compresseur pour écraser un moustique. 
