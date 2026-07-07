---
title: JobAlign — Analyse CV / offre d'emploi par IA locale
publishDate: 2026-05-27 00:00:00
img: /assets/job-align-logo.jpeg
img_alt: JobAlign, analyseur de CV et d'offres d'emploi propulsé par une IA locale
description: |
  Analyseur de CV et d'offres d'emploi propulsé par une IA locale, avec score de correspondance et génération de lettre de motivation.
tags:
  - Python / FastAPI
  - IA locale (Ollama)
  - TypeScript
---

## Faire matcher un CV avec une offre, sans dépendre d'une API externe

> Contexte

JobAlign est un projet de groupe qui répond à un besoin très concret : savoir à quel point son CV correspond réellement à une offre d'emploi avant de postuler. L'originalité du projet est de faire tourner l'intelligence artificielle **entièrement en local** via Ollama, sans envoyer de données à une API tierce (confidentialité du CV oblige) : extraction du texte du CV et de l'offre au format PDF, analyse NLP pour identifier compétences techniques, soft skills et expériences, puis calcul d'une similarité sémantique par embeddings entre les deux documents.

> Ma contribution

Sur ce projet réalisé à 3, ma contribution s'est concentrée sur deux points précis : la **génération automatique de lettre de motivation** (à partir du LLM local, en s'appuyant sur l'analyse de matching déjà calculée entre le CV et l'offre, pour produire une lettre argumentée et personnalisée), et une partie du **frontend** (TypeScript/Vite) qui permet d'uploader ses documents et de visualiser les résultats d'analyse.

Le reste de l'équipe a construit : l'API FastAPI, l'extraction PDF, le NLP (spaCy) et le calcul d'embeddings/similarité (sentence-transformers).

> Stack technique

- **Backend** : Python, FastAPI
- **IA** : Ollama (LLM local)
- **Frontend** : TypeScript, Vite
- **Déploiement** : Docker / Docker Compose

Vous pouvez consulter le projet sur <a href="https://github.com/armanceau/JobAlign">Github</a>
