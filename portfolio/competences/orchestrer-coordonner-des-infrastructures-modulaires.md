# \[ORCHESTRER] Coordonner des infrastructures modulaires

par [Kylian Adam](../)

### Apprentissages critiques

**Niveau 2 — Administrer une infrastructure Cloud**&#x20;

* AC34.01DevCloud | Concevoir, administrer et superviser une infrastructure Cloud
* AC34.02DevCloud | Orchestrer les ressources Cloud
* AC34.03DevCloud | Investiguer sur les incidents et les résoudre afin d’améliorer la qualité et la fiabilité des infrastructures

**Niveau 1 — Assister l’administrateur infrastructure et Cloud**

* AC24.01DevCloud | Proposer une solution Cloud adaptée à l’entreprise
* AC24.02DevCloud | Virtualiser un environnement
* AC24.03DevCloud | Utiliser les services du Cloud
* AC24.04DevCloud | Analyser un service Cloud au travers des métriques

### Détails

**Niveau 2**

J'ai conçu un microservice pour le Cloud (AC34.01), afin de gérer le panier client et les commandes d'un site d'e-commerce. J'ai aussi fait en sorte que l'infrastructure contenant l'ensemble des microservices soient inclus dans un cluster de plusieurs nœuds (AC34.02). Il m'ai arrivé de devoir débogué avec un collaborateur afin de résoudre un problème d'accès web non autorisé, après avoir investigué (AC34.03), j'ai pu déduire que l'incident était lié à un déploiement de mon microservice qui ne respectait pas la sécurité. J'ai pu adapter mon code afin de ne plus permettre un déploiement non sécurisé (CE4.03).&#x20;

J'ai mis en place des outils d'administration d'infrastructure Cloud (AC34.01) via Terraform permettant de (re)déployer des VMs et de les reconfigurer rapidement par la suite avec Ansible. J'ai aussi prévu de mettre à disposition des moyens pour superviser les systèmes et les applications via un playbook de déploiement de Promotheus et Grafana. J'ai conçu un pipeline CI/CD pour une application Cloud (CE4.05).&#x20;

**Niveau 1**

J'ai imaginé un environnement cloud pour héberger les outils métiers d'une PME (AC24.01) en m'appuyant sur leurs contraintes du client (CE4.01) en durée RPO/RTO et en charge de connexions simultanés (AC24.04). À la suite de mes recherches des solutions existantes (CE4.04), j'ai proposé une infrastructure divisée On-premise et Cloud par les services de OVH Cloud (AC24.03), en fournissant une documentation explicite (CE4.02) de ma solution.

J'ai virtualisé une maquette (AC24.02) avec des switchs et des routeurs afin de simuler l'infrastructure d'une entreprise. J'ai séparé le flux utilisateur et administrateur par une segmentation VLAN afin de pouvoir limiter l'accès (CE4.03) à la configuration des switchs. Puis j'ai relié ma maquette réseau d'entreprise avec d'autres (datacenter et opérateur) réalisés par mes collègues (CE4.05).

J'ai développé une application bancaire composé de plusieurs micro-services (AC24.01) basé sur des conteneurs Docker, les endpoints permettant de gérer les clients et  les agents bancaires (création d'utilisateur, authentification, gestion des comptes, des opérations, ...) puis en générant des logs avec types et niveau de criticité (CE4.03), regroupés sur une page de visualisation avec filtre et recherche. J'ai collaboré avec un autre étudiant sur GitHub avec un dépôt commun et l’outil de projet afin de planifier les tâches dans le temps (CE4.05).

### Composantes essentielles

* CE4.01 | en respectant un cahier des charges
* CE4.02 | en documentant le travail réalisé
* CE4.03 | en intégrant les problématiques de sécurité
* CE4.04 | en assurant une veille technologique
* CE4.05 | en respectant les pratiques d’équipes et des méthodes de production

### Traces

**Niveau 2**

* [SAE5.DevCloud.03 Orchestrer la conteneurisation d'une application](../projets/sae5.devcloud.03-orchestrer-la-conteneurisation-dune-application.md)
* [SAE6.DevCloud.01 Gérer le pipeline d’une application orientée Cloud](../projets/sae6.devcloud.01-gerer-le-pipeline-dune-application-orientee-cloud.md)

**Niveau 1**

* [SAE3.DevCloud.03 Concevoir un réseau informatique multi-sites hébergeant des services](../projets/sae3.devcloud.03-concevoir-un-reseau-informatique-multi-sites-hebergeant-des-services.md)
* [SAE3.DevCloud.04 Mettre en place une infrastructure virtualisée](../projets/sae3.devcloud.04-mettre-en-place-une-infrastructure-virtualisee.md)
* [SAE4.DevCloud.01 Développer et déployer un microservice dans un environnement virtualisée](../projets/sae4.devcloud.01-developper-et-deployer-un-microservice-dans-un-environnement-virtualise.md)

### Comment m'améliorer

**Niveau 2**

Une veille technologique plus poussée et une meilleure communication d'équipe permettrai de gagner du temps. Je pense à rester notifié sur [les actualités DevOps de ITSocial](https://itsocial.fr/cloud-infrastructure-it/).

**Niveau 1**

Je me suis déjà familiarisé avec des outils comme docker afin de réaliser facilement un déploiement de mon infrastructure Cloud, mais j'ai besoin de connaître plus de mécanismes et de bonnes pratiques qui me permettront de simplifier et de réduire le volume de données de mes projets. Je peux m'inspirer de solutions existantes comme ceux de [Self-Hosting](https://selfh.st/apps/)
