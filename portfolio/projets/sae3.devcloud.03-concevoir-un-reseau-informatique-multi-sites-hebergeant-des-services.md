# SAE3.DevCloud.03 Concevoir un réseau informatique multi-sites hébergeant des services

SAE3.DevCloud.03 Concevoir un réseau informatique multi-sites hébergeant des services

par [Kylian Adam](../)

### Contexte

Les entreprises ont besoin d'une infrastructure réseau solide et sécurisée pour connecter leurs différents sites et accéder facilement aux ressources locales ou dans le Cloud. Avec l’évolution des technologies et des besoins, maintenir et faire évoluer ce réseau est essentiel pour garantir des performances optimales et offrir de la disponibilité à toutes épreuves. Un professionnel en Développement Système et Cloud doit donc être capable de concevoir et gérer une infrastructure qui permet de relier ces différents sites, tout en offrant des services performants et sécurisés. Cela implique de comprendre les bases du réseau, mais aussi les protocoles avancés. De savoir configurer les équipements nécessaires, et de mettre en place des solutions adaptées aux besoins spécifiques de l’entreprise.

### Consigne

Mettre en place une architecture réseau multi-sites pour deux entreprises dans l’e-commerce : UC Exchange et ABC Conseil, présentes à Strasbourg, Nancy, Metz. Chaque site comprend quatre services, plus une salle des serveurs. Le réseau doit permettre aux sites d’accéder aux services locaux et Cloud, avec une infrastructure réseau scalable. Maîtrise couche liaison de donnée et couche réseau.

### Compétences acquises

* Conception et architecture de réseaux multi-sites
* Routage et gestion des VLAN
* Redondance de passerelle
* Administration de services avancés
* Configuration de protocoles pour l'acheminement
* Gestion du Pare-feu et de la translation d’adresses
* Rapport des actions réalisés

### Image

[![](<../.gitbook/assets/download (9).php>)](https://e-portfolio.uha.fr/artefact/file/download.php?file=259753\&view=65408\&time=1770752493)

### Ma réalisation

Dans cette réalisation, j'ai conçu et configuré l'architecture LAN de deux entreprises réparties sur plusieurs sites. J'ai créé un plan d’adressage IP structuré, divisant chaque site en VLANs dédiés aux différents services (informatique, serveurs, direction, finance) pour une gestion optimale du trafic. J’ai configuré des switches en MST pour éviter les boucles et mettre en place des liens redondants via EtherChannel. Afin d'assurer la redondance et la haute disponibilité, j'ai implémenté VRRP entre les routeurs principaux. Le NAT et le PAT ont été configurés pour garantir la sécurité des communications avec l’extérieur. Enfin, l'architecture en 3 couches (core, distribution, access) a été choisie pour sa scalabilité et sa tolérance aux pannes, assurant ainsi une infrastructure résiliente et facilement extensible.

### Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) (page 195)

### Emplacement du dossier travail

Google Drive - Dossier partagé

{% embed url="https://drive.google.com/drive/folders/1ndrpCKEHVGUE7ulryyLV2OoK_Kk5Cj5W?usp=sharing" %}
