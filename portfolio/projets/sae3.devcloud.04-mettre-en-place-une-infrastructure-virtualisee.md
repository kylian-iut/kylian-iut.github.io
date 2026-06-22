# SAE3.DevCloud.04 Mettre en place une infrastructure virtualisée

Par [Kylian Adam](../)

## Contexte

Les commerçants cherchent à se digitaliser pour mieux vendre leurs produits et gérer leur activité. Cela passe par la mise en place de sites e‑commerce pour toucher une clientèle plus large, et de solutions internes pour automatiser la gestion comptable, administrative ou logistique. Ces besoins impliquent de déployer des infrastructures informatiques fiables, capables de fonctionner sans interruption, surtout lors de périodes d’activité intense. La continuité de service, la sécurité des données et la facilité de maintenance sont des enjeux clés dans ce type de projet.

## Consigne

Architecturer une infrastructure pour les activités de Lor pâtisserie. Déploiement de deux services principaux :

* un site e‑commerce pour la vente en ligne
* une plateforme de gestion administrative

Le projet inclut le dimensionnement matériel, le choix des solutions logicielles, la mise en place des architectures réseau et virtuelle, ainsi que la définition des procédures de maintenance, sauvegarde et montée en charge lors des périodes critiques.

## Image

[![](<../.gitbook/assets/download (8).php>)](/broken/pages/ed6bf529f48b24eba50b253cf38d4d27a2767fdd)

## Ma réalisation

J'ai d'abord simulé une solution hybride combinant des serveurs on‑premise et des ressources cloud. J’ai étudié l’allocation dynamique des ressources OVH Cloud pour gérer les périodes de surcharge, en augmentant les vCPU et la mémoire RAM pour Prestashop pendant les pics de trafic (Noël, Pâques, Saint‑Valentin).

J'ai conçu des schémas d'architecture avec des serveurs DELL R640 en RAID6, la gestion via Proxmox VE pour la virtualisation des bases de données (MySQL et PostgreSQL) en haute disponibilité. J’ai imaginé des scénarios de panne (perte de disque) et proposé des solutions pour maintenir la continuité des services.

J’ai aussi analysé les aspects de sécurité du réseau, recommandant l'utilisation d'un VPN pour sécuriser les communications. Enfin, j’ai préparé un plan d’action détaillé pour l’installation et la configuration, en estimant le temps et les coûts associés.

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS — page 196](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf)

## Compétences acquises

* Analyse et conception d'infrastructure hybride
* Virtualisation avec Proxmox VE
* Rédaction de rapport technique
* Gestion de la sécurité des données et conformité légale

## Emplacement du dossier de travail

Google Drive - Dossier partagé

{% embed url="https://drive.google.com/drive/folders/1uZnxuJLcSBsGQBQxjKjtUr-_9gXXpXAd" %}
