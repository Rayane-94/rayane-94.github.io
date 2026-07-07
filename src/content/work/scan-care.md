---
title: Scan Care — Rappel de médicaments par scan d'ordonnance
publishDate: 2026-01-23 00:00:00
img: /assets/scancare-logo.png
img_alt: Scan Care, application mobile de rappel de médicaments par scan d'ordonnance
description: |
  Application mobile qui scanne une ordonnance médicale et notifie l'utilisateur pour ne pas oublier son traitement, grâce à l'OCR et une IA.
tags:
  - React Native
  - TypeScript
  - Expo
  - IA / OCR (Mistral)
  - Firebase
order: 2
---

## Ne plus jamais oublier de prendre son traitement

> Contexte

Scan Care part d'un problème simple et universel : on oublie de prendre ses médicaments, ou on ne comprend pas toujours bien une ordonnance manuscrite. L'application permet de prendre en photo son ordonnance et se charge automatiquement d'identifier les médicaments prescrits, leur fréquence, et de programmer des rappels de prise adaptés.

> Ma contribution : le cœur technique du projet

C'est le projet de groupe sur lequel j'ai eu la responsabilité de la partie la plus critique : le **pipeline de reconnaissance**. Concrètement, j'ai développé la prise de photo de l'ordonnance et l'upload du fichier, l'appel à l'API de l'IA **Mistral** pour interpréter le contenu du document, le passage par OCR pour extraire le texte brut, puis un script de **matching** qui compare le texte détecté (souvent imparfait) à une base de référence de médicaments afin d'identifier avec fiabilité de quel médicament il s'agit malgré les éventuelles erreurs de lecture. Le tout renvoie une réponse structurée en JSON exploitée ensuite par l'app. J'ai aussi participé à une passe de refactorisation de ce pipeline ainsi qu'à une partie du frontend React Native.

Le reste de l'équipe a travaillé sur l'authentification (Firebase), la gestion des rappels/notifications et une partie de l'interface.

> Stack technique

- **Frontend mobile** : React Native, Expo, TypeScript, React Navigation
- **IA / OCR** : API Mistral AI
- **Backend** : Firebase (authentification, stockage)

Vous pouvez consulter le projet sur <a href="https://github.com/armanceau/scan-care">Github</a>
