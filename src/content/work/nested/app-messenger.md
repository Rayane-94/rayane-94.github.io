---
title: Application style Messenger 
publishDate: 2025-03-04 00:00:00
img: /assets/messenger.svg.webp
img_alt: image morpion 
description: |
  Application de messagerie en temps réel développée en équipe, avec React, NestJS, RabbitMQ et GraphQL.
tags:
  - React
  - NestJS
  - GraphQL

---

Ce projet a été réalisé dans le cadre d’un travail de groupe à 3 personnes. Il s’agit d’une application de messagerie en temps réel, inspirée de Messenger, qui permet à des utilisateurs de s’inscrire, se connecter, créer des conversations à deux et s’envoyer des messages instantanément.

Nous avons conçu le backend avec NestJS, en utilisant GraphQL pour les requêtes et mutations, ainsi que RabbitMQ pour la gestion asynchrone des messages. Les messages sont stockés dans une base de données via Prisma, puis diffusés en temps réel grâce aux subscriptions GraphQL.

Le frontend, développé en React avec TypeScript, utilise Apollo Client pour interagir avec l’API GraphQL et recevoir les messages instantanément via WebSocket.

Ce projet web, réalisé en groupe en fin d’année sur un peu plus d’une semaine, m’a permis de consolider mes compétences en développement full-stack en mettant en pratique la majorité des technologies vues en cours à l’EFREI. Il m’a également permis de progresser en collaboration d’équipe, en participant activement à la conception d’une application moderne, fonctionnelle et bien structurée.


Vous pouvez consulter l'intégralité du projet sur ce repertoire <a href="https://github.com/gyom2003 efrei-projet-web">Github</a>.
