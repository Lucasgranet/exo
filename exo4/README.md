# Exo 4

## Part 1 Création d'image docker

1. Créer une image ayant pour base `centos:7`
2. Installer le package `sl` dans cette image.
   1. Vous aurez besoin pour cela d'installer au **préalable** le package `epel-release` (Google It)
3. Réalisez une première version de l'image qui lance le binaire `sl`
   1. Lors du `docker run` vous allez devoir préciser une option pour permettre à `sl` de dessiner sur votre terminal.
   2. Le tag de l'image doit être `:1st`
5. Faites en sorte que le train vol par défaut mais que **si** on précise un autre argument (lors du `docker run`), **seul** ces arguements seront appliqués (les arguments peuvent se cumuler):
   - Pour voler, `sl` a besoin de l'argument `-F`
   - Pour que les gens crient "à l'aide", préciser l'argurment `-a`
   - **Attention**, je veux pouvoir utiliser l'argument `-a` sans forcément avoir l'argument `-F`
   - Pour un petit train, utiliser l'argument `-l`
   - Le tag de cette version de l'image sera `:2nd`
6. En plus des comportements précédents, faites en sorte que le train soit de petite taille.
   - Le tag de cette image sera `:3rd`

## Part 2 Publication d'une image Docker

1. Créer un compte sur le registry Docker-Hub.

2. Créer un nouveau repository dans votre namespace.

3. Publier l'image créé dans la partie 1 dans ce repository (poussez les trois versions de votre image dans le même repository):
   - Vous allez devoir vous logger au registry DockerHub. Utilisez la commande `docker login` pour effectuer cette authentification .
   - Pour créer une nouvelle image/tag, vous pouvez utiliser la commande `docker tag <img_src:tag> <img_dst:tag>`
   - Utiliser la commande `docker push <img:tag>` pour publier votre image sur le registry par défault (docker.hub)

4. Supprimer les image en local.

   `docker rmi <img_name>`

5. Téléchager l'image avec le tag `:3rd`.

6. Vérifier que votre image est toujours fonctionnel.

### Avec l'un de vos voisins

1. Publier l'image avec le tag `:1st` en prenant soin de mettre le tag `:latest`.

2. Votre voisin télécharge cette image avec le tag `:latest`. Votre voisin doit voir la première version de votre image sur son poste.

3. Publier l'image avec le tag `:3rd` en prenant soin de mettre le tag `:latest`.

4. Votre voisin doit mettre à jour votre image avec le tag `:latest`.


\* Si vous n'êtes pas sur votre PC personnel, **supprimer** le fichier `~/.docker/config.json` afin de ne pas laisser votre compte sur la machine !