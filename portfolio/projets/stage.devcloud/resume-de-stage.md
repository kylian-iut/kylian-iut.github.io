# Résumé de stage

## Comprendre les mécanismes DHCP Snooping, DAI, IGMP Snooping, Storm-control

DHCP Snooping va permettre d’analyser les échanges DHCP qui transitent sur le switch, et ainsi constituer une table d’écoute comme ci-dessous.

| Interface | Vlan  | IP           | MAC                | Durée restante |
| --------- | ----- | ------------ | ------------------ | -------------- |
| Ge-0/0/1  | User  | 192.168.1.14 | 06 :44 :e6 :3f :41 | 15:12          |
| Ge-0/0/2  | Admin | 192.168.1.16 | 06 :98 :00 :14 :b2 | 01:20          |

Aussi, les paquets DHCP Offer reçu sur des interfaces non approuvées seront supprimés. Ainsi il ne peut pas y avoir un faux serveur DHCP.

L’inspection dynamique ARP va se baser sur la table d’écoute DHCP afin d’autoriser uniquement les paquets provenant des hôtes enregistrés dans la table. Les équipements qui n’ont pas terminer l’obtention DHCP ne pourront donc pas communiqer.

![](<../../.gitbook/assets/Unknown image>)

Si IGMP Snooping est activée, les pertes de bande passante et les attaques hostiles DDoS seront largement réduites. Tous les hôtes situés dans le réseau en aval ne reçoivent que les paquets de multidiffusion pour lesquels ils ont été préalablement autorisés. L'utilisation d'un switch réseau prenant en charge IGMP Snooping est donc utile dans tous les environnements où une grande largeur de bande est nécessaire. Il s'agit par exemple de l'IPTV et d'autres services de streaming ainsi que des solutions de conférence web. Cependant, les réseaux ne comptant que quelques utilisateurs et n'ayant pratiquement pas de trafic de multidiffusion ne bénéficient pas de cette procédure de filtrage. Même si le switch ou le routeur offre la fonction IGMP Snooping multicast, celle-ci doit rester désactivée pour éviter les interceptions inutiles. C’est le cas à la CEA, nous garderons l’option désactivé.

Une tempête de trafic est générée lorsque des messages sont diffusés sur un réseau et que chaque message invite un nœud récepteur à répondre en diffusant ses propres messages sur le réseau. Ceci, à son tour, suscite d’autres réponses, créant un effet boule de neige. Le réseau local est soudainemet submergé de paquets, ce qui crée un trafic inutile qui entraîne de mauvaises performances du réseau, voire une perte totale du service réseau. Il faut donc définir une limite. J’ai choisi que 30% de la capacité totale de l’interface peut supporter des paquets à destination inconnu, le surplus n’est pas acheminé.

## Déployer un service pour Ansible

La version 2.13.5 de Sémaphore offre une interface graphique pour l’utilisation de différents outils dont Ansible.

![](<../../.gitbook/assets/Unknown image (1)>)

Nous pouvons regrouper les équipements dans des inventaires et les associer à une entrée d’une base d’identifiants chiffrés qui permettra d’établir des connexions SSH sur les switchs.

![](<../../.gitbook/assets/Unknown image (2)>)

Le service est déployé sous Cent OS car c’est le système recommandé à la CEA, il a un support externe spécifique pour cet environnement.

## Rédiger et stocker avec Git des playbook adaptés aux solutions

**IaC Infrastructure As Code**

Les playbook sont des scripts séquentiels contenant les tâches à réaliser, pour traiter des informations et appliquer des changements dans la configuration.

![](<../../.gitbook/assets/Unknown image (3)>)

Avec Loïc, nous partions du principe pour notre utilisation, que l’exécution d’un playbook pouvait prendre autant de temps que nécessaire. Mais il est possible de réaliser des connexions asynchrones afin de gagner du temps. Il faut déclarer le paramètre « async » avec une durée d’exécution maximale. J’ai choisi 45 secondes maximum, comme ci-dessous, pour récupérer toutes les informations du switch afin de générer un rapport.

![](<../../.gitbook/assets/Unknown image (4)>)

Avant, j’utilisais une tâche par commande et Ansible ferme la connexion à la fin de la tâche avant de se reconnecter pour les besoins d’une autre, on constatait plusieurs connexions à la suite dans les logs. Regrouper les commandes dans une seule tâche réduit à une seule connexion par switch.

Ce n’était pas plus compliqué à traiter, car les différentes sorties sont ajoutées à la liste stdout. ![](<../../.gitbook/assets/Unknown image (5)>)

J’utilise VS Code comme éditeur, il me permet de manipuler les différentes versions de mon code grâce à Git. Le dépôt Git pour l’équipe SIN-RT est [https://codebox.bas-rhin.fr/sin-rt](https://codebox.bas-rhin.fr/sin-rt)

La connexion de l’éditeur s’effectue seulement par SSH à l’aide d’une clé privée sur codebox.

Note : pour générer une paire de clé utilisez ssh-keygen dans l’invite de commande. Récupérez la clé publique associé C:\Users%username%/.ssh/id\_ed25519.pub et ajoutez là sur le site codebox dans User Settings/SSH Keys.

Sur VS Code, j’utilise l’extension git-autoconfig afin de configurer les valeurs git.email et git.username lorsque je clone un dépôt.

Une fois l’environnement préparé, on peut sélectionner Clone Git Repository…, il faut ensuite spécifier l’URL SSH que l’on trouve comme ci-dessous ([git@codebox.bas-rhin.fr:sin-rt/playbook.git](mailto:git@codebox.bas-rhin.fr:sin-rt/playbook.git))

![](<../../.gitbook/assets/Unknown image (6)>)
