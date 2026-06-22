# \[DEVELOPPER] Accompagner le développement d’applications

Par [Kylian Adam](../)

## Apprentissages critiques

**Niveau 2 — S’intégrer dans une équipe DevOps**

* AC35.01DevCloud | Adopter les pratiques de pilotage de projet
* AC35.02DevCloud | Concevoir, gérer et sécuriser un environnement de microservices
* AC35.03DevCloud | Gérer son infrastructure comme du code
* AC35.04DevCloud | Gérer une chaîne d’intégration et/ou de déploiement continu

**Niveau 1 — Développer pour le Cloud**

* AC25.01DevCloud | Développer un microservice
* AC25.02DevCloud | Mettre en production une application
* AC25.03DevCloud | Programmer son réseau par le code

## Détails

**Niveau 2**

J'ai préparé un ensemble de machines virtuelles en les configurant via Ansible (AC35.03DevCloud) afin qu'ils puissent rejoindre le cluster.

J'ai conçu un environnement de microservices via les paquets de chacun et des manifests qui définissent les spécificités des conteneurs. Puis en déployant via Kubernetes en fournissant des secrets à travers les outils intégrés afin que les identifiants et mots de passes restent chiffrés (AC35.02). J'ai conçu un pipeline CI/CD pour GitLab (AC35.04) pour intégrer et déployer facilement les changements sur un projet d'une application API d'évènement du calendrier. C'est aussi par l'introduction dans cette chaîne, une série de tests qu'on vérifie la non régression des changements, qu'on adopte les pratiques de pilotage de projet de façon automatique.&#x20;

En tant qu'MOE\*, j'ai confirmé au niveau fonctionnel que la solution que j'ai apportée répond aux besoins énoncés par la MOA\*.

\*MOE = La maîtrise d’œuvre (réalise), \*MOA = La maîtrise d'ouvrage (formule le besoin) d'un projet.

**Niveau 1**

J'ai développé une application bancaire composé de plusieurs micro-services (AC25.01) basé sur des conteneurs Docker.

Durant mon stage j'ai réalisé des playbooks Ansible afin de déployer en masse des fonctionnalités de protection sur une flotte de Switch\* de la CEA\* (AC25.03DevCloud)

En entreprise, j'ai rédigé une fiche d'évolution (CE5.01) afin de renseigner les spécifications fonctionnelles et techniques de mon changement. J'ai développé et préparé en vu de sa production (AC25.02DevCloud) une nouvelle fonctionnalité d'une application afin d'y intégré un export de tableau Excel de données web filtrés, j'ai suivi la chaine d'intégration et de déploiement continu (CE5.04) mis en place afin de la rendre accessible en environnement de test (CE5.03). J'ai enfin mis à jour ma fiche d'évolution afin de rédiger une série de tests (CE5.02) permettant de valider les attendus.

\*CEA = Collectivité Européenne d'Alsace. \*Switch = équipement de commutation réseau.

## Composantes essentielles

* CE5.01 | en respectant un cahier des charges
* CE5.02 | en documentant le travail réalisé
* CE5.03 | en respectant les bonnes pratiques de développement et de production
* CE5.04 | en visant l’amélioration continue

## Traces

**Niveau 2**

* [SAE5.DevCloud.03 Orchestrer la conteneurisation d'une application](../projets/sae5.devcloud.03-orchestrer-la-conteneurisation-dune-application.md)
* [SAE6.DevCloud.01 Gérer le pipeline d’une application orientée Cloud](../projets/sae6.devcloud.01-gerer-le-pipeline-dune-application-orientee-cloud.md)

**Niveau 1**

* [SAE3.DevCloud.04 Mettre en place un infrastructure virtualisée](../projets/sae3.devcloud.04-mettre-en-place-une-infrastructure-virtualisee.md)

## Comment m'améliorer

**Niveau 2**

Manque encore d'adopter des pratiques de pilotage de projet et de savoir gérer une chaîne d'intégration CI/CD.&#x20;

**Niveau 1**

Il faudrait favoriser l'amélioration continue dans la partie développement en prenant des notes sur les erreurs courantes que j'ai rencontrés pendant mes développements.
