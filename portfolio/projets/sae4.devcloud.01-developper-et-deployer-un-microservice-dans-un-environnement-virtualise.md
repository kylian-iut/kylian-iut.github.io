# SAE4.DevCloud.01 Développer et déployer un microservice dans un environnement virtualisé

par [Kylian Adam](../)

## Contexte

Nous devons être capable de collaborer avec un équipe de développement, contribuer à la conception d'applications. En s'appuyant sur un ensemble de microservices, qui doivent être déployable indépendamment, et ceux afin de permettre la scalabilité, la mise à jour transparente, et une évolution détaché des différentes parties qui composent les systèmes interconnectés. Comme nous réalisons à chaque fois des projets fictifs qui doivent être utiles aux entreprises, nous pourrions imaginer une application bancaire destinée à trois acteurs : les administrateurs, les agents bancaires et les clients interagissant sur le système bancaire intégrant les comptes, les utilisateurs, les virements, les dépôts, etc.

## Consigne

Développer une application bancaire en binôme permettant à un client :

* de visualiser ses comptes
* de faire un dépôt
* sur validation par l'agent de faire :
  * un retrait
  * un virement
  * créer un compte

L'agent pourra accéder aux statistiques des clients et valider les différentes actions des clients. Les actions sur l'interface web exécuteront des requêtes API. Une interface de gestion de log sera accessible par l'administrateur, celle-ci récupèrera les informations d'une base de donnée de logs. C'est avec un service de messagerie NATS que les différents services enverront leurs logs vers la BDD.

## Image

[![](<../.gitbook/assets/download (10).php>)](/broken/pages/11eb19f4e9002a1055d319ebf4e278510173c1d7)

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) — page 218

## Compétences acquises

* Concevoir et coder un microservice selon une architecture distribuée
* Utiliser un framework (Django)
* Gérer la communication entre microservices
* Déployer le microservice dans un environnement conteneurisé
* Écrire des scripts d’automatisation
* Mettre en œuvre une surveillance
* Gérer le projet en équipe avec des outils collaboratifs (Git)

## Ma réalisation

J’ai tout d’abord planifié et analysé le projet afin de répartir efficacement les tâches au sein de l’équipe. J’ai ensuite développé le module de gestion des clients, comprenant la consultation des comptes, la création de transactions et la gestion des opérations bancaires. J’ai également mis en place la gestion des logs à l’aide d’un service de messagerie, permettant la centralisation et l’affichage des journaux d’activité et des statistiques sur une interface web dédiée. J’ai participé aux tests unitaires et à l’intégration des différents services pour assurer la cohérence de l’ensemble, puis j’ai finalisé le projet en nettoyant, commentant et documentant le code afin de garantir sa maintenabilité et sa clarté.

## Emplacement du dossier travail

Dépôt GitHub

{% embed url="https://github.com/kylian-iut/SAE4.DevCloud" %}

Projet GitHub

{% embed url="https://github.com/users/kylian-iut/projects/3/views/4" %}
