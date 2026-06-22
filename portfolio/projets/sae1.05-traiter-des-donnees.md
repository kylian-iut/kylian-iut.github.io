# SAE1.05 Traiter des données

SAE1.05 Traiter des données

par [Kylian Adam](../)

### Contexte

La sécurité n'est pas inhérente à tous les systèmes. Ce n'est pas parce qu'un inventeur a décidé que sa technologie serait imprenable, qu'elle l'est vraiment. On veut éviter que des personnes malveillantes accèdent à un réseau. Pour prévenir ce risque, on va se mettre dans la peau de cette personne et tenter de trouver des failles : c'est ce qu'on appelle le pentesting.

Imaginons qu'un employé, donc une personne de confiance, est en fait un espion infiltré. Il va être au sein de la communication avec les autres employés. Pourquoi un LAN est-il si vulnérable ? Peut-on réellement espionner le traffic dans un réseau ?

### Consigne

Par groupe de deux étudiants, mettez en place :

{% stepper %}
{% step %}
### Découverte des machines sur le réseau

Mettre en place un script qui fait la découverte des machines connectées sur le réseau (IP + MAC).
{% endstep %}

{% step %}
### Attaque de l'homme du milieu

Mettre en place un script de l'attaque de l'homme du milieu permettant de visualiser le traffic entre deux machines du réseau.
{% endstep %}
{% endstepper %}

### Image

[![](<../.gitbook/assets/download (11).php>)](/broken/pages/d06640cc8319e2f1f72ac53273047c6ca01ecc57)

### Ma réalisation

J'ai d'abord appris à utiliser le module Scapy permettant d'envoyer et d'obtenir des paquets.

J'ai constitué en quelques heures le premier script demandé : il permet de déterminer la présence des machines sur le réseau et d'obtenir l'adresse MAC d'une machine de manière passive ou active. Ces différentes fonctions implémentées peuvent être choisies avec des arguments d'exécution.

Une interface réseau n'est pas configurée par défaut pour prêter attention aux paquets qui ne sont pas destinés à son adresse MAC, donc j'ai dû modifier un paramètre dans mon ordinateur permettant cette fonctionnalité essentielle pour réaliser l'activité.

Pour réaliser mon script je me suis beaucoup inspiré d'autres scripts déjà existants sur Internet, dont un qui fonctionnait seulement pour le système d'exploitation Kali Linux ; je m'en suis servi comme base.

Finalement, pour tester mon programme il m'a fallu plusieurs machines virtuelles : deux machines qui communiquent entre elles et la troisième qui va espionner la conversation. J'ai utilisé le logiciel VMWare dans lequel j'ai configuré deux sous Debian 12 et une sous Kali Linux.

J'ai accompli ma mission : j'ai réussi à visualiser en clair les trames avec Wireshark sur la machine espion.

### Compétences acquises

* Programmer en Python
  * Intégrer des arguments d'exécution
  * Intégrer un message d'aide
  * Implémenter et utiliser des modules
* Utiliser un réseau virtuel de machines
* Générer du traffic sur un réseau
* Analyser le traffic sur un réseau

### Emplacement dossier travail

[Google Drive - Dossier Archivé - Accès Restreint](https://drive.google.com/open?id=1Me-XmWi8cSx7V2-a946FTKAzOAFIAGRR\&usp=drive_fs)

### Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) (page 72)
