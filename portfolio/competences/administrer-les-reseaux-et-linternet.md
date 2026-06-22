# ADMINISTRER les réseaux et l'internet

par [Kylian Adam](../)

### Apprentissages critiques

**Niveau 3 — Assister l'administrateur du réseau**

* AC11.01 | Maîtriser les lois fondamentales de l’électricité afin d’intervenir sur des équipements de réseaux et télécommunications
* AC11.02 | Comprendre l’architecture et les fondements des systèmes numériques, les principes du codage de l’information, des communications et de l’Internet
* AC11.03 | Configurer les fonctions de base du réseau local
* AC11.04 | Maîtriser les rôles et les principes fondamentaux des systèmes d’exploitation afin d’interagir avec ceux-ci pour la configuration et l’administration des réseaux et services fournis
* AC11.05 | Identifier les dysfonctionnements du réseau local et savoir les signaler
* AC11.06 | Installer un poste client, expliquer la procédure mise en place

**Niveau 2 — Administrer un réseau**

* AC21.01 | Configurer et dépanner le routage dynamique dans un réseau
* AC21.02 | Configurer et expliquer une politique simple de QoS et les fonctions de base de la sécurité d’un réseau
* AC21.03 | Déployer des postes clients et des solutions virtualisées adaptées à une situation donnée
* AC21.04 | Déployer des services réseaux avancés
* AC21.05 | Identifier les réseaux opérateurs et l’architecture d’Internet
* AC21.06 | Travailler en équipe pour développer ses compétences professionnelles

**Niveau 1 — Concevoir un réseau**

* AC31.01 | Concevoir un projet de réseau informatique d’une entreprise en intégrant les problématiques de haute disponibilité, de QoS, de sécurité et de supervision
* AC31.02 | Réaliser la documentation technique de ce projet
* AC31.03 | Réaliser une maquette de démonstration du projet
* AC31.04 | Défendre/argumenter un projet
* AC31.05 | Communiquer avec les acteurs du projet
* AC31.06 | Gérer le projet et les différentes étapes de sa mise en œuvre en respectant les délai

### Détails

**Niveau 3**

En participant au développement du jeu Krojanty lors de l'immersion à l'ENSISA, j'ai eu l'occasion d'échanger afin de répartir les rôles ciblé de chacun dans le temps (AC31.06) et de collaborer même à distance sur ce projet. Il a fallu également échanger avec d'autres équipes afin de fonctionner sur un même protocole de communication (AC31.05). J'ai commenté mon code (AC31.02) lors du développement des programmes C de communication réseau lors du développement de Krojanty.

J'ai mis en place un prototype (AC31.03) fonctionnel de traceur de véhicule avec communication LoRa via une carte Pycom et le serveur de réception avec LoRa, MQTT et web sur RasberyPi.

**Niveau 2**

J'ai développé mon protocole client/serveur TCP (CE1.01), ainsi que l'IHM pour mon cluster de calcul. J'ai anticipé les erreurs en développant avec des exceptions (CE1.03). Sur une maquette Eve NG simulant des équipements réseaux et des postes (AC21.03), j'ai utilisé VRRP (AC21.01) afin de proposer une redondance de passerelle vers la maquette opérateur (AC2.05) d'un coéquipier (AC21.06). Il m'a fallu appliquer des règles NAT et PAT (AC21.04) pour gérer le changement d'adressage, puis définir des règles de pare-feu (AC21.02) pour le trafic acheminé, inter-VLAN et internet (CE1.02).

**Niveau 1**

J'ai appris à respecter les principes fondamentaux de la sécurité informatique (CE1.02) en faisant des recherches (CE1.05) sur les bonnes pratiques (vérifier l'authenticité des emails, se méfier des clés USB trouvées : USB Killer / Bad USB, respecter la charte locale (CE1.04), tenir à jour les applications, prendre conscience des failles (AC11.02) et sauvegarder correctement nos données : HDD/SSD), des techniques qui permettent de prévenir les risques de piratage ou de dysfonctionnement (AC11.05 CE1.03).

Sous Eve NG (CE1.01) j'ai eu l'occasion de configurer les fonctions de base du réseau local (AC11.03) par moi-même (adressage IP, segmentation du réseau pour chaque groupe de l'entreprise avec les VLANs et l'encapsulation dot1q, routage inter-VLAN). Une fois le réseau prêt, j'ajoute les postes clients "VPCS", je change son hostname et j'applique le DHCP (AC11.06). J'ai également utilisé le système d'exploitation Linux (AC11.04) pour configurer un service DHCP pour le réseau.

### Composantes essentielles

* CE1.01 | en choisissant les solutions et technologies réseaux adaptées
* CE1.02 | en respectant les principes fondamentaux de la sécurité informatique
* CE1.03 | en utilisant une approche rigoureuse pour la résolution des dysfonctionnements
* CE1.04 | en respectant les règles métiers
* CE1.05 | en assurant une veille technologique

### Traces

**Niveau 3**

* [SAE5.01 Concevoir, réaliser et présenter une solution technique](../projets/sae5.01-concevoir-realiser-et-presenter-une-solution-technique.md)
* [SAE5.02 Piloter un projet informatique](../projets/sae5.02-piloter-un-projet-informatique.md)

**Niveau 2**

* [SAE3.02 Développer des applications communicantes](../projets/sae3.02-developper-des-applications-communicantes.md)
* [SAE3.DevCloud.03 Concevoir un réseau informatique multi-sites hébergeant des services](../projets/sae3.devcloud.03-concevoir-un-reseau-informatique-multi-sites-hebergeant-des-services.md)

**Niveau 1**

* [SAE1.01 Sensibilisation à l'hygiène informatique et à la cybersécurité](https://e-portfolio.uha.fr/view/view.php?t=9bf50148d08ae307f4a9)
* [SAE1.02 S’initier aux réseaux informatiques](../projets/sae1.02-sinitier-aux-reseaux-informatiques.md)

### Comment m'améliorer

**Niveau 3**

Prendre la défense d'un projet serai intéressant à découvrir, tout comme intégrer dans un projet d'entreprise des problématiques de haute disponibilité, de QoS, de sécurité et de supervision

**Niveau 2**

Il faudrait que je développe d'avantage mes explications, concernant les procédures et méthodes pour mettre en place les protocoles réseaux dans mes rapports.

**Niveau 1**

Il faudrait que je précise mes notes dans mes recherches lors de la veille technologique, car cela me permettrait de balayer l'ensemble des solutions envisageables. J'aurai évité par exemple d'utiliser trois liens pour relier un switch (configuré avec trois VLANs) à un routeur. En effet, il existe la technique des interfaces virtuelles, paquets encapsulés passant par un seul lien en trunk (int g0/0/0.10, int g0/0/0.20, ...)
