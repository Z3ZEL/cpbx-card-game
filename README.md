# JEU DE CARTE CPBX

## Tutoriel : Ajouter vous-même des cartes à jouer

Pour rajouter une carte :

 Retourner dans le dossier racine du projet et aller dans card_data. Une fois dedans créer un nouveau fichier :
 ![](https://raw.githubusercontent.com/Z3ZEL/cpbx-card-game/main/tutorial_img/Capture%20d%E2%80%99%C3%A9cran%202021-12-12%20174522.png)
 
 Vous serez rediriger sur une page comme cela :
  ![](https://raw.githubusercontent.com/Z3ZEL/cpbx-card-game/main/tutorial_img/Capture%20d%E2%80%99%C3%A9cran%202021-12-12%20174642.png)
  
 Renommer votre fichier avec le nom de la carte en majuscule et sans ponctuations et espaces comme ci dessus à la place des XXXX. Cela s'appelle un tag. N'oubliez pas de rajouter .json à la fin pour mettre l'extension json à votre fichier.
 
 Dans la partie editeur de texte rajouter le code ci-dessous :
 
```json
 
 {
        "name" : "Blaudez",
        "description":"Le big boss",
        "string_effect" : "Une fois posé il peu kill n'importe quelle carte sur le terrain de l'adversaire",
        "raw_effect" : "event:INVOKE/type:KILL/target:ANY/targetGenre:ANY",
        "rarity" : "COMMON",
        "force" : 10,
        "intelligence" : 10,
        "charisme" : 10,
        "genre" : "MALE",
        "type" : "PROFESSOR",
        "price" : 10,
        "tag" : "BLAUDEZ"
}   
``` 

Puis remplacer par ce que vous voulez

**tag** doit etre EXACTEMENT pareil que le nom de votre fichier sans le .json

**genre** = soit MALE ou FEMALE

**type** = soit PROFESSOR ou STUDENT

**force,intelligence,charisme** max 10

**price** cout de la carte

**rarity** "COMMON","UNCOMMUN","RARE","VERY_RARE","ULTRA_RARE" => rareté de la carte

**raw_effect** est un peu particulier car il est sensible sur la syntaxe
event:INVOKE le event indique la variable à modifier et INVOKE est la valeur de cette variable (en majuscule) il faut la séparer par ":" et de même il faut separer chaque variable par "/" vous pouvez aussi ajouter plusieurs valeurs à une même variable en les séparants par des "," comme par exemple "target:RIGHT,LEFT"

Ici est détailler toutes les variables disponibles ainsi que leur valeurs disponibles.


Quand vous êtes satisfait il vous suffit de descendre en bas de la page et de cliquer sur "Propose File"


##Rajoutons l'image:

Retouner dans la racine du projet et allez dans le dossier card_img comme ceci :
![](https://raw.githubusercontent.com/Z3ZEL/cpbx-card-game/main/tutorial_img/Capture%20d%E2%80%99%C3%A9cran%202021-12-12%20174718.png)

Cliquer ici non pas sur AddFile mais sur UPLOAD FILE et uploadez une image ayant pour nom EXACTEMENT le même nom que votre fichier .json le tag le fichier doit être en .png . Cliquer sur "Propose File" en bas de page et c'est terminé pour cette étape

##Référence
Retourner dans le dossier racine et ouvre le fichier reference.txt et éditez-le et rajouter sur un ligne le nom de vos fichier. Le tag toujours.

