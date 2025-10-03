Projet MIRO – Bilan et Perspectives
1. Travail réalisé
Architecture matérielle définie
Utilisation de trois cartes Arduino Mega (gestion moteurs, capteurs ultrasons, joysticks).
Intégration du RPLidar pour la cartographie et la détection des obstacles.
Mise en place de capteurs ultrasoniques (12 au total) pour compléter la perception.
Gestion des moteurs pas à pas NEMA avec drivers TB6600 validée.
Développement logiciel
Code Arduino pour les moteurs (Arduino_1) fonctionnel avec trames de commande.
Code Arduino pour les capteurs ultrasons (Arduino_2) retournant les distances.
Code Arduino pour les joysticks et boutons (Arduino_3) permettant de générer des trames de déplacement et des réponses ("oui"/"non").
Début du runtime Python sur Mac :
Communication série avec les trois cartes Arduino.
Gestion des trames moteur et capteurs.
Intégration d’un module d’arrêt automatique si un obstacle est détecté.
Tests et validations
Vérification du câblage et fonctionnement des moteurs.
Test des capteurs ultrasons individuellement et en séquence.
Mise au point du protocole de trames série (moteurs, capteurs, joysticks).
Intégration progressive de la logique “arrêt si obstacle < 10 cm”.
Documentation et organisation
Définition de la structure du projet (répertoires Python/Arduino).
Création d’un dépôt GitHub (atoucam/Miro).
Rédaction de documents explicatifs (codes Arduino, runtime Python, protocole de mise sous tension).
2. Travail à venir
Amélioration du logiciel de navigation
Finaliser le module Python d’orchestration (fusion lidar + ultrasons).
Développer la logique de contournement automatique :
arrêt → analyse gauche/droite → reprise trajectoire libre.
Gestion des exceptions et robustesse du protocole série (ACK, watchdog).
Intégration complète du Lidar
Exploiter les trames en temps réel pour autoriser ou refuser un déplacement.
Filtrer les obstacles “hauts” pertinents pour un guidage en intérieur.
Interaction utilisateur
Intégrer Whisper + ChatGPT pour la commande vocale et le dialogue.
Utiliser la synthèse vocale du Mac pour restituer les réponses.
Prendre en compte les boutons du guidon pour des réponses simples (oui/non).
Fonctionnalités avancées
Ajout de la gestion inertielle via IMU pour fiabiliser la navigation.
Amélioration de la sécurité : gestion des distances de sécurité variables selon la vitesse.
Préparation d’une version extérieure (roues plus grandes, moteurs DC avec encodeurs).
Documentation et diffusion
Poursuivre la rédaction des guides techniques (codes Arduino, Python, mise sous tension).
Rédiger une documentation utilisateur pour les tests réels.
Développer un site vitrine du projet MIRO pour communication externe.

