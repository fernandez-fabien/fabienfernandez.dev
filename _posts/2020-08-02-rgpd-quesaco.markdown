---
layout: post
title: "RGPD quésaco ?"
categories: [Méthodologie, Développement-Web]
published: true
image: "2020/08/rgpd.jpg"
excerpt: "Le RGPD, on a souvent entendu parlé de ce concept sans toujours vraiment savoir de quoi il en retourne. Introduisons le sujet pour connaître les conséquences."
---

Le **RGPD** ou **règlement général de protection des données** est un décret entré en vigueur en mai 2018. 

Pourtant il reste souvent flou dans les esprits et on ne connaît pas vraiment les conséquences que cela engendre. 

Cet article n’a pas pour but de rentrer dans les détails profonds et d’exprimer de manière exhaustive les répercussions de ce texte de loi, mais plutôt d’en introduire simplement les concepts phares afin d’en ressortir un peu plus éclairé sur le sujet. 

## Concrètement ça correspond à quoi ? 

Règlement européen qui prend le pas sur toutes les législations locales de tous les pays européens, avec une légère marge de manoeuvre pour être adapté à des besoins spécifiques. 

{% include image.html img = "2020/08/rgpd.jpg" title = "Image d'illustration de la rgpd" %}

Ce dernier est basé sur la définition de la **donnée personnelle**,c’est-à-dire tout ce qui peut permettre d'identifier une personne directement ou indirectement comme par exemple : 
- nom 
- prénom
- adresse
- date de naissance 
- ...
Est également inclus tout ce qui touche au profilage comme le comportement sur internet.

Il concerne tous ceux qui utilisent ces données d’un point de vue légal ou technique, c’est donc dans le rôle du développeur de contrôler et vérifier comment sont gérées ces dernières. 

Pas de moyen d’y échapper, où que les données soient stockées (pays hors UE) ou si la société détentrice est étrangère c’est la nationalité de la personne à qui correspond la donnée qui compte. 

Il est nécessaire de connaître le moyen de protéger ce nouveau pétrole du XXIe siècle que sont les données. 

## Principe de minimisation

On ne collecte pas de données qui ne servent pas, dans le cas contraire, il faut apporter la preuve que cette collecte de données était un besoin. Ce qui consiste à écrire une documentation qui devra être fournie en cas de contrôle de l’autorité pour servir de justificatif. La charge de la preuve étant dans le camp de “l’accusé”.

On parle également du concept de privé par défaut, soit collecter le strict minimum correspondant au traitement qui sera exécuté. 

Un concept plus avancé est celui de la pseudonymisation, le but de cette mécanique étant de rendre les données comme anonymes dans le sens où elles ne peuvent pas être attribuées sans avoir recours à des informations tierces (stockées ailleurs, à part). 

Mais cela ne reste pas une garantie à 100% en soi. 

## Le client est roi 

L’une des principales raisons valables de collecter des informations selon le RGPD est d’avoir obtenu le consentement de l’utilisateur en amont et comme dit précédemment de pouvoir prouver cette acceptation. 

L’utilisateur doit être informé des informations qui seront récupérées dans quel but ainsi que le temps que sera détenue cette information (la donnée ne peut pas être stockée éternellement elle doit avoir une durée de vie spécifiée et être supprimée passé ce délai. 

Il est important de savoir que le consentement doit être éclairé et actif c’est à dire qu’une action doit être réalisée (exemple case à cocher à valider et non mise par défaut) pour valider l’accord. Il faut oublier la fameuse phrase : "Qui ne dit mots conssent". 
De plus, ce dernier doit pouvoir refuser la demande et il est légalement interdit de lui interdire l’accès au service de par ce refus. 

En outre, l’utilisateur doit à tout moment avoir les pleins pouvoirs sur ces données, à savoir demander un recueil complet ou simplement solliciter une modification ou une suppression de ces dernières. 

Le sujet est tout de même complexe et il est important de se renseigner sur le sujet, surtout en tant que développeur qui a un fort rôle de conseil auprès du client ainsi qu’un rôle de garde de fou… 
