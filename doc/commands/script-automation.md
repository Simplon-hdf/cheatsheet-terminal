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

## Paramètres dans un Script

Les paramètres passés à un script sont accessibles via des variables positionnelles :

*   `$0` : Nom du script.
*   `$1, $2, ..., $N` : Paramètres passés au script.
*   `$#` : Nombre total de paramètres.
*   `$@` : Liste de tous les paramètres.

Exemple: 

```bash
#!/bin/bash
echo "Le script est exécuté avec le nom : $0"
echo "Le premier argument est : $1"
echo "Le second argument est : $2"
echo "Vous avez passé $# arguments"
```

Exécution :

```bash
./mon_script.sh arg1 arg2
```

Sortie :

```bash
Le script est exécuté avec le nom : ./mon_script.sh
Le premier argument est : arg1
Le second argument est : arg2
Vous avez passé 2 arguments
```

### Structures de Contrôle

1.  Conditions (if-else)

    Vous pouvez inclure des conditions dans vos scripts pour exécuter des commandes sous certaines conditions :

    ```bash
    #!/bin/bash
    if [ $1 -eq 10 ]; then
        echo "Le premier paramètre est égal à 10"
    else
        echo "Le premier paramètre n'est pas égal à 10"
    fi
    ```

    * -eq : égal à.
    * -ne : différent de.
    * -gt : supérieur à.
    * -lt : inférieur à.

2.  Boucles (for, while, until)

    *   Boucle `for` : Pour itérer sur une série d'éléments.

    ```bash
    #!/bin/bash
    for fichier in *.txt; do
        echo "Traitement de $fichier"
    done
    ```

    *   Boucle `while` : Exécute tant qu'une condition est vraie.

    ```bash
    #!/bin/bash
    compteur=0
    while [ $compteur -lt 5 ]; do
        echo "Compteur: $compteur"
        compteur=$((compteur + 1))
    done
    ```

    * Boucle `until` : Exécute tant qu'une condition est fausse.

    ```bash
    #!/bin/bash
    compteur=10
    until [ $compteur -lt 5 ]; do
        echo "Compteur: $compteur"
        compteur=$((compteur - 1))
    done
    ```

## Fonctions dans les Scripts

Les fonctions permettent de réutiliser des parties du code :

```bash
#!/bin/bash
ma_fonction() {
  echo "Ceci est une fonction"
}
ma_fonction
```

Vous pouvez également passer des paramètres à une fonction :

```bash
#!/bin/bash
addition() {
  echo "La somme de $1 et $2 est $(( $1 + $2 ))"
}
addition 5 10
```

## Redirection et Pipes dans les Scripts

Vous pouvez rediriger la sortie ou l'entrée dans les scripts comme vous le feriez dans le terminal :

```bash
#!/bin/bash
# Redirige la sortie de la commande ls vers un fichier
ls -l > sortie.txt
```

Vous pouvez également utiliser des pipes :

```bash
#!/bin/bash
# Utilise un pipe pour filtrer la sortie de ls avec grep
ls -l | grep ".sh"
```

### Gestion des erreurs

Il est possible de gérer les erreurs dans un script Bash :

```bash
#!/bin/bash
if [ ! -f "$1" ]; then
  echo "Erreur : le fichier $1 n'existe pas."
  exit 1
fi
```

`exit` : Termine l'exécution du script avec un code de retour. Par convention, 0 signifie succès et un autre nombre indique une erreur.

## Exécution en arrière-plan et planification

* Exécuter un script en arrière-plan :

```bash
./mon_script.sh &
```

* Planification avec `cron` : Vous pouvez planifier l'exécution automatique de scripts en utilisant `cron`. Pour éditer le `cron` de votre utilisateur, utilisez :

```bash
crontab -e
```

* Ajoutez une ligne pour exécuter un script tous les jours à 2h du matin :

```bash
0 2 * * * /chemin/vers/mon_script.sh
```