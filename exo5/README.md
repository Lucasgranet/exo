# Exo 5

## Créer de vrais conteneurs applicatifs

### Serveur Web

Démarrer une image Docker permettant d'afficher la page par défaut du serveur web Nginx.

Pour cela, utiliser une image de base [Nginx](https://hub.docker.com/_/nginx/) 

Pour valider le bon fonctionnement, afficher la page `index.html` (Welcome to Nginx) dans votre navigateur internet.

### Serveur Tomcat - WAR (oldschool)

Déployer un serveur tomcat avec l'image `tomcat:7.0` avec pour applicatif ce fichier [WAR](https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war). Le Dokerfile doit être autonome.

Pour déployer le WAR, déposer le fichier dans le **répertoire** `/usr/local/tomcat/webapps/`

Accéder ensuite à l'application via votre navigateur à l'adresse suivante : `http://une-adresse:un-port/sample/`

### Serveur SpringBoot - Tomcat (The fashion way)

Cloner le projet [Spring-Boot Hello World](https://forge.granux.fr/ics/spring-hello-world) sur votre poste.

En utilisant l'image docker `maven:3-jdk-11`, réaliser une image de façon à :

- Compiler le projet UNE seule fois (à l'aide de la commande `mvn package` dans le répertoire du projet, au niveau du fichier `pom.xml`). Pour cela, il faut que les fichiers sources soit dans l'image.
  - Il ne faut pas que le projet se compile à tous les lancements de container. Uniquement durant la phase de `build` de l'image.
- De démarrer le service SpringBoot à l'aide fichier `.jar`, générer dans le répertoire `./target/` suite à la compilation, avec la commande suivante `java -jar spring-boot-0.0.1-SNAPSHOT.jar`
  - Par défaut, le serveur SpringBoot démarre sur le port 8080

**Bonus** : Optimiser la taille de l'image en supprimant tout ce qui n'est pas nécéssaire pour le démarrage du service  (le fichier `.jar` est totalement **autonome** - vous pouvez supprimer les dépendances et le code source !)

**Ceci n'est bonne une bonne image pour une production**, à ne pas reproduire. Voir la CI/CD.