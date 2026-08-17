# SAE5.DevCloud.03 Orchestrer la conteneurisation d’une application

par [Kylian Adam](../)

## Contexte

Permettre à une application sa migration dans le cloud permet ainsi de gagner en optimisation énergétique, matérielle mais aussi en disponibilité et élasticité de service. Pour que tous ces avantages puissent s'opérer, il est primordial de développer l'application en plusieurs microservices autonomes (ex : les logiques de catalogue produit, d'authentification client, de gestion du panier, et bien sûr de l'affichage de l'interface web). Ainsi l'environnement cloud pourra au besoin ajouter des nœuds qui représentent chaque microservice afin d'assurer la charge montante de requêtes.

## Consigne

Concevoir le développement et le déploiement, dans une équipe de 4 étudiants, d'une application d'e-commerce de votre choix, dans le langage de votre choix. Elle sera hébergée sur un cluster Kubernetes et comportera plusieurs nœuds pour chaque microservice.

## Compétences acquises

* Développer avec le framework ASP .NET Core
* Concevoir des endpoints
* Réaliser des manifests Kubernetes pour déployer des services
* Générer un document PDF avec QuestPDF

## Ma réalisation

J'ai conçu une API pour la gestion du panier du client et des commandes. J'ai développé ce microservice en C# avec le framework ASP .NET Core. J'ai utilisé les informations contenues dans le token afin d'identifier le client, ce qui permet de mettre un nom sur la facture après avoir passé commande. J'ai aussi rédigé des manifests Kubernetes qui décrivent l'état désiré des nœuds dans le cluster. Pour chaque microservice, j'ai réutilisé le fichier docker-compose réalisé lors du développement et je l'ai adapté aux besoins du cluster.

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) — page 239

## Emplacement du dossier travail

Organisation GitHub (6 Dépôts, 1 Projet)

{% embed url="https://github.com/LesProsDevCloud" %}
