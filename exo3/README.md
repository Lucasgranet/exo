# Exo 3

## Gestion des containers

1. Démarrer un container en arrière plan. L'image a utilisé est `jpetazzo/clock`

2. Afficher et suivez la sortie de logs (l'équivalent de tail -f) sur votre terminal. 

3. Démarrer un nouveau container avec la même image, en arrière plan.

   1. Trouver un moyen de stocker l'identifiant du container pour pouvoir le manipuler par la suite (deux solutions possible)

4. Stopper le container que vous avez créé à l'étape 3 (avec l'aide de l'information stocker dans le 3.1)

5. Afficher uniquement les containers qui sont en fonctionnement

   Il ne doit en avoir qu'un seul en fonctionnement.

6. Redémarrer le container que vous avez stoppé (toujours à l'aide du 3.1)

7. Créer un script/function Shell permettant d'arreter tous les containers qui sont en fonctionnement. 

8. Afficher les containers stoppés.

## Assez malin ?

1. Démarrer un container en arrière plan. L'image a utilisé est `jpetazzo/clock`

2. Trouvez au moins un moyen de **stopper** le container sans passer par les commandes `docker stop`, `docker pause`, `docker kill`.

