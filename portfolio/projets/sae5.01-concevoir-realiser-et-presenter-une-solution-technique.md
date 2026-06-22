# SAE5.01 Concevoir, réaliser et présenter une solution technique

par [Kylian Adam](../)

## Contexte

Les systèmes embarqués sont utiles pour fournir une solution sur mesure à un besoin. Le professionnel R\&T est capable de collaborer, en utilisant les pratiques de gestion de projets, pour la mise en place des moyens de communications nécessaires à la solution (Radio, GSM, Wi‑Fi, GPS, ...), les implémenter dans le code et documenter son travail. Nous espérons balayer tous ces points en groupe, en concevant un traqueur pour véhicule.

## Consigne

Utiliser un module Pycom afin de transmettre les données GPS d’un véhicule à travers le réseau LoRaWan de la plateforme publique The Things Network et de visualiser sa position sur une carte dans une page web. Pour garantir l'autonomie de la batterie, le système doit consommer peu tout en permettant le suivi lorsque c’est nécessaire. L'électronique embarquée doit être mise dans un mode « sleep ». Ce n’est que lorsque le véhicule se déplace que les communications se font, grâce à l’accéléromètre par son interruption dédiée. Le système sera remis en mode faible consommation par une action de l’utilisateur. Il sera aussi prévenu par SMS que la voiture se déplace.

## Image

[![](<../.gitbook/assets/download (4).php>)](/broken/pages/b0c17185fb9ace8b1651bb2fc0f732992c748852)

## Compétences acquises

* Automatiser l'envoi et la réception SMS
* Échanger des données LF, LoRa WAN
* Évaluer les infos de l'accéléromètre
* Visualiser un emplacement sur une carte
* Traiter des données brutes avec un Payload
* Utiliser l’interruption matérielle

## Ma réalisation

J'ai contribué à la réalisation d'une plateforme IoT complète de suivi GPS avec gestion intelligente de l'énergie. Concrètement :

* Implémentation sur la Pycom de l'acquisition GPS via le module L76GNSS avec gestion des tentatives de reconnexion et fallback sur une position en cache.
* Détection de mouvement via l'accéléromètre LIS2HH12 intégré au Pytrack avec interface vers le PIC MCU.
* Connectivité LoRaWAN/TTN en mode OTAA pour l'envoi des données de position et réception des commandes de contrôle.
* Configuration d'une alternative Wi‑Fi/MQTT pour les tests en environnement local.
* Intégration de payload formatters JavaScript côté TTN pour encoder/décoder les messages.
* Remplacement des boucles actives par un véritable système de deepsleep avec réveil par accéléromètre, réduisant la consommation de \~100 mA à \~1–5 mA en veille et multipliant l'autonomie batterie par 20–100×.
* Implémentation d'un système de heartbeat automatique toutes les 30 secondes pour maintenir la position à jour.
* Configuration du Raspberry Pi comme passerelle avec Mosquitto en tant que broker MQTT, Node‑RED pour l'orchestration des flux et l'UI (Worldmap, actions sleepmode, configuration numéro de téléphone), et intégration de Gammu pour l'envoi de notifications SMS via clé 2G/3G. Support des notifications Pushover ajouté.
* Documentation complète du projet, création d'une suite de tests automatisée et fourniture de scripts de déploiement automatisé incluant Docker Compose.
* Gestion de plusieurs modes d'opération : mode actif avec envois GPS fréquents, mode idle avec heartbeats périodiques en veille profonde, et mode downlink awaiting sur commande LoRa. Support complet de la persistance d'état entre réveils et sauvegarde automatique de la dernière position GPS pour les situations sans fix satellite.

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS — page 160](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf)

## Emplacement du dossier travail

Dépôt GitHub

{% embed url="https://github.com/kylian-iut/SAE5.01" %}
