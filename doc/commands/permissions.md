### Commandes liées aux permissions

Les permissions en ligne de commande sont un système qui permet de contrôler l'accès aux fichiers et répertoires.
Elles sont généralement définies via une notation que l'on appelle *octale* 

**La notation octale**

Pour définir les permissions d'un fichier, on utilise généralement trois chiffres octaux, un pour chaque catégorie d'utilisateurs.

Le premier chiffre représente le **propriétaire** (user), le second représente le **groupe** (group), et le dernier représente **tout le reste** (others)

*Exemple : une permission pourra avoir le nombre 644, nous verrons plus tard à quel(s) droit(s) elle correspond*

**Calcul des permissions**
Chaque droit représente une valeur : 
- Lecture (r) : valeur de 4
- Écriture (w) : valeur de 2
- Exécution (x) : valeur de 1

Si l'on veut donner les permissions de lecture **et** d'écriture à quelqu'un, il suffira alors d'additionner les nombres **4** *(lecture)*, et de **2** *(écriture)*, ce qui donne **6**.

### La commande à utiliser pour gérer les permissions

La commande `chmod` permet de modifier les permissions en utilisant la notation octale :

`chmod 644 nomdufichier.txt`

Cette commande attribue les droits :
- de lecture et écriture au propriétaire (6)
- de lecture seule au groupe (4)
- également de lecture seule aux autres utilisateurs (4)

<p align="center"><img src="assets/img/octal-notation.png"/></p>

*Note : la valeur 7 existe : elle donne l'accès à tous les droits : lecture, écriture et exécution*

