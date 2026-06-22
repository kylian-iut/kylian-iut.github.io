# SAE3.02 Développer des applications communicantes

par [Kylian Adam](../)

## Contexte

Dans certains environnements, il est important de pouvoir faire circuler des données entre plusieurs machines ou utilisateurs, de manière fiable et organisée. Cela peut concerner des échanges en continu, des envois de fichiers, ou encore des interactions entre différents services d’un même réseau. Les outils existants ne répondent pas toujours précisément aux besoins, ce qui pousse parfois à créer des solutions sur mesure, capables de s’adapter aux contraintes techniques du système en place. Ce type de situation demande de maîtriser la manière dont les données sont envoyées, reçues, enregistrées, et consultées, tout en gardant un bon niveau de stabilité et de sécurité.

## Consigne

Développer une architecture multi-serveurs capable de traiter des requêtes clients, de compiler et d’exécuter du code dans un langage donné, tout en répartissant la charge entre les serveurs pour garantir la disponibilité en cas de forte demande.

## Image

[![](<../.gitbook/assets/download (7).php>)](/broken/pages/8f2a2fbdefb9f3376d9e2756291eebc2566c87fa)

## Compétences acquises

* Programmation en Python
  * Gestion des erreurs et des exceptions
  * Gestion des sockets et de la communication client/serveur
* Développement d’interfaces graphiques
* Compilation et exécution dynamique de code
* Optimisation du code
* Rédiger une documentation technique schématisé

## Ma réalisation

J’ai développé une solution où un client envoie un programme à un serveur pour l’exécuter à distance. J’ai codé un serveur capable de recevoir une requête, vérifier s’il est occupé, et si ce n’est pas le cas, compiler (si nécessaire), exécuter le programme et renvoyer les résultats au client.

J’ai aussi conçu un client avec une interface graphique permettant à l’utilisateur de sélectionner un programme, spécifier l’adresse du serveur, et suivre l'exécution en temps réel via un compteur. Si le serveur est occupé, l’utilisateur peut changer d’adresse sans interrompre le processus. Chaque serveur peut être lancé sur différents ports, permettant ainsi l'exécution sur plusieurs serveurs simultanément.

Tout au long du projet, j’ai veillé à bien commenter et structurer mon code, ce qui a demandé une attention particulière étant donné la quantité de lignes écrites en Python. Cette tâche m’a pris du temps, mais ça permet d’assurer la lisibilité et une facilité pour maintenir le projet à long terme.

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) (page 194)

## Emplacement du dossier travail

Dépôt GitHub

{% embed url="https://github.com/kylian-iut/SAE3.2" %}
