---
layout: post
title: "Les tests fonctionnels, un apport multifacette"
categories: [Méthodologie, Développement-Web]
published: true
---

À la suite de notre article abordant la base de la pyramide via la [méthodologie du TDD]({% post_url 2020-03-01-tdd-investissement-trop-consequent %}) j’ai nommé les tests unitaires. On va maintenant parler de la partie haute de cet ensemble, les tests fonctionnels et ce qu’ils apportent à leur niveau. 

{% include image.html img = "2020/03/pyramide.png" title = "Schéma de la pyramide des tests" style = "w-1/2" %}

On peut se dire que les tests unitaires (TU) peuvent être suffisants, comme ils apportent des bases solides donnant par conséquent une garantie de meilleure qualité.

Le haut d’une pyramide de besoin est souvent associé à un idéal à atteindre qui peut sembler être un détail superflu pour viser la perfection. 

On va ainsi chercher à voir les apports des tests fonctionnels et déterminer s'ils sont intéressants ...

## Comment décrire un test fonctionnel 

Les tests fonctionnels, à l’opposé des tests unitaires qui eux nécessitent de rentrer dans le code de l’application pour être réalisés (“boîte blanche”), sont dit “boîte noire” car il n’est pas nécessaire de connaître le code de l’application pour pouvoir les réaliser. 

Les tests fonctionnels ont pour but de s’assurer que dans un contexte d’utilisation réelle, le comportement fonctionnel obtenu est bien conforme avec celui attendu.

Un test fonctionnel est destiné à dérouler un **scénario** composé d’une liste d’actions et d’une liste de vérification validant la conformité avec le processus recherché.

La destination convoitée des tests fonctionnels est de valider la qualité d’un système dans son ensemble, le fonctionnement adéquat. On peut avoir des tests unitaires tous au vert, mais des fonctionnalités qui ne s'intègrent pas entre elles. 
Grâce à ces derniers, nous allons valider la conformité de nos actions au moment de leur mise en place mais en plus de ça, ils nous permettent également de réaliser des **tests de non-régression**. En effet, lorsque l’on va ajouter une fonctionnalité à notre application, on va pouvoir relancer l’ensemble des tests afin de vérifier que notre évolution s'intègre bien avec le reste sans provoquer de problème sur les parties déjà en place précédemment. 

## La mise en place concrète

Le but de cet article n’est pas de rentrer dans le détail technique de la mise en place de tests fonctionnels mais plutôt d’en donner les premières clefs et montrer comment il peut permettre le bon déroulement d’un projet à plusieurs niveaux

Quand on parle de tests fonctionnels, on a des langages particuliers qui ressortent et notamment le format de spécification **Gherkin**.
Cette syntaxe permet de spécifier les attentes à l’écrit qui seront retranscrites par la suite dans le code afin d’automatiser les tests.

Ce format se présente sous le format suivant : 
* Titre de la fonctionnalité
* Nom de scénario de test
* Développement du scénario en suivant les étapes (mots clefs) suivantes :   
  * Étant donné que …
  * Quand …
  * Alors …

L’avantage premier de ce format c’est qu’il doit rester simple et compréhensible de tous en respectant toujours le même patron de conception. 

## Intégrer le client dans son processus

Maintenant que nous avons défini un peu à quoi correspond vraiment la notion de tests fonctionnels, je propose de prendre un peu de recul pour découvrir ce qu’ils peuvent apporter dans un projet d’un point de vue plus généraliste. 
Nous avons vu que ces derniers étaient assez élémentaires dans leur représentation.
Cette simplicité permet d’ouvrir les champs du possible au niveau de la communication et du partage. 

Il peut être intéressant d’intégrer ce système dans la **relation client** du projet, que cela soit directement avec ou par l’intermédiaire d’un PO (Product owner) ou autre en fonction de l’organisation de votre projet. 
L’idée c’est de concevoir la spécification de ces tests en coopération.

Cela permet dans un premier temps de remettre le client au centre de son projet, l’impliquer de manière positive et retrouver la sensation que **la réussite d’un projet vient d’une bonne collaboration**. 

Ce processus permet également de ne pas avoir de soucis au moment de la recette des fonctionnalités, comme le client aura été acteur de la rédaction des attentes il ne pourra pas aisément dire que le rendu et l’attendu ne sont pas cohérents. 

Cet argument peut également être utilisé lors de la réalisation du devis et dans le conseil du choix à opérer pour trouver le bon équilibre dans le fameux **triangle “Coût - Qualité - Délais”**, concept sur lequel je reviendrais peut-être dans le cadre d’un futur article. 


