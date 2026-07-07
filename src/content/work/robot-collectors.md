---
title: Robot Collectors — Essaim de robots en Rust
publishDate: 2026-06-19 00:00:00
img: /assets/Animation.gif
img_alt: Simulation terminal en Rust d'un essaim de robots explorateurs et collecteurs
description: |
  Simulation temps réel en Rust d'un essaim de robots qui explorent une carte, communiquent et récoltent des ressources. J'ai pris en charge la logique de simulation et la concurrence.
tags:
  - Rust
  - Concurrence
  - Terminal UI (Ratatui)
---

## Un essaim de robots qui s'auto-organise

> Contexte

Ce projet a été réalisé en trinôme, dans la lignée d'un exercice type "Jeu de la Vie" mais appliqué à des agents autonomes plutôt qu'à des cellules. L'idée : simuler un essaim de robots qui explorent une carte inconnue, se transmettent des informations entre eux, puis vont collecter des ressources en fonction de ce qui a été découvert. Le tout s'affiche en temps réel dans un terminal.

> Ma contribution : la logique de simulation

Ma partie était le cœur du projet, à savoir toute la **logique de simulation et la synchronisation concurrente** entre les robots. Deux types de robots cohabitent : les *scouts*, qui explorent la carte de façon aléatoire pour découvrir les ressources, et les *collectors*, qui utilisent un parcours en largeur (BFS) pour aller récupérer les ressources signalées par les scouts.

Chaque robot tourne sur son propre thread (2 scouts, 2 collectors), coordonnés par un thread central via des canaux `mpsc` pour la communication asynchrone, et un état partagé protégé par `Arc<RwLock>` pour que plusieurs threads puissent lire/écrire la carte sans se marcher dessus. C'était l'occasion de vraiment manipuler les concepts de concurrence de Rust (ownership, borrow checker, synchronisation) sur un cas concret plutôt que sur un exercice isolé.

Le reste de l'équipe s'est occupé de la génération procédurale de la carte (bruit de Perlin pour placer obstacles et gisements de ressources de façon réaliste) et de l'interface terminal avec la librairie Ratatui, qui affiche la carte et les robots en temps réel avec un code couleur.

> Stack technique

- **Rust** 
- **Ratatui** pour le rendu terminal
- **mpsc channels** et **Arc\<RwLock\>** pour la concurrence
- **Bruit de Perlin** pour la génération de carte

Vous pouvez consulter le projet sur <a href="https://github.com/armanceau/robot-collectors">Github</a>
