---
layout: post
title: "Git, la face cachée de l'iceberg"
categories: "Méthodologie Développement-Web"
published: true
---

Git, un outil devenu tellement culte que l’ensemble des développeurs le connaissent, ou du moins pense le connaître. 

Cet article n’aura pas pour but d’expliquer ce qu’est Git dans son ensemble, de nombreux articles le font déjà et la valeur ajoutée ne serait pas visible. 
Je vais plutôt faire de petits rappels ou constats sur ce dispositif qui peut être utilisé en mode tête baissée, mais il est toujours intéressant d’en savoir un peu plus. 

## L’arbre qui cache la forêt

Git est devenu le **logiciel de gestion de versions** utilisé dans la plupart des projets de développements. Et comme ses cousins logiciels devenus plus ou moins universels (Word, excel, photoshop, etc), il fait partie des potentielles “usines à gaz” qui présentent une immensité de possibilités et pour qui pourtant la plupart des utilisateurs se contentent d’utiliser très peu de commandes. En effet, avec un petit nombre nécessaire de fonctionnalités, on peut remplir l’ensemble des besoins classiques.

Je vous conseille d’ailleurs cet article de blog d’un ami qui a l’avantage d’être très facilement compréhensible et en même temps très complet concernant les principales commandes et d’autres pouvant permettre d’aller plus loin, sans rentrer dans les détails trop profonds de l’outil : <https://guillaumebriday.fr/comment-jutilise-git-mes-astuces-et-bonnes-pratiques>.

Pour en revenir sur les capacités avancées, on connaît bien la partie de gestion de branche et de push sur un serveur distant (même si la plupart des personnes ne connaissent pas l’ensemble des commandes correspondant à cette thématique) mais d’autres concepts sont disponibles. Encore une fois, je ne vais pas en faire la liste exhaustive je vous renvoie sur d’autres articles ou simplement la documentation officielle, je voudrais plutôt juste égayer votre curiosité. 

Quand j’ai personnellement découvert ne serait-ce que les possibilités que nous offre Git en termes de statistiques j’étais bluffé, et j’ai pu découvrir par la suite qu’il pouvait être utilisé notamment directement pour du debugging ou encore pour de l’administration voir la gestion de mail automatisé. 

## Une utilisation adaptative 

Mais du coup si la plupart des développeurs n’utilisent qu’une très petite partie des commandes disponibles c’est qu’ils ont tous la même utilisation de l’outil ? 

Disons en fait qu’au niveau des commandes tapées les différences ne seront pas vraiment notables cependant c’est l’utilisation dans son ensemble et notamment l’organisation des **branches** qui peut fortement être différent d’un projet à l’autre. 
Vous avez peut-être déjà entendu parler de “**Gitflow**”, ce terme désigne en fait simplement une manière d’organiser son projet (certainement la plus populaire) et surtout l’architecture des branches. 

{% include image.html img = "2020/02/gitflow.png" title = "Schéma de la méthode Git-flow" %}

Sans rentrer trop dans les détails, le principe de base est que le projet sera basé sur deux branches principales : **master** et **develop**. Ces deux branches ne sont pas accessibles en écriture aux développeurs. 
La branche master servant uniquement de miroir de la production, avec des annotations des différentes versions.
La branche develop sera elle la branche qui permettra de centraliser les fonctionnalités qui seront livrées dans la prochaine version.
Elles seront accompagnées de 3 autres types de branches qui viendront se fixer aux moments voulus  :
* Hotifx
* Release
* Feature

Comme toute méthode, cette dernière possède des qualités et des défauts, elle est populaire parce que les qualités sont nombreuses cependant il est toujours intéressant de remettre le projet dans son contexte avant de foncer sur une méthodologie qui pourrait s’avérer non adaptée. 
Pour ce faire il faut se poser des questions importantes du type : 
* Le projet va-t-il être régi par un système d’intégration continue ?
* Est-ce que potentiellement plusieurs personnes vont être amenées à travailler sur une même fonctionnalité ?
* Plusieurs versions du projet vont-elles être nécessaires d’être utilisées en même temps durant la réalisation du projet, que ça soit pour les tests ou autre ?
Cette liste n’est pas exhaustive, mais permet de mettre en exergue la nécessité de découpage plus ou moins profond de différentes strates de branches.

## Bas les masques 

Comme on a pu le dire précédemment, Git est un outil très utilisé de par sa simplicité pour répondre aux besoins primordiaux. 
Cette simplicité ne doit pas nous faire fermer les yeux sur la flexibilité de l’outil et donc la sécurité à mettre autour. 

L’importance de gérer des droits surtout dans le cadre d’une intégration continue mais dans n’importe quel contexte les **droits de push** sur les différentes branches principales du projet ne doivent pas être gérés par défaut. Il faut pouvoir gérer les accès pour contrôler les changements convenablement.
De plus même avec une gestion de sécurité un peu avancée, il ne faut pas perdre à l’idée que Git n’est pas un outil de sauvegarde, que l’historique d’un projet Git est manipulable et qu’il ne garantit en rien la sauvegarde des données, même si dans les cas simples il peut permettre de revenir sur des versions demandées, ce ne doit pas être le principal outil de sauvegarde de vos projets.

Pour conclure, je dirais simplement que lorsque l’on utilise des outils qui nous simplifient la vie il est toujours intéressant de s’intéresser au fonctionnement concret. J’utilise par exemple un utilitaire graphique pour utiliser Git mais je me suis d’abord forcé à comprendre et utiliser les lignes de commandes avant de passer sur cet outil afin d’être plus en maîtrise sur les actions que je réalise. 
Je reviendrais surement sur cette thématique lors d’un prochain article sur le sujet des ORM…  

