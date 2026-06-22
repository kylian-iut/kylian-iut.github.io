# SAE1.03 Découvrir un dispositif de transmission

par [Kylian Adam](../)

## Contexte

S'initier c'est commencer par les bases. Nous pourrions étudier le tout premier réseau ARPANET datant de 1969, mais son fonctionnement est différent de ce qu'on trouve aujourd'hui. La technologie à évolué, et malheureusement le temps nous manque. Il serait plus important de considérer le fonctionnement actuel d'un réseau informatique type entreprise, puisque cela va nous servir très rapidement, je rappel la possibilité de faire une alternance dès la seconde année d'étude. Un exemple simple et à porté : le réseau du campus de l'IUT de Colmar. On s'y connecte chaque jours, que ce soit les étudiants, les enseignants ou le personnel. Une connexion sans-fil s'effectue entre notre téléphone, notre tablette ou notre laptop pour que nous puissions accéder aux ressources de l'IUT, et à Internet également. Quels sont les dispositifs mis en places et comment fonctionnent t'ils ?

## Consigne

{% stepper %}
{% step %}
### Simuler le réseau étudié
{% endstep %}

{% step %}
### Effectuer la liaison filaire entre les baies de brassages C100 et C102

Connectoriser un noyau, partie femelle de part et d'autre du câble, et connectoriser les parties mâles d'un cordon RJ45.
{% endstep %}

{% step %}
### Positionner correctement un point d'accès Wi-Fi
{% endstep %}

{% step %}
### Effectuer des mesures des signaux
{% endstep %}
{% endstepper %}

## Image

[![](<../.gitbook/assets/download (13).php>)](/broken/pages/0073cf8bd5f3cdb3621d524115127675d41e207b)

## Ma réalisation

J'ai commencé par conenctorisé un cordon RJ45 grâce à la méthode que m'a ensigné une intervenante Mme. Bendele. Ce cordon a permis de relier le point d'accès de notre groupe au noyau de la baie de brassage.

J'ai découvert le logiciel Acrylic Wi-Fi Analyser qui permet de faire des captures des signaux en se déplacant avec un ordinateur dans un bâtiment. J'ai appris à m'en servir, en faisant plusieurs test.

Dans l'IUT de Colmar j'ai effectué des captures avec Acrylic dans le bâtiment C, devant le bâtiment C et dans la Bibliothèque Universitaire. Cela m'a permis d'obtenir une heatmap du SSID Eduroam.

J'ai effectuer des mesures diverses et varié : électrique par PoE, de débits avec la transmission d'un fichier en FTP, et de puissance avec l'antenne intégré de mon laptop, que j'ai ensuite comparé à l'antenne intégré de mon smartphone.

## Compétences acquises

* Matériel
  * Connectoriser en RJ45
  * Utiliser le dispositif PoE
  * Effectuer des mesures électriques
* Logiciel
  * Simuler une topologie
  * Capturer et étudier des signaux 2,4GHz et 5GHz
  * Mesurer un débit de données
* Social
  * Collaborer en groupe
  * Rédiger un compte rendu
  * Présentation

## Emplacement du dossier travail

Google Drive - Dossier partagé - Accès Public

{% embed url="https://drive.google.com/drive/folders/1NCN9kYIEHbeRKUkoDZGOePFxxK7OFuOq?usp=sharing" %}

## Source

[Programme national RÉSEAUX ET TÉLÉCOMMUNICATIONS](https://www.iut-rt.net/wp-content/uploads/2023/01/spe617_annexe22_1426160.pdf), page 70
