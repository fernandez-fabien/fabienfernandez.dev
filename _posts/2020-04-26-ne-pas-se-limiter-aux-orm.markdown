---
layout: post
title: "Ne pas se limiter aux ORM"
categories: [Développement-Web]
published: true
image: "2020/04/traduction.jpg"
excerpt: "Les ORM font parti intégrante des outils de programmation et gèrent la communication avec la base de données. On peut donc avoir une confiance aveugle en eux ?"
--- 

Vous vous dites peut-être, mais qu’est-ce que c’est que ça un ORM ? 
Si je vous parle de Doctrine pour Symfony, Eloquent pour Laravel ou encore JPA pour Java, vous avez éventuellement déjà côtoyé ces termes. 

**Object Relational Mapping** ou **mapping objet-relationnel** est en fait un outil informatique qui va servir d’interface de communication entre la partie applicative et la **base de données relationnelle**. 

On va en fait avoir une couche d’abstraction qui va lier nos schémas de base de données à nos classes du programme applicatif. On va à partir de ce dernier gérer des requêtes dans un **langage** simplifié et plus intuitif qui viendra s’intégrer et créer une homogénéité avec le reste du code. 

## Pourquoi faire compliqué quand on peut faire simple ? 

L’ORM est devenu un “must-have” dans les projets informatiques, ils en existent de nombreux, en fonction des langages de programmation et même des différents frameworks que l’on retrouve pour chacun. Pour autant, il fait désormais partie du pack d'installation apporté avec la plupart. 

En effet ces derniers apportent une simplification plus que significative : 

Partons du principe que nous ayons une entité User (utilisateur) dans notre application qui corresponde en base de données à une table ‘user’ qui contient les colonnes ‘email’ et ‘password’ (pour mot de passe’). Grâce à la relation établie via notre ORM nous allons pouvoir créer une instance de notre objet User et faire une demande de répercuter cette information en base dans la table associée (l’exemple suivant est développé avec Doctrine mais le concept reste le même pour l’ensemble des ORM).

```php
$user = new User();
$user->email = "john@doe.fr";
$user->password = "password";
// Demande de répercussion à l’ORM doctrine
$user->save();
```
Ce simple appel à `save()` va permettre de faire la demande à notre **ORM** de traduire notre volonté à notre base relationnelle afin de reproduire l’action est de reste iso entre nos environnements. Il va ainsi produire la requête suivante en conséquence :

```sql
INSERT INTO user (email, password) VALUES ("john@doe.fr", "password");
```
Ceci est un exemple parmi tant d’autres des utilisations d’un ORM qui permet d’adapter des demandes sans les écrire explicitement, dans le **langage SQL** compris par la base de données. 

Un outil qui nous simplifie la vie, où est le mal ? 

## Faut-il avoir une totale confiance en nos ORM  ?

On pourrait ici parler du fait que l’ajout d’une couche supplémentaire peut bien entendu nuire à la maintenance et la maintenabilité. Que les ORM ont fait leur preuve pour les requêtes simples, mais qu’il peut s’avérer plus difficile de déboguer, voire même créer, des requêtes plus complexes. 

Mais le but de cet article n’est pas de démonter les ORM (s’ils sont présents dans la plupart des frameworks, c’est pour une bonne raison). L’intention n’est donc pas de dire s’il faut utiliser ou non un ORM, je vous laisse vous faire votre propre opinion là-dessus. 

Je souhaiterais plutôt mettre en garde, avoir une simple attention à connaître l’envers du décor. Quand j’utilise un ORM je suis conscient de ce qui se passe derrière, je sais quelle requête SQL va être générée en faisant telle ou telle action ou demande. 

Cette réflexion peut paraître bête, mais garder le contrôle est la clé. De plus malgré le fait que les ORM soient très avancés dans leur fonctionnement on ne peut pas tout faire avec ni leur faire confiance à 100% et les utiliser les yeux fermés. 

## Et si c’était vous ? 

Le langage SQL est un langage à part entière, qui possède ces complexités et souvent des possibilités bien plus étendues que ce que l’on pourrait imaginer. 

Si on essayait maintenant de l’humaniser un peu … L’espace d’une minute, voyons l’ORM pareillement à un développeur comme vous et moi. 
Si je vous disais maintenant que je n’ai plus besoin de vous, je vous remplace en intégralité, un robot permet désormais de traduire mes volontés écrites en français en termes de langage informatique qui me serviront à dresser mon site Web ou mon application. 

{% include image.html img = "2020/04/traduction.jpg" title = "Illustration de la traduction automatique" %}

Sans rentrer dans le débat du fait qu’il faudra toujours des développeurs pour programmer une telle intelligence. C’était surtout pour vous piquer dans votre égo et vous donner une image. 

En soi, ce genre d’outil existe déjà, avec Wordpress, Wix ou autre on peut déjà créer des sites sans connaissances techniques. Cela n’empêche qu’il est toujours intéressant de connaître l’envers du décor de la construction et également que ce genre d’outil atteint vite ses limites lorsque l’on cherche de la spécificité. 

Tout ça pour dire que quelque soit l’outil, technique ou non, même s'il paraît magique et sans embûche, il est toujours intéressant de s’attarder un minimum sur la partie cachée de l’iceberg. 
  

