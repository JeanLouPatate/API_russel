🌊 API Russell – Port de plaisance
📌 Description

Ce projet est une application Express.js connectée à une base de données MongoDB, permettant à la capitainerie du port de plaisance Russell de gérer les catways (appontements), les réservations et les utilisateurs.

L’application fournit :

Une API REST privée pour gérer les données.

Une interface frontend simple (React) pour interagir avec l’API.

Un système d’authentification pour sécuriser l’accès.

🚀 Fonctionnalités
🔹 Gestion des catways

Créer un catway

Lister tous les catways

Récupérer les détails d’un catway

Modifier l’état d’un catway

Supprimer un catway

🔹 Gestion des réservations

Créer une réservation

Lister toutes les réservations

Récupérer une réservation spécifique

Modifier une réservation

Supprimer une réservation

🔹 Gestion des utilisateurs

Créer un utilisateur

Lister tous les utilisateurs

Récupérer un utilisateur spécifique

Modifier un utilisateur

Supprimer un utilisateur

🔹 Authentification

POST /login : connexion

GET /logout : déconnexion

📂 Structure du projet
API_russel/
│── backend/            # API Express.js
│   ├── models/         # Schémas Mongoose (User, Catway, Reservation)
│   ├── routes/         # Routes Express
│   ├── controllers/    # Logique métier
│   └── server.js       # Point d’entrée du serveur
│
│── frontend/           # Application React
│   ├── src/
│   │   ├── pages/      # Pages (Login, Dashboard, CRUD)
│   │   ├── components/ # Composants réutilisables
│   │   └── App.js
│
│── catways.json        # Données d’exemple pour les catways
│── reservations.json   # Données d’exemple pour les réservations
│── README.md           # Documentation du projet

⚙️ Installation
1. Cloner le projet
git clone https://github.com/JeanLouPatate/API_russel.git
cd API_russel

2. Installer les dépendances

Backend :

cd backend
npm install


Frontend :

cd frontend
npm install

3. Lancer le projet

Backend (Express) :

npm start


Frontend (React) :

npm start

🗄️ Importer les données dans MongoDB

Assurez-vous que MongoDB est installé et accessible.
Importez les collections avec :

mongoimport --jsonArray --db port_russell --collection catways --file catways.json --drop
mongoimport --jsonArray --db port_russell --collection reservations --file reservations.json --drop

📖 Documentation API

Une documentation de l’API est disponible à la racine du projet (/api-docs) une fois le serveur lancé.

Exemples de routes :

GET /catways

POST /catways

GET /catways/:id/reservations

POST /users

POST /login

🌍 Déploiement

Le projet peut être déployé sur :

Render ou Railway (backend)

Vercel ou Netlify (frontend)

👤 Auteur

Projet réalisé par JeanLouPatate dans le cadre du module Développement Web Full Stack.
