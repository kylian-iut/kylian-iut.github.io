# SAE6.DevCloud.01 Gérer le pipeline d’une application orientée Cloud

par [Kylian Adam](../)

## Contexte

Nous arrivons dans une ère du perfectionnement de l'automatisation. Nous l'avons compris, les applications doivent s'orienter vers le Cloud afin de gagner en efficacité, robustesse à la charge, et même en sécurité. C'est aussi un moyen de segmenter et d'isoler les développements de fonctionnalités d'une même application, on l'a vu dans le dernier projet. Maintenant, l'automatisation de la chaîne d'intégration (CI) pour les contrôles habituels de sécurité et de non régression, et le déploiement continu (CD) pour les processus habituels de mise à disposition vont nous permettre de gagner du temps et de l'efficacité sur ces manipulations techniques répétitifs.&#x20;

## Consigne

Configurer une machine avec l'OS Proxmox SE afin de créer notre environnement de systèmes d'informations d'entreprise fictif afin d'héberger sur une première machine virtuelle (VM) une plateforme GitLab pour stocker les versions de codes des projets et de permettre l’exécution des pipelines CI/CD. 3 autres machines virtuelles vont servir de Runners pour récupérer les jobs du pipeline du projet préalablement choisi. Le déploiement et la configuration de ces 4 VMs sera reproductible facilement via des scripts IaC\* avec Terraform qui déclarent l'état attendu de la VM sur Proxmox, et via des scripts Ansible qui spécifient les étapes de configuration sur le système cible.&#x20;

\*IaC = Infrastructure as Code

## Images

<div><figure><img src="../.gitbook/assets/Capture d’écran (11).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Capture d’écran (10).png" alt=""><figcaption></figcaption></figure></div>

## Compétences acquises

* S'appuyer sur l'IaC Terraform pour mettre en place un environnement
* Mettre en place une Pipeline CI/CD pour un projet
* Sécuriser des scripts de configuration
* Fournir un rapport de sécurité

## Ma réalisation

Sur un ordinateur j'ai manuellement installé l'OS Proxmox SE pour virtualiser mon environnement.&#x20;

J'ai utilisé Terraform via le provider bpg/proxmox afin que Terraform puisse utiliser les API qui permettent de contrôler Proxmox. J'ai veillé à respecter la notion du moindre privilège afin de donner un utilisateur pour Terraform qui dispose uniquement des permissions qui lui sont nécessaires et en stockant sont api\_token en haché dans l'environnement du système. J'ai réalisé un script Terraform pour définir nos 4 VMs simultanément avec des spécificités différentes grâce à la typographie (ex: cores = count.index == 0 ? 4 : 2), puis une sortie Terraform qui constitue automatiquement l'inventaire d'Ansible.&#x20;

J'ai conçu des playbooks afin de configurer client/serveur DNS, mettre en place GitLab, mettre en place un cluster swarm avec Load Balancer sur les 3 VMs et les faire rejoindre le cluster, et enfin déployer trois services sur ce cluster de deux répliquas de conteneurs Alpine pour faire office de Runners Docker.

Enfin, j'ai conçu le script gitlab-ci sur le projet de l'application Cloud afin de permettre différents traitements : les tests unitaires, la compilation, la vérification de sécurité de l'image Docker avec rapport, le déploiement sur l'environnement requis et la vérification de l'accès à la page. Le pipeline permet le déploiement par étape sur chaque environnement ; A l'envoie d'un changement et selon le nom de la branche et de l'ajout d'un tag on affecte le mode de déploiement (review, intégration, préproduction, production).

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) — page 258

## Emplacement du dossier travail

2 dépôts GitHub

{% embed url="https://github.com/kylian-iut/SAE6.DevCloud.01" %}

{% embed url="https://github.com/kylian-iut/SAE6.DevCloud.01-app" %}
