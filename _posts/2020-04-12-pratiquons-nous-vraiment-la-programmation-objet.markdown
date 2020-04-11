---
layout: post
title: "Pratiquons-nous vraiment la programmation objet ?"
categories: [Développement-Web]
published: true
image: "2020/04/boite-noire-programmation-objet.jpg"
excerpt: "La programmation orientée objet ou POO semble complètement acquise dans le monde de la programmation, mais est-elle pour autant respectée correctement ?"
---

La programmation objet, ou plutôt la **programmation orientée objet** (**POO**), est un paradigme de programmation informatique qui est, aujourd’hui, sûrement le plus utilisé. Il s’oppose principalement à la programmation procédurale. 

Comme son nom l’indique, la programmation objet consiste en une interaction de briques logicielles appelées objets. 

Cet article aura pour but d’essayer d’apporter une vision simple sur ce que cela représente et quels en sont les intérêts, pour enfin terminer sur une prise de recul et une critique de l’utilisation actuelle … 

## Concrètement qu’est-ce qu’un objet ? 

En informatique, un objet représente une sorte de conteneur, qui va permettre des manipulations, pour pouvoir interagir avec les informations qu’il renferme. Je reconnais que le concept est assez abstrait et peut paraître compliqué à aborder. 

Je vais tenter d’aller un peu plus loin dans les explications sans trop complexifier, vous pouvez également faire vos propres recherches (je vous conseille notamment [cette explication](https://www.youtube.com/watch?v=cD2o7YudR3k)) ou si vous connaissez déjà le concept, réfléchissez à comment vous présenteriez la chose. 

Reprenons, on connaît les objets standards que sont les chaînes de caractère, les nombres ou encore les tableaux, mais sans vouloir entraver sur la deuxième partie de cet article, il faut savoir que l’on est en capacité de créer nos propres objets et pouvoir gérer les informations qu’ils comportent. 

Un des objets que l’on retrouve le plus dans les différentes applications (même s'il n’a pas toujours le même format), c’est l’objet qui représente un utilisateur. Celui-ci est utilisé pour *incarner*/*symboliser* les données qui permettront l’identification sur la plateforme. 

Le but premier d’un objet est de détenir des mécanismes internes qui accorderont la possibilité, en l’interrogeant, d’obtenir des informations spécifiques. 

## Quels sont les avantages de ce concept ?

Un des apports de la programmation orientée objet, c’est de pouvoir se débarrasser du fouillis légendaire de la programmation procédurale, en organisant son code pour qu’il devienne plus réutilisable. Généralement on va avoir tendance à créer des **objets programmatiques qui vont correspondre aux entités du domaine métier** dans lequel s'inscrit le projet. 
En allant plus loin, des objets pourront servir de base à d’autres, en retirant seulement des évolutions nécessaires (il faudra alors s’intéresser à des concepts tels que l’héritage, le polymorphisme, etc). 

Cette organisation multiplie les avantages, elle encourage notamment le **travail collaboratif**, apporte de la **stabilité** et ainsi une plus grande aisance dans la maintenance ; permet en général la **simplification du code** dans son ensemble (en fonction du niveau d’abstraction adopté, mais rend généralement la production plus agréable).  

Le succès de ce paradigme est régi par la communication entre les objets ; les interactions entre chacun d’eux vont en effet permettre d’assembler et de formater des données, afin de les fournir à l’utilisateur final qui interagit lui directement avec l’application. 

## Programmation objet, une fin en soi ?

La première partie correspond à une présentation objective du sujet, la seconde partie va, quant à elle, être plus subjective. Je préfère prévenir, que ce qui va suivre engage plutôt mon avis sur le sujet, mais je suis prêt à échanger sur toute autre position sur cette thématique.

Passons ainsi au vif du sujet :  

L’utilisation actuelle de la programmation objet, ou du moins ce que nous convenons comme telle, est pour moi biaisée. Mes travaux personnels entrent également dans cette restriction et sortent également de l’essence même du paradigme.

Laissez-moi m’expliquer, et revenons-en pour ça à une image simple, pour commencer à exprimer mon ressenti. Précédemment, nous avons vu les objets classiques tels que les chaînes de caractère ou les nombres. Imaginons maintenant quelques interactions que nous pourrions avoir avec des instanciations de ces derniers à l’intérieur d’un logiciel (de manière un petit peu familiarisée).

“Hé salut, peux-tu me donner ta taille (chaîne de caractère) ?”
“Es-tu un multiple de trois ? Es-tu un chiffre pair ?”

Mes exemples ne sont peut être pas parlant d’eux-mêmes mais ils comportent pourtant un point commun qui va permettre d’aborder le point central de cette “revendication”. 
À chaque question on va en fait faire une requête et attendre une réponse concrète en retour sans pour autant s’attarder sur la manière avec laquelle cette question va être résolue. 

Pour moi, la quintessence de la programmation objet se trouve dans le fait que **l’intelligence du programme doit résider dans la communication et donc dans les échanges entre les objets, plutôt que dans les objets eux-mêmes**. Bien entendu, chaque objet doit avoir son propre mécanisme interne, mais par principe, la construction des éléments doit être réalisée dans la transmission d’informations. 

Pour être plus clair, chaque objet devrait être une sorte de **boîte noire**, on veut lui fournir des données en entrée et qu’il nous retourne des informations en sortie, sans savoir quels sont ses processus en interne pour nous apporter les renseignements escomptés. 
 
 {% include image.html img = "2020/04/boite-noire-programmation-objet.jpg" title = "Schéma d'explication de la boîte noire" style = "w-1/2" %}

Si vous avez maintenant compris le concept que j’essaye de vous partager, réfléchissez désormais à ce que proposent la plupart des **frameworks de langages orientés objet**. Notamment les fonctions de bases que sont les **Getters** et les **Setters**…
Ces dernières vont à l’encontre même de l’esprit du paradigme objet que je viens de partager avec vous. En effet, avec ces dernières, on part du principe que l’on sait ce qui se passe à l’intérieur de l’objet et on peut lui demander expressément des données internes. Les objets deviennent alors ce que l’on appelle des boîtes blanches…

Pour conclure, cet article ne vise pas à inciter à vouloir absolument coder en respectant une programmation orientée objet, que je qualifierais de pure. Ayant moi-même expérimenté le respect total de cette option, je me suis rapidement confronté aux difficultés de cette dernière, qui est souvent dure à concevoir et à vraiment mettre en place (ce que les frameworks apportent étant souvent incompatibles avec cette façon de faire). 
Mon but était plutôt de vous amener à une prise de recul, pour savoir adopter un regard critique, même dans les cas qui paraissent universellement acquis. 
