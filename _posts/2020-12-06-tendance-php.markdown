---
layout: post
title: "PHP 8 : la tendance continue"
categories: [Développement-Web]
published: true
image: "2020/12/php.jpg"
excerpt: "PHP, l'évolution suit son court, mais y a t-il une cible à atteindre ? Une tendance continue ? Prenons un peu de recul sur la continuité du langage"
--- 

On a tendance à dire que le Web évolue à une vitesse folle, on pense notamment aux nombreux frameworks Javascript qui naissent régulièrement et dont les versions continuent d’être mises à jour, cependant, c’est également le cas pour les langages de programmation eux-mêmes qui se doivent de proposer des améliorations et permettre de suivre ce rythme endiablé.

{% include image.html img = "2020/12/php.jpg" title = "Image d'illustration de l'évolution de PHP" style = "w-1/2" %}

Parlons de la version 8 de PHP, entre autre …

## La vitesse à l’honneur

Il ne faut pas l’oublier, le progrès principal de la version 7 de PHP se tenait autour des performances et de la vitesse d’exécution qui avait pris un gros coup de boost par rapport à la version précédente (5). 

Pour rappel, PHP est un langage interprété, ce qui veut dire que le code n’est pas transformé en fichiers exécutables par la machine, contrairement aux langages compilés.
Dans le cadre de PHP, il est d’abord converti en opcode, qui sera à son tour exécuté par une machine virtuelle. Ce choix de conception fait que l’exécution est plus lente que pour les langages compilés.

Cette problématique a ainsi été à l’honneur pour la communauté PHP, avec des opérations pour booster les performances, on pense alors notamment au cache d’opcode.
Comme son nom l’indique, c’est un système de cache, qui a fini par être intégré par défaut au cœur de PHP, qui permet de garder en mémoire et ne pas répéter entièrement l’interprétation complète à chaque requête. 

PHP 8 arrive avec son compilateur JIT (“Just In Time”), qui promet d’améliorer les performances (module activable ou non, au choix comme l’était l’extension Zend OPcache). 
Pour faire simple, il va se rapprocher d’un système de cache, en passant par la compilation à la volée de certaines parties du code pendant son exécution.

Dans l’ensemble une simplification et une amélioration, qui est annoncée comme ayant ses limites lorsqu'on l’associe à Wordpress ou encore et qui pourrait apporter, dans certains cas, une certaine complexité. Il faudra attendre d’avoir plus de recul sur cette nouveauté …

## Une tendance vers un point central

PHP 8 arrive avec de nouvelles fonctionnalités à l’appui. Ce billet de blog n’a pas pour but de faire la liste de ces dernières, elles seront bien mieux détaillées dans la documentation officielle ou dans des blogs spécifiques orientés sur la technique. 

Nous parlerons simplement de la tendance qui en découle, pas seulement à partir de cette dernière version, mais plutôt une continuité dans l’évolution qui est amenée petit à petit au langage. 

PHP était au départ un langage très libre, à la base qui ne faisait pas partie des langages orientés objet, mais la tendance semble être continue. 

En effet, certains des langages “concurrents” de PHP sont au départ des langages plus rigides dans le sens où ils utilisent du typage strict et d’autres méthodologies de ce type.
La tendance étant souvent de leur côté à l’assouplissement. 

À l’opposé, comme s' il y avait un point de rencontre à atteindre, PHP à tendance à proposer plus de rigueur et de précision notamment au niveau des typages que l’on retrouve maintenant pour les paramètres de fonctions/méthodes et pour leur valeur de retour.

On retrouve notamment les types d’union 2.0 et les attributs v2 dans cette dernière version. 

Comme toujours, pour apprécier, comprendre et avoir un regard critique sur les évolutions d’un langage, il est intéressant d’avoir un oeil sur ce qu’il se fait ailleurs… 
