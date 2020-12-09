# Exo 4

## Part 1 Création d'image docker

1. Créer une image ayant pour base `centos:7`
2. Installer le package `sl` dans cette image.
   1. Vous aurez besoin pour cela d'installer au préalable le package `epel-release`
3. Lancer l'image afin que le train s'affiche à l'écran
4. Faites en sorte que le comportement par défaut de l'image est d'affiché le train.
5. Faites en sorte que le train vol par défaut mais que si on précise un autre argument, qu'il change de comportement 
   1. Pour voler, sl a besoin de l'argument `-F`
   2. Pour que les gens crient "à l'aide", préciser l'argurment `-a`
   3. Attention, je veux pouvoir utiliser l'argument `-a` sans forcément avoir l'argument `-F`

## Part 2 Publication d'une image Docker

1. Créer un compte sur le registry Docker-Hub

2. Créer un nouveau repository dans votre namespace

3. Publier l'image créé dans la partie 1 dans ce repository

4. Supprimer l'image en local

   `docker rmi <img_name>`

5. Téléchager votre image

6. Vérifier que votre image est toujours fonctionnel