---
title: Pojet IOT
publishDate: 06-01-2023 00:00:00
img: /assets/IOT.PNG
img_alt: Dashboard
description: |
  Cette application Flask a pour but de recevoir des données provenant de capteurs d'humidité et de température via des requêtes HTTP POST, puis écrit ces données dans une base de données InfluxDB.
tags:
  - Python
  - Capteur
  - API
---

# Capteurs d'humidité et de température

Application Flask qui permet de recevoir des données de capteurs d'humidité et de température via des requêtes HTTP POST, puis de les écrire dans une base de données InfluxDB.

## Routes de l'API

Cette route est utilisée pour recevoir les données d'humidité des capteurs.

- Méthode HTTP : POST
- URL : `/api/humidity`

Le traitement des données se fait comme suit :

1. Récupérer les données de la requête via `request.data`.
2. Extraire la valeur de la charge utile (payload) des données reçues.
3. Convertir la charge utile de l'héxadécimal en décimal.
4. Diviser la valeur obtenue par 10 pour obtenir la valeur réelle de l'humidité.
5. Appeler la fonction `writes` pour écrire les données d'humidité dans la base de données InfluxDB.
6. Retourner les données de la requête.


Cette route est utilisée pour recevoir les données de température des capteurs.

- Méthode HTTP : POST
- URL : `/api/temperature`

Le traitement des données est similaire à celui de la route `/api/humidity`, mais concerne les données de température.

## Fonction `writes`

La fonction `writes` est utilisée pour écrire les données dans la base de données InfluxDB.

- Paramètres :
  - `name` : Le nom de la mesure (humidité ou température).
  - `value` : La valeur de la mesure.

Les étapes de la fonction sont les suivantes :

1. Définition des détails de connexion à InfluxDB (URL, jeton, organisation).
2. Création d'un client InfluxDB et d'une API d'écriture en utilisant les détails de connexion.
3. Création d'un point de données avec le nom et la valeur fournis.
4. Utilisation de l'API d'écriture pour écrire le point de données dans la base de données.

---
## Conclusion

En utilisant ce code, vous pouvez mettre en place un service web qui collecte et enregistre les données provenant de capteurs d'humidité et de température dans une base de données InfluxDB. Cela vous permet de stocker ces données et de les analyser ultérieurement.

---