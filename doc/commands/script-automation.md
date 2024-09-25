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



