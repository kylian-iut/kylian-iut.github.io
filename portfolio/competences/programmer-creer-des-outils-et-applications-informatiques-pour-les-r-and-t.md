# \[PROGRAMMER] Créer des outils et applications informatiques pour les R\&T

par [Kylian Adam](../)

### Apprentissages critiques

**Niveau 3 —** Piloter un projet de développement d’une application R\&T

* AC33.01 | Élaborer les spécifications techniques et le cahier des charges d’une application informatique
* AC33.02 | Mettre en place un environnement de travail collaboratif
* AC33.03 | Participer à la formation des utilisateurs
* AC33.04 | Déployer et maintenir une solution informatique
* AC33.05 | S’informer sur les évolutions et les nouveautés technologiques
* AC33.06 | Sécuriser l'environnement numérique d'une application

**Niveau 2 — Développer une application R\&T**

* AC23.01 | Automatiser l’administration système avec des scripts
* AC23.02 | Développer une application à partir d’un cahier des charges donné, pour le Web ou les périphériques mobiles
* AC23.03 | Utiliser un protocole réseau pour programmer une application client/serveur
* AC23.04 | Installer, administrer un système de gestion de données
* AC23.05 | Accéder à un ensemble de données depuis une application et/ou un site web

**Niveau 1 — S’intégrer dans un service informatique**

* AC13.01 | Utiliser un système informatique et ses outils
* AC13.02 | Lire, exécuter, corriger et modifier un programme
* AC13.03 | Traduire un algorithme, dans un langage et pour un environnement donné
* AC13.04 | Connaître l’architecture et les technologies d’un site Web
* AC13.05 | Choisir les mécanismes de gestion de données adaptés au développement de l’outil et argumenter ses choix
* AC13.06 | S’intégrer dans un environnement propice au développement et au travail collaboratif

### Détails

**Niveau 3**

Durant mon stage, j'ai mis en place une plateforme Opensource de versionnage du code Gitea (AC33.02). J'ai respecté les bonnes pratiques de sécurité en réduisant les rôles aux besoins des utilisateurs et en chiffrant les mots de passes stockés dans l'environnement (AC33.06). J'ai expliqué à mes collaborateurs durant une réunion, appuyé d'une présentation, comment fonctionne Sémaphore UI, une interface d'orchestration de tâches Ansible et comment ma solution s'articule avec Git (AC33.03).

Dans mon entreprise, j'ai rédigé une fiche d'évolution (CE3.02) afin de renseigner les spécifications fonctionnelles et techniques de mon changement (AC33.01).

Je maintiens à jour régulièrement (AC33.04) mes services personnels de gestion d'agendas, de tâches & journaux et fichiers via Radicale en réalisant les mises à jours de sécurités et en renforcent au maximum les méthodes de connexions en fonction de la criticité du service ciblé. &#x20;

**Niveau 2**

Durant mon stage j'ai réalisé des playbooks Ansible afin de déployer en masse des fonctionnalités de protection sur une flotte de switch de la CEA\* (AC23.01), prenant en compte les modèles d'équipements et donc la diversité des commandes. J'ai mis en place une plateforme Gitea (AC23.04) pour collaborer et partager mes scripts, donnant des autorisations appropriées aux membres de l'équipe SINRT\*, sur requête de l'authentification LDAP du domaine. J'ai détaillé mes réalisations (CE3.02) et, dans le sens de l'IaC, j'ai recommandé l'utilisation de MS VS Code (CE3.04) à mes collaborateurs.

Basé sur les exigences d'un client fictif, souhaitant explorer plusieurs possibilités (CE3.01), j'ai réalisé une interface graphique pour le client (AC23.02) permettant d'établir le transfert d'un code vers un serveur de calcul à l'aide de mon protocole (AC23.03) et de visualiser le traitement de celui-ci. J'ai utilisé GitHub (AC23.05) pour assurer une sauvegarde régulière (CE3.03) et l'évolution de ma solution client/serveur.

\*CEA = Collectivité Européenne d'Alsace.\
\*SINRT = Équipe Systèmes d'information et du numérique orienté Réseaux et Télécommunications de la CEA.

**Niveau 1**

J'ai documenté (CE3.02) un travail basé sur l'e-réputation, ce qui m'a amené à concevoir mon propre site web avec l'éditeur VSCode (CE3.04). Le site est un répertoire composé de plusieurs fichiers (AC13.04) : 5 HTML pour le contenu des pages (1 redirection langue, 2 français et 2 anglais), un CSS pour la mise en forme et quelques PNG pour l'icône de l'onglet et pour illustrer les pages.

J'ai aussi collaboré avec un autre étudiant sur GitHub (AC13.06) pour programmer un script d'attaque de l'homme du milieu en Python destiné à visualiser le trafic entre deux machines du réseau pour une utilisation dans un cadre de tests uniquement (CE3.03). Il s'agit d'un outil d'espionnage de communication conçu pour être exécuté sur le système d'exploitation Kali Linux (AC13.01) qui dispose d'un environnement adapté à ces usages. Avant cela, un programme d'échauffement en Python (AC13.03) récupérait l'adresse MAC d'une machine ciblée par son adresse IP de manière passive ou active (échange avec les machines) et permettait aussi de lister toutes les machines connectées au réseau. Nous avons dû lire, exécuter et modifier le programme plusieurs fois pour qu'il corresponde aux attentes (AC13.02).

### Composantes essentielles

* CE3.01 | en étant à l'écoute des besoins du client
* CE3.02 | en documentant le travail réalisé
* CE3.03 | en utilisant les outils numériques à bon escient
* CE3.04 | en choisissant les outils de développement adaptés
* CE3.05 | en intégrant les problématiques de sécurité

### Traces

**Niveau 3**

* [SAE5.01 Concevoir, réaliser et présenter une solution technique](../projets/sae5.01-concevoir-realiser-et-presenter-une-solution-technique.md)
* [SAE5.02 Piloter un projet informatique](../projets/sae5.02-piloter-un-projet-informatique.md)

**Niveau 2**

* [SAE3.02 Développer des applications communicantes](../projets/sae3.02-developper-des-applications-communicantes.md)
* [Poster de stage du semestre 4](https://www.figma.com/design/m5KNDMzvPccVTQpC065E6w/PosterS4?node-id=0-1\&t=GmVpH5FjJhT8LEro-1)

**Niveau 1**

* [SAE1.04 Se présenter sur internet](../projets/sae1.04-se-presenter-sur-internet.md)
* [SAE1.05 Traiter des données](../projets/sae1.05-traiter-des-donnees.md)
* [SAE2.03 Mettre en place une solution informatique pour l'entreprise](../projets/sae2.03-mettre-en-place-une-solution-informatique-pour-lentreprise.md)

### Comment m'améliorer

**Niveau 3**

Il serait bien d'être mieux tenu informé sur les évolutions et les nouveautés technologiques. Comme se tenir informé depuis [Le monde informatique](https://www.lemondeinformatique.fr/reseau-1.html).

**Niveau 2**

Je trouve que j'ai passé trop de temps pour une solution client/serveur plutôt basique. Avec plus d'entraînement, même dans d'autres langages que Python, je pourrais être plus à l'aise pour développer et y prendre davantage plaisir dès que l'envie et le besoin se présentent.

**Niveau 1**

Nous avions choisi GitHub comme environnement de développement et de travail collaboratif car c'est le plus répandu. Il intègre beaucoup de fonctionnalités ; certains professionnels doivent même suivre une formation pour l'utiliser correctement. Pour ma part, je vais essayer d'apprendre par moi-même à l'utiliser de manière plus efficace : moins de Google Drive et plus de GitHub. Avec GitHub, soyons ouverts à partager avec tous — ainsi le monde progressera.
