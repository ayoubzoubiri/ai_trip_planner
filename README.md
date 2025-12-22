# ai_trip_planner

Welcome to **ai_trip_planner** — Toplago.com planification de voyage (AI-powered trip planner).

Badges:

-   **Status**: WIP
-   **Tech**: Laravel 10 · React 18 · TailwindCSS · MySQL · Docker

## Short description

`ai_trip_planner` is a full-stack web application that generates personalized travel itineraries using Gemini Pro, suggests activities via Viator , and includes a manual blog for SEO and content management. The app centralizes discovery, recommendations and planning to save travelers time.

## Why this project?

-   Problem: Travelers visit multiple sites to discover activities, read reviews and plan trips. That is fragmented and time-consuming.
-   Solution: Centralized AI itinerary generation + curated activity suggestions and reviews + blog for SEO.

## Cahier des Charges (Résumé)

1. Avant-propos

-   Description: Plateforme pour créer automatiquement un itinéraire via Gemini, suggestions d'activités via Viator et TripAdvisor, et gestion d'un blog.
-   Objectif: Générer des itinéraires personnalisés, proposer des activités populaires et fiables, permettre sauvegarde/édition, et fournir un blog manuel.

2. Prérequis

-   Connaissance du web
-   Compte utilisateur
-   Clés API: Gemini, Viator

3. Type de site

-   Application web full-stack: planificateur IA, recommandations d'activités, avis, plans de voyage et blog.

4. Ciblage

-   Utilisateurs: voyageurs (planifier rapidement), créateurs de contenu (gérer blog), admin (superviser plateforme).

5. Création & Design

-   Interface moderne et responsive
-   Maquettes Figma (desktop + mobile)
-   Composants réutilisables: cards, boutons, formulaires

6. Pages principales

-   Accueil
-   Planificateur IA
-   Activités (Viator )
-   Fiche activité
-   Mes plans de voyage (CRUD)
-   Blog (liste + article CRUD)
-   Auth: Connexion / Inscription
-   Profil utilisateur

## Fonctionnalités principales

-   Planificateur IA: génération d'itinéraire selon destination, dates, budget, style; résultat éditable
-   Recommandations d'activités: Viator (prix, images, catégories)
-   Gestion plans de voyage (CRUD)
-   Blog manuel (CRUD) avec champs titre, contenu, image, catégorie, meta description
-   Recherche, partage d'itinéraire, mode sombre (features secondaires)

## Architecture Technique

-   Backend: Laravel 10 (API, auth, business logic)
-   Frontend: React 18 + Vite + TailwindCSS
-   State: Redux Toolkit
-   DB: MySQL
-   External APIs: Gemini, Viator
-   Auth: Laravel Breeze + Sanctum
-   Docker: containers for frontend, backend, mysql

## Diagrammes & Maquettes & planification

-   Diagrams to produce: https://app.eraser.io/workspace/EFYrU8xK0X5Y02jjY4IK?origin=share
                         https://app.eraser.io/workspace/0n7w5Tk8eHtoPGVjJhmi?origin=share
-   Figma (Design mockups - Desktop & Mobile): 
-   Planification jira: https://ayz.atlassian.net/jira/software/projects/TPLG/boards/168/backlog?atlOrigin=eyJpIjoiMzE3Yzk0ODBlNDViNDc4NmFjZmE3YTM5NGQ5NGVkYTgiLCJwIjoiaiJ9


## Backend (Laravel) — Important models & endpoints
-   https://github.com/ayoubzoubiri/tpf
-   Models: `User`, `Trip`, `DayPlan`, `Activity`, `BlogPost`
-   Key API endpoints (examples):
    -   `POST /api/itinerary/generate` — generate itinerary via Gemini
    -   `GET /api/activities` — list activities (Viator )
    -   `CRUD /api/trips` — manage saved trips
    -   `CRUD /api/blog` — manage blog posts

## Frontend (React) — important notes
-   https://github.com/ayoubzoubiri/tpb
-   Router: React Router
-   State: Redux Toolkit
-   Styling: TailwindCSS
-   API calls: Axios
-   Setup with Vite

## Environment & API keys

-   Backend: set `.env` variables for `DB_*`, `APP_KEY`, `GEMINI_API_KEY`, `VIATOR_API_KEY`, `TRIPADVISOR_API_KEY` and other provider secrets.
-   Frontend: set `VITE_API_URL` and any client keys (only safe, public keys) in `.env`.

## Quick Start (development)

Prerequisites: Docker/Desktop or PHP 8.1+, Composer, Node 18+, npm/yarn, MySQL.

Using Docker (recommended):

```powershell
# from repo root
docker compose up --build
```

Without Docker (local dev):

```powershell
# Backend
cd backend_or_repo_root
composer install; cp .env.example .env; php artisan key:generate; php artisan migrate

# Frontend
cd frontend_or_repo_root
npm install; npm run dev
```





