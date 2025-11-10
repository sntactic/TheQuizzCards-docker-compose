# TheQuizzCards-docker-compose
🧠 QuizzCards — Plateforme de création et partage de cartes de quiz culture générale
Une application web complète pour créer, partager et explorer des cartes de quiz de culture générale. Développée avec Angular, Spring Boot, MongoDB, Spring Security (JWT + OAuth2 Google) et Spring AI.

🚀 Aperçu du projet
QuizzCards est une plateforme interactive où les utilisateurs peuvent :
* ✏️ Créer leurs propres cartes de quiz (question + réponse)
* 🌍 Partager leurs cartes avec la communauté
* 🔒 Choisir si leurs cartes sont publiques ou privées
* 👁️ Explorer les cartes publiques des autres utilisateurs
* ⚙️ Modifier / Supprimer leurs cartes à tout moment
* 🧑‍💼 Espace administrateur : modération des cartes signalées (propos injurieux, fausses infos…)
L’objectif du projet est d’offrir une expérience ludique et éducative, tout en expérimentant une architecture logicielle complète (front + back + sécurité + microservice IA).

🧩 Stack technique
🎨 Frontend — Angular
* Framework : Angular 17
* Authentification JWT + OAuth2 (Google)
* Gestion des rôles (utilisateur / admin)
* UI responsive et dynamique
* Communication avec l’API Spring Boot via HttpClient

⚙️ Backend principal — Spring Boot
* Framework : Spring Boot 3+
* Sécurité : Spring Security (Basic Auth + JWT + OAuth2 Google)
* Base de données : MongoDB 
* CRUD complet pour les cartes et utilisateurs
* Gestion des rôles (USER / ADMIN)
* API RESTful bien structurée (architecture en couches)
* Spring AI pour générer automatiquement des réponses aux questions de quiz (utilisant l’API de Groq)

🐳 Déploiement — Docker / Docker Compose
* Conteneurisation du front, du back et de la base de données
* Communication entre services via Docker network
* Variables d’environnement sécurisées
* Un seul déploiement via :  docker compose up -d
* Et aller sur http://localhost 

🔐 Authentification et rôles
* JWT : connexion classique (email + mot de passe)
* OAuth2 Google : connexion via compte Google
* Rôles :
    * USER → accès standard (créer / modifier / supprimer ses cartes)
    * ADMIN → accès total à toutes les cartes + modération

🧠 Fonctionnalité bonus — IA générative
Lors de la création d’une carte, si l’utilisateur ne connaît pas la réponse, le système peut générer automatiquement la réponse grâce à une intégration de GroqAI.
