# CONNECTER les entreprises et les usagers

par [Kylian Adam](../)

## Apprentissages critiques

**Niveau 3 — Déployer une solution de connexion ou de communication sur IP**

* AC32.01 | Déployer un système de communication pour l’entreprise
* AC32.02 | Déployer un réseau d’accès sans fil pour le réseau d’entreprise en intégrant les enjeux de la sécurité
* AC32.03 | Déployer un réseau d’accès fixe ou mobile pour un opérateur de télécommunications en intégrant la sécurité
* AC32.04 | Permettre aux collaborateurs de se connecter de manière sécurisée au système d’information de l’entreprise
* AC32.05 | Collaborer en mode projet en français et en anglais

**Niveau 2 — Maîtriser les différentes composantes des solutions de connexion des entreprises et des usagers**

* AC22.01 | Déployer et caractériser des systèmes de transmissions complexes
* AC22.02 | Mettre en place un accès distant sécurisé
* AC22.03 | Mettre en place une connexion multi-site via un réseau opérateur
* AC22.04 | Déployer des réseaux d’accès des opérateurs
* AC22.05 | Capacité à questionner un cahier des charges RT

**Niveau 1 — Découvrir les transmissions et la ToIP**

* AC12.01 | Mesurer, analyser et commenter les signaux
* AC12.02 | Caractériser des systèmes de transmissions élémentaires et découvrir la modélisation mathématique de leur fonctionnement
* AC12.03 | Déployer des supports de transmission
* AC12.04 | Connecter les systèmes de ToIP
* AC12.05 | Communiquer avec un tiers (client, collaborateur...) et adapter son discours et sa langue à son interlocuteur

## Détails

**Niveau 3**

J'ai programmé la connexion mode AP Wi-Fi sécurisé (AC32.02) avec Python sur la carte Pycom. En utilisant LoRa (AC32.01) la sécurité du dispositif (AC32.03) tracé est assuré par la portée plus importante quelle propose comparé à d'autres technologies. Les connexions à la configuration du serveur se fait via SSH sécurisé par identifiant et mot de passe (AC32.04).

**Niveau 2**

J'ai réalisé une veille technologique (CE2.03), puis j'ai comparé des composants électroniques. J'ai suivi les étapes du Cycle en V (CE2.02) afin de concevoir une prise connectée par MQTT (AC22.01). J'ai préparé le LAN d'une entreprise fictive afin de la connecter à son opérateur (AC22.03), et à un site distant à travers un tunnel VPN (AC22.02). J'ai rectifié le tir plusieurs fois, à plusieurs étapes de l'avancement du développement de mon application, en vérifiant si cela respecte le cahier des charges (AC22.05). J'ai coordonné le déploiement du réseau d'opérateur (AC22.04), en expliquant les techniques et les commandes à utiliser pour établir le routage, les systèmes autonomes BGP et les liens MPLS entre les sites d'une entreprise.

**Niveau 1**

J'ai collaboré (AC12.05) pour réaliser un plan, une heatmap Acrylic (CE2.03) Wi‑Fi du réseau d'un bâtiment de l'établissement pour repérer les problèmes et les besoins, pour les connections avec les équipements sans-fil. Puis j'ai installé un point d'accès (AC12.03) et j'ai évalué ses capacités en effectuant une mesure de porté du signal qu'il émet, et son influence sur les canaux voisins. Puis une mesure de débit de transfert de données à différentes distance du point d'accès. J'ai résumés les résultats des mesures par des graphiques et des conclusions rédigés dans un compte rendu (AC12.01). Dans notre installation, le point d'accès utilise un seul câble pour l'alimentation et les données, c'est le commutateur qui délivre la puissance sur les ports PoE. J'ai pu les configurer pour qu'ils fonctionnent seulement la journée, car on souhaite économiser l'énergie la nuit (CE2.04).

## Composantes essentielles

* CE2.01 | en communiquant avec le client et les différents acteurs impliqués, parfois en anglais
* CE2.02 | en faisant preuve d'une démarche scientifique
* CE2.03 | en choisissant les solutions et technologies adaptées
* CE2.04 | en proposant des solutions respectueuses de l'environnement

## Traces

**Niveau 3**

* [SAE5.01 Concevoir, réaliser et présenter une solution technique](../projets/sae5.01-concevoir-realiser-et-presenter-une-solution-technique.md)
* [SAE5.02 Piloter un projet informatique](../projets/sae5.02-piloter-un-projet-informatique.md)

**Niveau 2**

* [SAE3.01 Mettre en œuvre un système de transmission](../projets/sae3.01-mettre-en-oeuvre-un-systeme-de-transmission.md)
* [SAE3.02 Développer des applications communicantes](../projets/sae3.02-developper-des-applications-communicantes.md)
* [SAE3.DevCloud.03 Concevoir un réseau informatique multi-sites hébergeant des services](../projets/sae3.devcloud.03-concevoir-un-reseau-informatique-multi-sites-hebergeant-des-services.md)

**Niveau 1**

* [SAE1.03 Découvrir un dispositif de transmission](../projets/sae1.03-decouvrir-un-dispositif-de-transmission.md)
* SAE2.02 Mesurer et caractériser un signal ou un système
* [SAE2.04 Projet intégratif](../projets/sae2.04-projet-integratif.md)

## Comment m'améliorer

**Niveau 3**

Je n'ai pas encore eu l'occasion de collaborer en mode projet en anglais/français&#x20;

**Niveau 2**

Il me faut maintenant plus d'attention sur les formules mathématiques, concernant les phénomènes physiques étudiés, et non seulement connaître leurs caractéristiques, ce qui est déjà un acquis.

**Niveau 1**

En faisant preuve d'une démarche scientifique (CE2.02)... Je n'ai pas vraiment eu l'occasion de mettre en œuvre ce point lors de ma première année. Alors peut-être l'année prochaine.
