---
title: JobAlign — Analyse CV / offre d'emploi par IA locale
publishDate: 2026-05-27 00:00:00
img: /assets/joballign-logo.svg
img_alt: JobAlign, analyseur de CV et d'offres d'emploi propulsé par une IA locale
description: |
  Outil qui compare un CV et une offre d'emploi grâce à une IA tournant en local (sans API externe), calcule un score de correspondance et propose des suggestions d'amélioration. Projet de groupe où j'ai développé la génération automatique de lettre de motivation ainsi qu'une partie du frontend.
tags:
  - Python / FastAPI
  - IA (LLM local)
  - Frontend TypeScript
---

## Faire matcher un CV avec une offre, sans dépendre d'une API externe

> Contexte

JobAlign est un projet de groupe qui répond à un besoin très concret : savoir à quel point son CV correspond réellement à une offre d'emploi avant de postuler. L'originalité du projet est de faire tourner l'intelligence artificielle **entièrement en local** via Ollama, sans envoyer de données à une API tierce (confidentialité du CV oblige) : extraction du texte du CV et de l'offre au format PDF, analyse NLP pour identifier compétences techniques, soft skills et expériences, puis calcul d'une similarité sémantique par embeddings entre les deux documents.

> Ma contribution

Sur ce projet réalisé à plusieurs, ma contribution s'est concentrée sur deux points précis : la **génération automatique de lettre de motivation** (à partir du LLM local, en s'appuyant sur l'analyse de matching déjà calculée entre le CV et l'offre, pour produire une lettre argumentée et personnalisée), et une partie du **frontend** (TypeScript/Vite) qui permet d'uploader ses documents et de visualiser les résultats d'analyse.

Le reste de l'équipe a construit le pipeline principal : l'API FastAPI, l'extraction PDF, le NLP (spaCy) et le calcul d'embeddings/similarité (sentence-transformers).

> Stack technique

- **Backend** : Python, FastAPI
- **IA** : Ollama (LLM local), spaCy (NLP), sentence-transformers (embeddings)
- **Frontend** : TypeScript, Vite
- **Déploiement** : Docker / Docker Compose

Vous pouvez consulter le projet sur <a href="https://github.com/armanceau/JobAlign">Github</a> (repo hébergé par un camarade de promo, ma contribution y est ciblée sur la lettre de motivation et le frontend).
