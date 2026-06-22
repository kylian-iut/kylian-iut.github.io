# SAE2.04 Projet intégratif

par [Kylian Adam](../)

## Contexte

Pour terminer la 1ère année du BUT, nous allons, en groupe d'autonomie, combiner les notions et techniques vues cette année. Pour cela, nous réaliserons un réseau informatique simple mais sécurisé, comprenant des postes téléphoniques. Cette structure accueillera une solution pour l'obtention d'informations de capteurs d'environnement ; cette solution comprend : un récepteur MQTT, une base de données et un site web pour afficher les données reçues.

## Consignes

* Créer 4 sous-réseaux sur une adresse réseau IPv4 classe C.
* La communication entre les sous-réseaux passera uniquement par le routeur afin de filtrer les communications.
* Pour que le VLAN User n'ait pas accès au VLAN Admin, le service FTP du VLAN Server sera uniquement accessible depuis le VLAN Admin.
* Restreindre le trafic du VLAN User sur les sites marchands sur Internet.
* Pour la téléphonie, utiliser un serveur Cloud existant : LinPhone.
* La réception MQTT se fera depuis le site test.mosquitto.org vers notre BDD.
* Réaliser un site web qui récupère les données de la BDD et les liste. L'utilisateur pourra nommer le capteur et définir son emplacement. Un graphique permettra de visualiser l'évolution de la température des capteurs.

## Images

<div><img src="../.gitbook/assets/download (15).php" alt="Image1" width="563"> <img src="../.gitbook/assets/download (16).php" alt="Image2" width="563"> <img src="../.gitbook/assets/download (17).php" alt="Image3" width="563"></div>

## Compétences acquises

* Réaliser un plan d'adressage IP
* Configurer des équipements réseaux (commutateur, routeur, téléphone IP)
* Configurer le rôle serveur DHCP pour commutateur Cisco
* Mettre en place des services sous Windows Server (DNS, FTP et MySQL)
* Programmer une application web dynamique liée à une base de données
* Configurer des postes clients

## Ma réalisation

J'ai d'abord réalisé le plan d'adressage dans un tableau que j'ai fourni à mes coéquipiers. Ensuite, j'ai réalisé le branchement sur la baie de brassage afin de relier les équipements au commutateur, le commutateur au routeur et le routeur à l'extérieur. J'ai apprécié cette partie ; je me suis vraiment appliqué au "Cable Management".

J'ai configuré une machine virtuelle Windows Server pour y installer le service FTP afin que l'administrateur puisse y faire des sauvegardes. J'ai également installé un service DNS avec des enregistrements A pour mon serveur, pour le serveur web et pour le commutateur : on a alors une adresse FQDN pour ces machines (serv1.rt14.lab.).

J'ai ensuite paramétré le téléphone matériel Yealink pour qu'il soit relié au serveur SIP en cloud Linphone. J'ai personnalisé la sonnerie, configuré les touches d'appels rapides et la liste de contacts.

Enfin, j'ai collaboré pour terminer la partie web du projet afin que l'utilisateur puisse interagir avec les données dans un tableau (ajouter des informations au capteur, visualiser ses données) et aussi les trier selon un critère choisi.

## Sources

[Programme national RESEAUX ET TELECOMMUNICATIONS](http://rt.pu-pm.univ-fcomte.fr/images/6/64/PN_BUT_RT_2022_BO_spe617_annexe22_1426160.pdf) — page 96

## Emplacement du dossier travail

Google Drive - Dossier partagé - Accès Public

{% embed url="https://drive.google.com/drive/folders/1MqmYZ0kQ0eV71hlbupR_CsPxt2_KbfNC?usp=sharing" %}

Dépôt GitHub

{% embed url="https://github.com/kylian-iut/SAE_integrative" %}
