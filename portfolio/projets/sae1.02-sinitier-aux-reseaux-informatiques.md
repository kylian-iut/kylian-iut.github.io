# SAE1.02 S’initier aux réseaux informatiques

par [Kylian Adam](../)

### Contexte

Un réseau permet aux équipements de différents utilisateurs de pouvoir échanger entre eux. Dans une entreprise, il se doit d'être en parfaite sécurité, car les échanges doivent toujours pouvoir s'effectuer sans interruption et les données qui transitent ne doivent pas être visible de l'exterieur. Souvent, pour plus de sécurité, on limite même le domaine de diffusion des informations secteur par secteur. Par exemple l'administration, la comptabilité, l'accueil, etc. Que pouvons-nous envisager pour réaliser ces différents réseaux d'entreprise ? Quels sont les équipements requis ?

### Consigne

J'ai suivit un cahier des charges demandant de réaliser un réseau "virtualisé" comprennant 4 secteurs différents. Les machines appertenant à un réseau spécifique devront avoir leur propre plage IP, l'obtention d'une adresse pour les équipements se fait de manière dynamique depuis un serveur dédié. Une dernière exigence demande à ce que le réseau soit extensible à l'aide d'un second commutateur.

### Image

[![](<../.gitbook/assets/download (5).php>)](https://e-portfolio.uha.fr/artefact/file/download.php?file=219844\&view=55344\&time=1770752493)

### Ma réalisation

J'ai utilisé Eve NG comme plateforme virtualisé, c'est un système d'exploitation all-inclusive car il comprend une image des systèmes d'exploitations cisco, linux, etc.

Pour l'adressage j'ai repris mes connaissances et ma technique de l'abre des CIDR voir Image2, c'est de la logique qui demande de comprendre le fonctionnement binaire.

La topologie se constitue selon les exigences du cahier des charges : j'ai simplement représenté les secteurs ou VLans par une seule machine.

Pour configurer le commutateur j'ai utilisé les commandes que j'ai appris pour créer les VLans et attribuer les port au VLan correspondant.

Le serveur DHCP sous linux est nouveau pour moi, j'ai appris à utiliser le service nommé isc-dhcp-server avec de la documentation fournie.

La méthode Trunk dot1q est aussi quelque chose que j'ai appris en travaux pratiques, que je maîtrise totalement. J'ai réutilisé mes connaissances ici.

### Compétences acquises

* Utiliser une machine virtuelle
* Réaliser un adressage IP
* Réaliser la topologie d'un réseau
* Configurer un commutateur Cisco pour qu'il prenne en charge les VLans
* Configurer un serveur Linux pour qu'il prenne en charge le service DHCP
* Configurer la méthode trunk avec l'encapsulation dot1q

### Image2

[![](<../.gitbook/assets/download (6).php>)](https://e-portfolio.uha.fr/artefact/file/download.php?file=219846\&view=55344\&time=1770752493)

### Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) — page 69
