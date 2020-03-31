---
layout: post
title: "Un blog sans Wordpress ?"
categories: [Développement-Web]
published: true
image: "2020/03/wordpress-jekyll.png"
---

Est-ce que je dois encore le présenter, [Wordpress](https://fr.wordpress.com/) est tout simplement l’outil de gestion de contenu le plus populaire au monde. Environ 35% des sites de la planète tournent sous Wordpress, tous sites confondus. 
C’est la référence en termes de **création de blog**, même s’il a bien sûr des concurrents, mais sa notoriété reste ultra présente et ancrée. 

Une telle réputation ne peut pas être infondée, on peut alors dans le droit de se demander s’il est vraiment intéressant d’explorer d’autres pistes si celle-ci a déjà prouvé son efficacité.

Quels seraient les besoins qu’une autre solution offrirait qui surpasserait le mastodonte ? 

Et si jamais on trouve un élément qui apporte un plus, l’investissement est-il justifié pour la qualité apportée ? 

Ou peut-être que c’est Wordpress qui va au-delà de mes besoins et qui entraîne des problématiques que je n’ai pas spécialement envie de gérer ? 

## La haine au coeur du débat ? 

Tout d’abord j’aimerais mettre les choses au clair, et éviter de vous laisser penser que le choix que j’ai fait été d’abord instancié par un avis subjectif.

En effet, malgré son utilisation massive, Wordpress a en général une mauvaise réputation auprès des développeurs, qui peuvent avoir jusqu’à des réactions de dégoût en entendant ce terme. 

Je suis moi-même développeur Web, j’ai été amené à travailler avec Wordpress sur plusieurs projets et pourtant je ne ressens aucune haine envers ce **CMS** (Content Management System), au contraire mon expérience avec lui était plutôt satisfaisante ! 

Et pourtant j’ai fait le choix de ne pas l’utiliser pour mon **blog personnel**. C’est notamment grâce à mes compétences de développeur que j’ai pu faire ce choix. En effet, Wordpress est un des outils parfaits pour la prise en main d’un site Web pour une personne lambda qui veut se lancer, sa simplicité pour un rendu bien travaillé est impressionnant. 

Cependant moi j’ai cherché plutôt à voir si je ne pouvais pas me débarrasser des boulets qui sont accrochés aux pieds de ce dernier.   

## Balayons les contraintes

Aller, je ne vous fais pas attendre plus longtemps. J’ai pour ma part choisi d’utiliser [Jekyll](https://jekyllrb.com/) pour réaliser mon blog. 
Tout comme ses concurrents plus récents comme Hugo ou Gatsby, Jekyll va permettre de réaliser ce que j’appelle un site “statique dynamique”. C’est paradoxal, mais l’idée derrière tout cela, c’est que l’on aura à la fin un site complètement statique (simple structure HTML, CSS) mais ces pages seront générées via des outils qui permettent de gérer des templates et autres types de fonctionnalité générique qui permette d’automatiser des parties. 
Je pourrais aller plus loin dans le détail de l’outil si cela vous intéresse dans un prochain article. 

{% include image.html img = "2020/03/wordpress-jekyll.png" title = "Wordpress versus Jekyll" style = "w-1/2" %}

En attendant, je vais plutôt vous présenter les avantages que présente cette solution par rapport à un site Wordpress classique : 
* *Gain de performance* : Le rendu visuel est le même est pourtant le site est plus rapide. En effet, le fait que l’ensemble des pages soient compilées et rendues en **pages statiques** HTML fait que ces dernières n’ont pas à être générées à chaque venue sur le site. Il n’y pas de nombreuses requêtes redondantes qui sont faites, il n’y a tout simplement pas de liaison à une base de données, les chargements sont donc plus rapides. La qualité de l’expérience utilisateur est augmentée.
* *Gain de stabilité et de sécurité* : Wordpress étant l’outil le plus utilisé au monde, il est également la cible numéro un des hackers. Il est toujours nécessaire de faire évoluer son code et se tenir à jour au niveau des mises à jour de sécurité pour éviter les mauvaises surprises. Comme on livre ici simplement des fichiers .html, les intrusions ne sont pas une crainte à prendre en compte. 
* *Sauvegarde* : Avec Jekyll, on se retrouve exclusivement avec des fichiers. Que ce soit pour la configuration de l’outil, le thème ou mêmes les articles, on a seulement à faire à des fichiers .md, .html ou .yml. Pas la peine de réaliser régulièrement des extractions de la base et de les sauvegarder afin de ne pas perdre toutes les données. Contrairement à WordPress, on versionne l’ensemble en un seul dossier léger.
* *Écriture non dépendante* : Jekyll permet d’utiliser le **format markdown** pour l’écriture de nos articles qui seront par la suite transformés en HTML. Ce principe permet de pouvoir écrire son article simplement, je peux même écrire mon article sur mon portable en me souciant de la structure sans prise de tête et sans avoir besoin de me connecter à une interface Web.  

## L’hébergement simplifié

Un autre avantage non cité précédemment qui n’est pas le plus important, mais ne fait pas partie des moindres non plus, c’est celui de l’hébergement. 

Une fois compilé, l'ensemble de votre site se retrouve dans dossier spécifique nommé _site. Ce dernier contient tous les fichiers HTML nommés en fonction des pages, mais aussi des sous-dossiers (pour gérer des catégories par exemple), ainsi que les images et l’ensemble des éléments nécessaires au bon fonctionnement du site.

Le processus ayant pour but de faire l’ensemble des réglages et modifications en amont et ne pas toucher ce dossier directement. L’idée étant simplement de glisser le dossier sur notre serveur via FTP et l’affaire est dans le sac. 

Mais on peut encore aller plus loin dans **la facilité et l’automatisation**. 
Aujourd’hui, plusieurs services d’hébergement proposent des connexions via Git pour faciliter l’automatisation. 

J’utilise pour ma part Netlify qui possède une offre d’hébergement gratuite dans le cadre d’un site statique non lié à une base de données (notre cas ici).
Mon compte Netlify est lié à mon compte Github sur lequel se trouve le repository du code de mon site Web. J’ai configuré ce dernier pour que chaque ajout sur la branche master de ce projet soit surveillé, et qu’au moment d’un push, cela déclenche l’action de générer le site et déployer la dernière version. 

J’ai ainsi un **hébergement gratuit** (en dehors du nom de domaine) qui en plus est automatisé pour les déploiements, je ne dois plus me soucier que de gérer mon projet Git afin de mettre à jour mon site. 
 
