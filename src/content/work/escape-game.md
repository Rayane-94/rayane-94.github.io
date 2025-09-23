---
title: Escape Game
publishDate: 2020-03-02 00:00:00
img: /assets/escapegame.png
img_alt: Iridescent ripples of a bright blue and pink liquid
description: |
 Dans ce projet, j'ai développé une interface Web permettant aux administrateurs de gérer un Escape Game de manière automatique, manuelle ou via des scénarios aléatoires.
tags:
  - HTML / CSS
  - JS
  - PHP

                  
  
---

## Projet de BTS SNIR 

> Contexte

Pendant mon BTS SNIR au Lycée Louis Armand, j'ai travaillé sur un projet d'Escape Game en partenariat avec la Marine Nationale et leur nouveau bateau, Antares. Les étudiants en Bac Pro étaient responsables de l'installation physique et du soudage pour les missions du jeu, ainsi que du scripting en Python pour chacune des tâches. 

Leurs responsabilités comprenaient la conception et la mise en place de la salle de jeu ainsi que des différentes missions, telles que les postes de commandement et de communication, le coffre et les scénarios d'avarie.

Le problème initial de ce projet était que les missions se lançaient de manière indépendante, sans contrôle à distance possible. Les programmes ne se lançaient que lorsque le compilateur était branché à la Raspberry Pi située à côté des missions. 

Cela signifiait qu'une personne devait être présente pour chaque mission, empêchant les joueurs de profiter pleinement du jeu. 

> Ma Contribution au Projet

Ma partie dans ce projet consistait à développer l'interface web de l'Escape Game. Cela incluait la création des systèmes de connexion, de création d'équipe et de gestion des missions en fonction du mode choisi (automatique, manuel ou un scénario aléatoire). Cette interface permet aux administrateurs de contrôler le jeu de manière fluide et de l'adapter en temps réel pour améliorer l'expérience des joueurs. Pour assurer un environnement de développement efficace, j'ai utilisé VirtualBox comme machine virtuelle, ce qui m'a permis de tester et de déployer l'interface web de manière sécurisée et isolée.

Vous pouver consulter l'integralité du code sur <a href="https://github.com/Rayane-94/Projet-Escape-Game">Github</a>.


> Description des Missions

L'Escape Game est composé de six missions principales, chacune dépendante des autres, et de deux missions supplémentaires d'avarie qui peuvent être activées à tout moment si les joueurs progressent trop rapidement.

Les missions se déroulent dans l'ordre suivant :

1. Déverrouiller le pupitre de commande

2. Poste de commandement

3. Coffre  

4. Brouilleur

5. Défis 

6. Avarie (si besoin pour retarder les joueurs)

Comme vous pouvez le constater dans l'image ci-dessus, les missions suivent un ordre précis. La numérotation met en évidence la progression à travers les différents postes au fil du temps. La première mission concerne le pupitre de commande, tandis que la sixième est dédiée aux scénarios d'avarie.

> Répartition des Tâches

Ce projet était réalisé en groupe de 3. Ma partie consistait à développer l'interface Web, un autre membre de l'équipe était chargé de développer l'API REST en PHP, et le troisième membre modifiait les scripts Python des Raspberry Pi pour implémenter des scénarios aléatoires.

Durant ce projet concret, j'ai pu mettre en application les notions apprises dans mon BTS et je suis fier que l'interface ait plu aux responsables de l'Escape Game et a mes professeurs. Elle a permis de gérer le jeu efficacement a distance et de faire participer les étudiants du lycée.

