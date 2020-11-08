---
layout: post
title: "DDD : théorie et pratique"
categories: [Développement-Web, Méthodologie]
published: true
image: "2020/11/ddd.jpg"
excerpt: "Domain Driven Design plus communément appelé DDD, tu as surêment déjà entendu ce terme mais connais tu ça signification, les aspects qui sont derrières ?"
---

Le DDD ou Domain Driven Design est un terme qui a le vent en poupe, qui est comme qui dirait à la mode. 

Mais que signifie vraiment ce concept ? 

Cette popularité est-elle méritée ? 

## L’architecture unique, pour les gouverner tous

Quand on parle de projet informatique, il y a un premier type d’organisation représenté par l’architecture technique de ce dernier. 

Le but d’une bonne architecture en DDD est de sanctuariser le métier, le sacraliser afin de le préserver de toutes les interactions extérieures susceptibles d’interférer dans son bon fonctionnement.

Le modèle principal possède sa propre existence à l’écart des autres composants du projet. Seule une demande émanant du métier doit pouvoir engendre une modification du modèle. Le modèle ne doit pas être impacté par les autres changements, que l’on parle de l’hébergement, la performance, la sécurité, la manière de consommer les données, etc. 

Dans l'idéal, le graal serait d'avoir un modèle unique et unifié. L’objectif à beau être noble, il ne colle pas réellement à la réalité, il se fragmente généralement en plusieurs modèles. Il est utile de reconnaître cette réalité et de travailler avec elle.

Plus concrètement, l’architecture DDD se découpe en 4 strates distinctes que sont :
Infrastructure : Représentant la partie technique qui peut être associée, à la persistance, la sécurité, etc.
Présentation : Communication extérieure, pouvant être représenté par des web services, une interface utilisateur, etc. 
Application : Règles qui auront pour rôle d’invoquer la logique métier présent dans le dernier compartiment.
Domaine : Représente toute la logique métier, le modèle principal. 

Mais la DDD ne s’arrête pas à une simple architecture loin de là ....

## Une vraie philosophie

Le DDD est avant tout une philosophie, une vision à emprunter et respecter. C’est un principe de conception qui se veut être piloté entièrement par le métier. 

{% include image.html img = "2020/11/ddd.jpg" title = "Image d'illustration du DDD" style = "w-1/2" %}

La base pour mettre le métier au centre est avant tout la communication et la compréhension qui permettra de définir explicitement le contexte dans lequel un modèle s'applique. 

Définir la chaîne de travail qui permet d’éclater la complexité des procédures métier à un niveau unitaire. La formule à suivre va être de documenter le flux métier au complet en ayant à l’esprit la notion de vulgarisation afin que n’importe qui soit capable de le comprendre. Tous les contributeurs et collaborateurs doivent atteindre une intelligence globale de la logique métier grâce à un langage commun.

Ce processus de modélisation porte le nom de “Knowledge crunching”, il doit être réalisé dans une collaboration conjointe entre les développeurs et les experts métier. 
Il faut alors faire le tri dans le flot d’informations à notre disposition afin de conserver seulement les plus importantes, les simplifier dans un même langage. 
Il faut bien évidemment se focaliser uniquement sur les aspects utiles pour éviter de se noyer dans un flot trop important d’informations non pertinentes. Il s’agit donc de traiter une quantité importante d’information et avoir la capacité de n’en retenir que les pertinentes d’une part ; et, d’autre part, d’être capable de suffisamment la vulgariser et la simplifier afin que l’équipe entière soit en mesure de travailler à partir de ces modèles de conception. L’équipe technique doit comprendre le produit et se l’approprier...

## Sortir des sentiers battus

Bien entendu, la mise en place du DDD engendre un certain coût, surtout que cela n’implique pas que le projet pourra être réalisé plus rapidement ou engendrer moins de lignes voire au contraire… Cependant l’objectif est plutôt long terme, cette façon de faire sera beaucoup plus fiable sur la maintenabilité et la mise en place d’évolution sera facilité par la suite. 

Son adoption est d’autant plus appréciable et retentissante lorsque le domaine métier est vraiment spécifique.

La conception DDD implique aussi de remettre en cause des actions qui peuvent être devenues des actes par défaut dans notre esprit. L’exemple de la factorisation à tout prix n’est pas toujours une bonne chose dans ce genre de contexte. 
Garder un code spécifique et décourager les réutilisations abusives susceptibles d'entraîner des couplages forts (fonctionnellement et par le code). 
Toutefois cela ne s’applique qu’au domaine métier, la mutualisation dans les socles comme l’infrastructure ou autres permettent en général de simplifier l’utilisation du SI.

Pour aller plus loin, on peut parler des tests fonctionnels, on utilise en général des langages simples comme avec la syntaxe gerkhin afin de définir des scénarios fonctionnels de tests. 
Les normes et bonnes pratiques veulent que le code soit toujours écrit en anglais, mais si le domaine métier est très spécifique et que des termes spécifiques (n’ayant pas toujours de traduction adéquate) sont utilisés, ne peut-on pas envisager d’écrire ces tests dans la langue d’origine ? 
