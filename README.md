#  GreenHand

> Application d'agriculture pensée pour aider les débutants à mieux comprendre, suivre et gérer leurs cultures, avec un chatbot intelligent intégré.

![Repo parent](https://img.shields.io/badge/monorepo-parent-2f855a?style=for-the-badge)
![Frontend](https://img.shields.io/badge/frontend-Expo%20%7C%20React%20Native-0f172a?style=for-the-badge)
![Backend](https://img.shields.io/badge/backend-Node.js%20%7C%20Express%20%7C%20TypeScript-1d4ed8?style=for-the-badge)
![Database](https://img.shields.io/badge/database-MongoDB-15803d?style=for-the-badge)
![AI](https://img.shields.io/badge/AI-Gemini%20%7C%20Recommandations-7c3aed?style=for-the-badge)

## À propos

**GreenHand** est une solution mobile orientée agriculture qui accompagne les utilisateurs débutants dans leurs premières décisions de culture.  
Le projet combine :

- une **application mobile** pour le suivi des plantes et des données utiles au quotidien ;
- un **backend sécurisé** pour l'authentification, l'inventaire, les profils et les recommandations ;
- un **chatbot agricole** capable de répondre en français avec des conseils simples et pratiques.

Ce dépôt est le **dépôt parent** du projet et centralise les deux sous-projets :

- [`GreenHand_frontend`](https://github.com/Andylamothe/GreenHand_frontend)
- [`GreenHand_backend`](https://github.com/Andylamothe/GreenHand_backend)

## Fonctionnalités principales

###  Accompagnement des débutants
- interface mobile accessible ;
- conseils pratiques pour l'entretien des cultures ;
- aide à la compréhension des besoins des plantes.

###  Chatbot agricole
- assistant conversationnel intégré dans l'application ;
- réponses orientées agriculture et jardinage ;
- recommandations enregistrables côté backend ;
- génération de réponses via **Google Gemini**.

###  Données météo et tableaux de bord
- affichage des conditions météo ;
- visualisation de l'humidité, des précipitations, de la température et du vent ;
- tableaux de bord dédiés à l'analyse des cultures.

###  Gestion des plantes et de l'inventaire
- ajout, recherche et suppression de plantes ;
- filtrage par catégories ;
- consultation de détails sur les plantes ;
- suivi d'un inventaire agricole personnel.

###  Gestion utilisateur
- inscription et connexion ;
- profil utilisateur ;
- paramètres de compte ;
- base d'administration et gestion des accès.

###  Fonctions mobiles natives
- accès à l'appareil photo ;
- sélection depuis la galerie ;
- expérience adaptée à une application mobile Expo / React Native.

## Architecture du projet

```text
Greenhand/
├── GreenHand_frontend/   # Application mobile Expo / React Native
├── GreenHand_backend/    # API REST Node.js / Express / TypeScript
└── README.md             # Présentation globale du projet
```

## Stack technique

### Frontend
`Expo` `React Native` `React` `JavaScript` `AsyncStorage` `Axios` `React Native Chart Kit` `React Navigation` `Lottie` `Lucide Icons`

### Backend
`Node.js` `Express` `TypeScript` `MongoDB` `Mongoose` `JWT` `Zod` `Swagger` `Winston` `Jest`

### IA & services
`Google Gemini` `Open-Meteo / Weather API` `REST API`

## Sous-projets

### 1. GreenHand Frontend
Application mobile construite avec **Expo / React Native**.

Fonctions visibles dans le frontend :
- écran d'accueil avec météo ;
- chatbot **GreenBot** ;
- dashboard météo ;
- dashboard plantes ;
- inventaire ;
- authentification ;
- profil, notifications et support.

Lien : https://github.com/Andylamothe/GreenHand_frontend

### 2. GreenHand Backend
API REST construite avec **Node.js, Express et TypeScript**.

Responsabilités principales :
- authentification ;
- gestion utilisateurs ;
- gestion de l'inventaire ;
- catégories et plantes ;
- recommandations IA sauvegardées ;
- documentation API Swagger ;
- configuration sécurité (CORS, rate limiting, JWT).

Lien : https://github.com/Andylamothe/GreenHand_backend

## Installation

### Prérequis

- `Git`
- `Node.js`
- `npm`
- `Expo CLI` / environnement Expo
- une instance `MongoDB` pour le backend

### Cloner le dépôt parent

```bash
git clone https://github.com/Andylamothe/Greenhand.git
cd Greenhand
git submodule update --init --recursive
```

## Lancement du projet

### Frontend

```bash
cd GreenHand_frontend
npm install
npm start
```

### Backend

```bash
cd GreenHand_backend
npm install
cp .env.example .env
npm run dev
```

## Variables d'environnement

### Frontend
Le chatbot utilise une clé d'environnement Expo pour Gemini :

- `EXPO_PUBLIC_GEMINI_API_KEY`

### Backend
Exemples de variables attendues :

- `MONGO_URI`
- `JWT_SECRET`
- `JWT_EXPIRES_IN`
- `CORS_ORIGINS`
- `HTTP_PORT`
- `HTTPS_PORT`

Voir le template : [`GreenHand_backend/.env.example`](https://github.com/Andylamothe/GreenHand_backend/blob/main/.env.example)

## Documentation API

Le backend expose une documentation Swagger.

- URL locale attendue : `http://localhost:3000/api/docs`

## Pourquoi GreenHand ?

GreenHand vise à rendre l'agriculture plus accessible en proposant une expérience claire, moderne et pédagogique.  
Le projet s'adresse particulièrement aux personnes qui débutent et qui ont besoin :

- d'un point d'entrée simple ;
- d'indicateurs météo utiles ;
- d'un suivi de leurs plantes ;
- d'une assistance instantanée grâce au chatbot.

## Dépôts liés

- Parent repo : https://github.com/Andylamothe/Greenhand
- Frontend : https://github.com/Andylamothe/GreenHand_frontend
- Backend : https://github.com/Andylamothe/GreenHand_backend

## Contribution

Les contributions sont les bienvenues.

1. Forker le projet
2. Créer une branche
3. Proposer vos changements
4. Ouvrir une pull request claire et descriptive

## Statut

Projet en cours d'évolution, avec une base solide autour de :
- l'accompagnement agricole des débutants ;
- la visualisation de données ;
- l'assistance intelligente via chatbot ;
- l'architecture mobile + API.
