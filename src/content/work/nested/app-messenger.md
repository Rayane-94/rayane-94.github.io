---
title: Application style Messenger 
publishDate: 2025-03-04 00:00:00
img: /assets/Facebook_Messenger_logo_2020.svg.webp
img_alt: image morpion 
description: |
  Application de messagerie en temps réel développée en équipe, avec React, NestJS, RabbitMQ et GraphQL.
tags:
  - React
  - TypeScript
  - NestJS
  - GraphQL
  - RabbitMQ
  - Prisma
---

Ce projet a été réalisé dans le cadre d’un travail de groupe à 3 personnes. Il s’agit d’une application de messagerie en temps réel, inspirée de Messenger, qui permet à des utilisateurs de s’inscrire, se connecter, créer des conversations à deux et s’envoyer des messages instantanément.

Nous avons conçu le backend avec **NestJS**, en utilisant **GraphQL** pour les requêtes/mutations et **RabbitMQ** pour la gestion asynchrone des messages. Les messages sont stockés en base de données via **Prisma**, puis publiés en temps réel grâce aux **subscriptions GraphQL**. Le frontend, développé en **React avec TypeScript**, utilise **Apollo Client** pour interagir avec l’API GraphQL et recevoir les messages instantanément via WebSocket.

Ce projet m’a permis de renforcer mes compétences en développement full-stack, en travaillant sur une architecture moderne orientée microservices et évènements. Il a aussi mis en avant l'importance de la coordination en équipe pour développer un système complet et robuste, de l’authentification JWT jusqu’à la gestion des états côté client.


Vous pouvez consulter l'intégralité du projet sur ce repertoire <a href="https://github.com/gyom2003 efrei-projet-web">Github</a>.
