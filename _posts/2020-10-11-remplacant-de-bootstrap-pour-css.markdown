---
layout: post
title: "Un remplaçant à Bootstrap trouvé pour le CSS ?"
categories: [Développement-Web, Design]
published: true
image: "2020/10/tailwind.jpg"
excerpt: "Bootstrap est depuis un moment le leader des bibliothèques CSS. As-tu déjà entendu parlé de Tailwind ? Une nouvelle façon d'appréhender le design."
---

CSS est l'un des langages principaux du Web, associé à la structure de page construite en HTML, il permet de mettre en forme cette dernière. Ainsi, les feuilles de style, aussi appelé les fichiers CSS, comprennent du code qui permet de gérer le design d'une page en HTML.

Bien implanté en tant que “titulaire indiscutable”, sa nécessité ne laisse pas place au doute, mais existe-t-il des moyens de faciliter son utilisation, sa mise en place, son optimisation ?

## Constante évolution 

Le CSS a beau être utilisé et bien pris en charge par les navigateurs depuis les années 2000, à l’image de l’univers du Web, il a été obligé d’évoluer. 
Tout comme le langage Javascript connu pour ses nouveautés nombreuses, ces dernières années, notamment via les technologies dérivées (Angular, ReactJs, Vue.js …), l’écosystème CSS a su s’adapter. 

Le code en Javascript et CSS dit pur n’est plus vraiment utilisé. Sans parler des navigateurs qui prennent de plus en plus en compte les possibilités proposées par le langage, différents outils ont permis d’améliorer indirectement la génération des feuilles de style. 

On pense notamment aux extensions comme LESS ou SASS, qui permettent d’écrire de façon plus simplifiée via notamment la possibilité de définir des variables, des fonctions, des boucles, d’utiliser l’héritage ou d’autres options avant de générer le code CSS classique associé. 

Mais outre ces extensions, il existe des bibliothèques qui permettent également d’atteindre une certaine simplification et un gain de temps ... 

## La boîte à outils

Aujourd’hui quand on parle de CSS on a tendance à penser à [Bootstrap](https://getbootstrap.com/). Ce dernier représente un ensemble de solutions comme Foundation, Materialize, Material UI, Bulma, etc, qui apportent un ensemble d’outils et d’éléments préformatés prêts à être utilisés. L’outil de la firme Twitter, Bootstrap, est simplement la bibliothèque la plus connue et la plus utilisée. 

Bootstrap fournit des définitions de base pour tous les composants HTML, ce qui permet de disposer d'apparences uniformes et de gérer le design (graphisme, animation et interactions avec la page dans le navigateur, etc).

La bibliothèque fournit également nombre d'éléments graphiques au format standardisé : boutons, libellés, icônes, cartes, barres de progression…

En plus de ça, il existe de nombreux thèmes communautaires permettant d’avoir des modèles préconstruits de tableaux de bord ou autre. 

L’outil apporte à de nombreuses qualités mais n’a-t-il pas certaines contraintes ? 

## L’utile avant tout : nouvelle vision 

Bootstrap et ses concurrents sont idéaux dans le cadre de POC (Proof Of Concept), dans lesquels ils permettent de mettre en forme de manière propre très rapidement. 

Cependant dans le cadre de projets plus élaborés avec des design spécifiques, ils peuvent atteindre certaines limites. 

Une nouvelle vision émerge via le nom de [Tailwind CSS](https://tailwindcss.com/) avec une manière d’aborder les choses plus orientées sur l’utilité. 

{% include image.html img = "2020/10/tailwind.jpg" title = "Image d'illustration de tailwindcss" style = "w-1/2" %}

Tout d’abord ce dernier se présente comme un véritable framework contrairement aux autres outils plutôt considérés comme des kits UI. 

De base, l’approche amène à écrire de manière exhaustive bien plus de classes (utilitaires) dans le code HTML qui permettent de spécifier les attentes visuelles. Cependant le framework permet bien évidemment de créer ses propres classes et de se rapprocher au besoin du fonctionnement de Bootstrap et de ces classes complètes réutilisables. 

L’avantage se retrouve essentiellement dans sa forte personnalisation, même si Bootstrap permet de ne pas charger l’ensemble de la bibliothèque avec un découpage par grande thématique, Tailwind via son fichier de configuration permet un découpage vraiment précis et ainsi seulement charger les spécifications utilisées. 
Ce qui permet un gain de performance via un poids optimisé. 

Les différences en termes d’avantages ou désavantages entre ces deux types de solutions n’ayant pas vraiment un poids considérable permettant de faire pencher la balance sans opposition possible. 

L’utilisation de l’un ou l’autre va dépendre du contexte et surtout d’une préférence personnelle. 

Cet article est une invitation à s’intéresser de plus près à TailWind CSS, car il est surtout intéressant de connaître cette autre voie et ne pas utiliser la solution classique, par défaut, sans jamais la remettre en question.  


