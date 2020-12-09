# Exo 7

## Construction d'un docker-compose

1. Construisez un docker-compose qui permettra de monter la stack suivante:

* Deux sites Wordpress (à l'aide de l'image `wordress`)
  * Un wordpress sur le port 8080, l'autre sur le port 8088
* Deux instances MySQL **différentes** (à l'aide de l'image `mysql:8`)
  * Les bases doivent **être persisté sur le disque
* Une instance PHPMyAdmin (à l'aide de l'image `phpmyadmin`)
  * Sur le port 8090
  * L'instance PHPMyAdmin **doit être préconfigurée** avec les deux instances MySQL