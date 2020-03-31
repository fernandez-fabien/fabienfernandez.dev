---
layout: post
title: "TDD, un investissement trop conséquent ?"
categories: [Méthodologie, Développement-Web]
published: true
image: "2020/03/cycle-tdd.png"
---

Vous avez peut-être déjà entendu parler de **TDD (Test Driven Development)**. Ce terme désigne en fait une méthodologie qui nous permet d’allier tests unitaires et programmation de manière organisée.

Le TDD est-il la solution miracle ?

Est-elle trop chère à mettre en place dans un projet ? 

## Mais au fait, qu’est-ce qu’un test unitaire ? 

Revenons dans un premier temps sur une notion qui peut être controversée, la définition du test unitaire et notamment de l’unité.  
Je vais prendre un peu parti dans ce cas parce qu’une partie des gens définit l’unité comme correspondant aux composants, aux méthodes aux classes … 
Dans mon esprit l’unité recherchée dans les tests unitaires concerne plutôt un **chemin logique** !

Si je prends en exemple une simple méthode dans laquelle on trouve une condition “if else” on aura alors une seule méthode et pourtant deux chemins logiques qui doivent chacun être testés afin de **couvrir** l’ensemble des possibilités qu’offre l’application. 

Mais alors on va simplement programmer l’ensemble de notre application et par la suite tester chacun des “itinéraires” qui peuvent être empruntés dans notre code ?

## La philosophie du TDD

Nous pouvons maintenant revenir sur notre sujet principal, j’ai nommé le TDD ! 
Cette méthodologie prend le pas sur l’idée naturelle d’écrire les tests à la suite du développement, au contraire celle-ci nous encourage à écrire le test avant même d’avoir écrit une ligne de code. 

La philosophie générale du TDD se résume ainsi : 
* Tout d’abord écrire un test,
* Vérifier qu’il échoue,
* Écrire le code suffisant (simple) pour que le test passe,
* Vérifier la validation de ce dernier,
* Optimiser le code et vérifier qu’il n’y ait pas de régression.
* Itérer sur ces principes afin d’avancer sur les fonctionnalités de l’application.

{% include image.html img = "2020/03/cycle-tdd.png" title = "Schéma du cycle de TDD" %}

## Un investissement de qualité

La méthode TDD peine à émerger parce qu’elle paraît apporter un surcoût sur le projet.
J’aime à voir ce genre de chose plutôt comme un investissement, comparer un loyer au remboursement d’un prêt pour l’achat d’un logement, le coût direct est plus important, mais sur la durée le coût est lissé et rentabilisé sur le gain obtenu. 

En effet, la **méthodologie**  peut être dans un premier temps assez compliquée à appréhender et à mettre en place du fait qu’il va falloir remettre en question son raisonnement, cette démarche est dans un premier temps à l’inverse du naturel. 
Cependant, une fois en place les avantages peuvent faire la différence sur une procédure normale qui plus est si les tests unitaires ne sont pas réalisés dans la foulée et demandent une analyse préalable pour se remettre dans le bain. 

Dans tous les cas cette façon de faire permet en général de se rendre compte plus tôt d'éventuels défauts qu’il aurait fallu rattraper par la suite.
Elle permet également de décorréler les tests de l’implémentation choisie, en effet lorsqu’on écrit les tests a posteriori, on a tendance à les rédiger en fonction de l’implémentation plutôt que vraiment en fonction de la fonctionnalité de départ en elle-même.
De plus la méthode itérable permet d’assurer naturellement une couverture de code haute du fait que l’on écrit le code qui correspond à la validation du test.  

De manière générale, cette stratégie évite en général de partir tête baissée dans son code et de se perdre en chemin et d’engendrer de la dette technique ou fonctionnelle qu’il sera surement nécessaire de rattraper dans un effort de mise au point en fin de projet. 

