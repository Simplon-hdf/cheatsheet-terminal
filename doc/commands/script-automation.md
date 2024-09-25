# Script et automatisation

## Intro

Les scripts Bash (.bash) sont des **fichiers texte contenant une séquence de commandes à exécuter** dans l'interpréteur de commandes Bash sous Linux. Ils permettent d'automatiser des tâches, de **réutiliser des commandes** fréquemment utilisées et de créer des processus complexes.

## Création d'un script bash

1.  **Création du fichier script**
    
    Utilisez un éditeur de texte (comme nano ou vim) pour créer un fichier texte qui contiendra les commandes à exécuter.

    ```bash
    nano mon_script.sh
    ```

2.  **Début du script**

    La première ligne du script doit indiquer quel interpréteur de commandes doit être utilisé pour exécuter le script. Pour Bash, c'est généralement :

    ```bash
    #!/bin/bash
     ```

3. **Ajout de commandes**

    Ensuite, vous pouvez ajouter des commandes que vous souhaitez exécuter. Par exemple :

    ```bash
    #!/bin/bash
    echo "Bonjour, bienvenue dans mon script Bash !"
    ls -l
    ```

## Exécution d'un Script Bash

1. Donner les droits d'exécution au script

    Avant de pouvoir exécuter le script, vous devez le rendre exécutable avec la commande chmod :

    ```bash
    chmod +x mon_script.sh
    ```

2. Exécution du script

    Vous pouvez ensuite exécuter le script en précisant son chemin relatif ou absolu.

    *   Si le script se trouve dans le répertoire courant :

        ```bash
        ./mon_script.sh
        ```

    *   Si le script est dans un autre répertoire, utilisez le chemin complet ou relatif :

        ```bash
        /chemin/vers/mon_script.sh
        ```

## Commentaires dans un Script

Les commentaires commencent par un `#` et ne sont pas interprétés par Bash. Ils sont utiles pour documenter le script.

```bash
#!/bin/bash
# Ce script affiche les fichiers du répertoire courant
echo "Liste des fichiers :"
ls -l
```

## Variables dans les Scripts Bash

Vous pouvez définir des variables dans un script Bash pour stocker des valeurs et les réutiliser :

```bash
#!/bin/bash
nom="Alice"
echo "Bonjour, $nom !"
```

Les variables sont accessibles en utilisant le symbole `$`. Il est important de ne pas utiliser d'espaces autour du signe `=` lors de l’affectation des valeurs.

