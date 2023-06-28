---
title: OpenVas
publishDate: 2019-12-01 00:00:00
img: /assets/openvas.jpg
img_alt: Openvas
description: |
  Scan de vulnérabilité 
tags:
  - OpenVas
  - Python
  - Wordpress
  - Automatisation
  - Email
---

OpenVAS est basé sur une architecture client-serveur et comprend plusieurs composants, tels que le scanner de vulnérabilité, le gestionnaire de tâches, la base de données de vulnérabilités et l'interface utilisateur. Il utilise une base de données de plugins contenant des milliers de tests de sécurité pour identifier les faiblesses potentielles dans les systèmes analysés.

Les utilisateurs peuvent configurer des scans de vulnérabilité en spécifiant les cibles à analyser et en sélectionnant les plugins à utiliser. Une fois le scan terminé, OpenVAS génère un rapport détaillé indiquant les vulnérabilités détectées, leur gravité et des recommandations pour les corriger.

OpenVAS est largement utilisé dans le domaine de la sécurité informatique, tant par les professionnels de la sécurité que par les administrateurs système. Il est apprécié pour sa flexibilité, sa extensibilité et sa capacité à identifier un large éventail de vulnérabilités courantes.

Script Python qui utilise le module python-gvm pour automatiser le scan avec OpenVAS, et envoie un e-mail si WordPress est infecté.

Ce script se connecte au gestionnaire OpenVAS via le fichier socket, s'authentifie, crée une tâche de scan pour une cible spécifiée, lance le scan, attend que le scan soit terminé, récupère le rapport généré et l'affiche. 