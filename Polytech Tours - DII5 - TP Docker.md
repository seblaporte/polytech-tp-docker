![](logo_apside.png)
![](logo_polytech.png) 

# Polytech Tours - DII5 - TP Docker

## Introduction

- Durée du TP : 4h
- Image source imposée : `alpine`
- Application à déployer :
	* Langage : Node.JS
	* Sources : `https://github.com/seblaporte/polytech-tp-docker.git`
	* Description : API Rest permettant d'obtenir des informations sur un utilisateur et son mot de passe de connexion. Documentation de l'API disponible dans les sources, dossier `doc`.

## Informations sur l'application

L'API permet de récupérer des informations au moyen d'une base de données MySQL.

L'application est paramètrable au moyen de variables d'environnement :

- ENV : Si cette variable d'environnement a pour valeur `dev`, les logs permettent le debug de l'application.
- DB_HOST : Nom d'hôte de la base de données
- DB_USER : Nom d'utilisateur pour la connexion à la BDD
- DB_PASSWORD : Mot de passe pour la connexion à la BDD
- DB_DATABASE : Nom de la base pour la connexion à la BDD
- DB_PORT : Port TCP utilisé par l'application

## Objectif du TP

- Permettre le déploiement d'une API Node.JS et de sa base de données avec Docker
- Disposer d'un déploiement pour un poste de développeur et un déploiement de production
- Poste de développement : Modification du code source avec prise en compte à chaud des modifications dans le conteneur (voir [nodemon](https://github.com/remy/nodemon))
- Proposer une solution à la définition du mot de passe de la base de données (Ne doit pas être stocké dans les sources)

## Travail demandé

### Déploiement avec Docker

Dans cette première partie du TP, l'objectif __unique__ est de déployer l'application seulement avec l'API de Docker.

### Déploiement avec Docker-compose

En reprennant le travail de la partie 1, utiliser Docker-compose pour effectuer le déploiement. L'objectif reste simple : déployer l'application pour un déploiement en production.

### Création d'une version permettant 2 types de déploiement

Cette troisième partie du TP a pour objectif de créer une version pour Dockeriser le poste du développeur. Il doit être possible avec un même livrable, de déployer l'application en production mais aussi pour un poste de développeur.

### Bonus : Déploiement multi-instance

Utilisation du reverse-proxy Traefik pour permettre de démarrer plusieurs instances de l'application.

## Ressources

- Image officielle Alpine Linux : [https://hub.docker.com/_/alpine/](https://hub.docker.com/_/alpine/)
- Image officielle MySQL : [https://hub.docker.com/_/mysql/](https://hub.docker.com/_/mysql/)
- Image officielle Traefik : [https://hub.docker.com/_/traefik/](https://hub.docker.com/_/traefik/)
- Hot-reload Node.JS : [https://github.com/remy/nodemon](https://github.com/remy/nodemon)