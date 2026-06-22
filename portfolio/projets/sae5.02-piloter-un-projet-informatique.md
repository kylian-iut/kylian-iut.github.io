# SAE5.02 Piloter un projet informatique

par [Kylian Adam](../)

## Contexte

Nous faisons une immersion à l'ENSISA, école d'ingénieur de Mulhouse. Avec les première années informatique & réseaux afin de travailler par groupe sur un projet de développement en C, d'un jeu de plateau inventé par un enseignant. Nous suivions les pratiques d'entreprise comme la gestion de projet, le versionnage de code, les tests unitaires automatisés et la documentation.

## Consigne

Durant 2 semaines avec votre équipe de 7/8 étudiant, développer en C une interface de jeu de plateau pour jouer soit contre une IA, soit contre un autre joueur, en local ou bien en réseau. Le jeu inventé spécialement : "Krojanty" comporte ses propres règles, il se joue sur un plateau d'échec virtuel. Il faudra utiliser Makefile afin de générer les tests et la documentation pour le rapport de couverture des tests. SVN sera la plateforme de versionnage du projet.

## Image

[![](<../.gitbook/assets/download (14).php>)](/broken/pages/454e1c5758b141f52f4befbee338b7ac07192038)

## Compétences acquises

* Collaborer dans une grande équipe
* Concevoir des tests automatisés
* Développer en C
* Utiliser la gestion des versions de SVN
* Créer un modèle client/serveur
* S'harmoniser sur un protocole commun

## Ma réalisation

Après avoir réparti les tâches avec mon équipe, je me suis occupé de la partie connectivité client/serveur de l'application afin de pouvoir échanger les coups de l'utilisateur avec l'application distante. Sachant que l'application de l'adversaire pouvait être conçue par une autre équipe, il a fallu collaborer avec les autres équipes afin de se mettre d'accord sur un protocole. Nous avions choisi un format ASCII/UTF-8 sur 4 octets afin d'avoir seulement l'information de la case initiale et de la case finale, par exemple : "H3B3".

Ensuite, j'ai dû concevoir une série de tests automatisés afin de vérifier que mon code réagisse correctement à ce qui est attendu. J'ai pu atteindre un taux de couverture pour mes tests sur 100% des fonctions dans mes fichiers `client.c` et `server.c`. Alors que le temps imparti était assez limité, mon équipe et moi avons réussi avec succès à mener ce projet à terme en balayant l'ensemble des attentes techniques, et nous avons décroché la deuxième place sur le podium lors de la compétition joueur contre joueur puis IA contre IA.

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf) page 162

## Emplacement du dossier travail

Dépôt GitHub

{% embed url="https://github.com/kylian-iut/Krojanty" %}
