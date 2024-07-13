# Fankem 

## Alex
### Eazytraining 18th DevOps Bootcamp
#### Period: march-april-may

##### Application
Il est question ici pour nous de deployer une application denomme "api", celle ci elle affiche la liste des etudiants et leurs ages.
Notre devoir est divise en 3 parties:
- La premiere partie consiste a utiliser les commandes docker pour afficher la liste des etudiants
- La deuxieme partie consiste a afficher la liste des etudiants en utilisant docker-compose
- La troisieme partie consiste a pusher notre image cree sur le registry

###### Plan de travail 
Nous allons mettre en place les commandes des differents conteneurs 
- Nous allons faire le tag de notre image apres run le conteneur api qui nous permettra de voir la liste des etudiants
- Nous allons mettre en place un conteneur en utilisant le docker-compose.yml pour l affiche des infos des etudiants
- Nous allons creer le registry avec le docker-compose-registry pour pouvoir heberger notre application en local
 
#### Elaboration du plan de travail

Partie 1
 
1-Ici nous avons faire le build de l image en precisant le version et le contexte

![Image Build](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/3f9eb99a-f167-42ce-8444-5dd886c81d22)

2- Run l image de l application qui a ete builde et creer le conteneur

![Image run](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/79bc432e-e254-47af-a29f-8ff5891d1cb2)


3- Cette commande permet de voir et confirmer que notre conteneur a bien ete cree 

![docker images](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/e1d7361d-a5fd-4078-96a5-2515df96a57a)


4- Cette commande permet de renvoyer la liste des etudiants et leurs ages

![commande curl](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/34852167-12fa-401b-9756-59dc8e9150d7)


Partie 2 Infrastructure as code

1 - Il nous d abord demande dans l exercice de supprimer les differents conteneurs qui ont ete cree car les ports de ses conteneurs peuvent faire obstables a d'autres conteneurs 

![docker stop and remove api](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/76c780f1-7a82-40a9-9c4b-f6f7a7e1fdc5)

2- le contast ici fait sur la commande du docker-compose.yml que nous allons run 

![docker-compose yml image+build](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/ca886206-cce3-4d8d-b87e-b8e83cde01c0)

![docker compose yml](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/148bfa84-21c2-4cc1-a78d-ee9960c5bbe4)

3- Une fois que la commande du docker-compose.yml a fonctionne nous pouvons interroge le port notre application(Backend) par le port 8000  

![Commande pour avoir la liste student](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/2647059b-489f-4334-a349-b3c5c0b8d0c4)

4- Apres avoir interroge notre apllication par le port 8000, nous faisons un constat simple que la liste des etudiants ne s affiche pas, nous modifie le dossier website plus precisement le fihier indexe.php

![List of student](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/5dea8665-eb73-43f1-9751-440ee3be46e5)


Partie 3 Docker Registry

1- Dans cette partie nous devons push a l'application sur un registry en utilisant le docker-compose-registry(docker-compose de l image) de joxit. Ensuite nous devons ajoute le port de pour pouvoir communiquer avec l'application  (registry:2.8.2) 

![Run Registry](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/078e1b6f-9e71-46a0-98cc-7a378c341ce9)

2- Le constat est e registry a bien ete cree et il faut push l'image en local

![Registry](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/6b06e2cf-c744-4ea6-b76c-a83e2f0cfc00)

3- Avant de push l image sur le registry en local il faudra d'abord la tag en utilisant la commande 

![Tag registry](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/bf9b7a8c-3db9-4871-90e9-c77b6852e034)

4- Une fois le tag a ete fait l image pourra etre push sur le registry en local

![Push l image du registry](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/03d28d68-627a-46cd-a864-84e83e5fbf26)

5- Affiche de l'image sur le registry en local

![registry details](https://github.com/alexzaza17/mini-projet-docker/assets/159175882/38ec098e-e0ca-4789-96ed-b6579ae2d932)


![describe2](https://github.com/user-attachments/assets/68965496-cf47-4666-acad-1961026e20e7)

