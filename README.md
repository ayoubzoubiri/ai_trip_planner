# 🌍 AI Trip Planner

<div align="center">

**Plan smarter, travel farther.**  
*Toplago.com — The next-gen AI-powered itinerary generator.*

[![Status](https://img.shields.io/badge/Status-Work_In_Progress-orange?style=for-the-badge)](https://github.com/ayoubzoubiri)
[![Frontend-link](https://img.shields.io/badge/Frontend-React_18-blue?style=for-the-badge&logo=react)](https://github.com/ayoubzoubiri/tpf)
[![Backend-link](https://img.shields.io/badge/Backend-Laravel_10-red?style=for-the-badge&logo=laravel)](https://github.com/ayoubzoubiri/tpb)

</div>

---

## 🚀 **Quick Access**

| 🖥️ **Frontend Repository** | ⚙️ **Backend Repository** |
| :---: | :---: |
| [**Explore the React Client**](https://github.com/ayoubzoubiri/tpf) | [**Explore the Laravel API**](https://github.com/ayoubzoubiri/tpb) |
| *Vite, TailwindCSS, Redux* | *Laravel 10, MySQL, Gemini AI* |

---

## 📖 Short Description

**AI Trip Planner** is an innovative full-stack application designed to take the hassle out of travel planning. By leveraging **Gemini Pro** for intelligence and **Viator** for real-world data, it generates personalized, bookable itineraries in seconds.

### 💡 Why this project?
-   **The Problem:** Planning a trip requires visiting dozens of sites for flights, hotels, activities, and reviews.
-   **The Solution:** A centralized hub that generates a complete plan, suggests top-rated activities, and allows for easy customization.

---

## 📋 Cahier des Charges (Résumé)

### 1. Avant-propos
-   **Description:** Plateforme pour créer automatiquement un itinéraire via Gemini, suggestions d'activités via Viator et TripAdvisor, et gestion d'un blog.
-   **Objectif:** Générer des itinéraires personnalisés, proposer des activités populaires et fiables, permettre sauvegarde/édition, et fournir un blog manuel.

### 2. Prérequis
-   Connaissance du web
-   Compte utilisateur
-   **Clés API:** Gemini, Viator

### 3. Type de site
-   Application web full-stack: planificateur IA, recommandations d'activités, avis, plans de voyage et blog.

### 4. Ciblage
-   **Utilisateurs:** Voyageurs (planifier rapidement), créateurs de contenu (gérer blog), admin (superviser plateforme).

### 5. Création & Design
-   Interface moderne et responsive
-   Maquettes Figma (desktop + mobile)
-   Composants réutilisables: cards, boutons, formulaires

### 6. Pages principales
-   Accueil
-   Planificateur IA
-   Activités (Viator)
-   Fiche activité
-   Mes plans de voyage (CRUD)
-   Blog (liste + article CRUD)
-   Auth: Connexion / Inscription
-   Profil utilisateur

---

## 🛠️ Fonctionnalités principales

-   **🤖 Planificateur IA:** Génération d'itinéraire selon destination, dates, budget, style (résultat éditable).
-   **🌟 Recommandations d'activités:** Intégration Viator (prix, images, catégories).
-   **📂 Gestion plans de voyage:** CRUD complet pour vos itinéraires.
-   **✍️ Blog manuel:** CRUD avec champs titre, contenu, image, catégorie, meta description.
-   **🔍 Extra:** Recherche, partage d'itinéraire, mode sombre.

---

## 🏗️ Architecture Technique

-   **Backend:** Laravel 10 (API, auth, business logic)
-   **Frontend:** React 18 + Vite + TailwindCSS
-   **State:** Redux Toolkit
-   **DB:** MySQL
-   **External APIs:** Gemini, Viator
-   **Auth:** Laravel Breeze + Sanctum
-   **Docker:** Containers for frontend, backend, mysql

### Backend (Laravel) Details
> [Repository Link](https://github.com/ayoubzoubiri/tpb)
-   **Models:** `User`, `Trip`, `DayPlan`, `Activity`, `BlogPost`
-   **Key Endpoints:**
    -   `POST /api/itinerary/generate` — Generate itinerary via Gemini
    -   `GET /api/activities` — List activities (Viator)
    -   `CRUD /api/trips` — Manage saved trips
    -   `CRUD /api/blog` — Manage blog posts

### Frontend (React) Details
> [Repository Link](https://github.com/ayoubzoubiri/tpf)
-   **Router:** React Router
-   **State:** Redux Toolkit
-   **Styling:** TailwindCSS
-   **API calls:** Axios

---

## 🎨 Diagrammes & Maquettes

-   **Diagrams:** [links](https://lucid.app/lucidchart/3d3d891f-0f23-4058-9c76-7317384497f3/edit?viewport_loc=-378%2C366%2C2577%2C986%2C0_0&invitationId=inv_443ee6c0-76f8-4d47-916c-36f69aa6c68b),
-   **Jira Board:** [Planning](https://ayz.atlassian.net/jira/software/projects/TPLG/boards/168/backlog?atlOrigin=eyJpIjoiMzE3Yzk0ODBlNDViNDc4NmFjZmE3YTM5NGQ5NGVkYTgiLCJwIjoiaiJ9)

---

## ⚡ Quick Start (Development)

**Prerequisites:** Docker/Desktop OR PHP 8.1+, Composer, Node 18+, MySQL.

### 🐳 Using Docker (Recommended)
```powershell
docker compose up --build
```

### 💻 Manual Setup (Local Dev)

**Backend Setup**
```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
```

**Frontend Setup**
```bash
cd frontend
npm install
npm run dev
```

## Environment & API keys

-   **Backend:** set `.env` variables for `DB_*`, `APP_KEY`, `GEMINI_API_KEY`, `VIATOR_API_KEY`, `TRIPADVISOR_API_KEY` and other provider secrets.
-   **Frontend:** set `VITE_API_URL` and any client keys (only safe, public keys) in `.env`.
