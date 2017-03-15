
#Programmation : Python
* * *

![image](http://blog.teamtreehouse.com/wp-content/uploads/2013/10/photo1.jpg)

# 1. Opérations 
---------------
* 10/5 = 2.0
* 10/3 = 3.3333...
* 10 // 3 = 3 | Partie entière de la division
* 10%3 = 1 | modulo (reste de la division=


# 2. Les variables
-----------------
* Les types de données : (fonction 'type(nomVariable)' afin de connaitre le type d'une variable)

Entier = int

Réels = Float (flottants)

Les booléens qui sont soient "True" soient "False"

* Chaines de caractères : entre ' ' ou " "

Utiliser les apostrophes dans une chaine de caractères : 
    chaine = 'J\'aime le Python!'

* Astuces diverses : 
    > a,b = b,a #Permutation
    > a+=1 #Incrément (valable avec *= /=)

# 3. Structures conditionnelles 
-------------------------------
Condition if 

    if a>0: # Si a est supérieur à 0 alors
        print("a est positif")
    elif a<0: # Négatif
        print(" a est négatif")
    else: # Nul
        print("a est nul")

Les mots clés and, or et not !=

# 4. Les boucles
---------------
4.1. La boucle **while**

    while condition:
        #instruction 1
        #instruction 2
        #... 

4.2. La boucle **for**

    for element in sequence:
        #instruction 1
        #instruction 2
        # ...

4.3. **Break** et **continue**
4.3.1. Break 
Permet d'interrompre une boucle :

    while 1: # 1 est toujours vrai -> boucle infinie
        lettre = input("Tapez 'Q' pour quitter : ")
        if lettre == "Q":
            print("Fin de la boucle")
            break

4.3.2. Continue 
Permet de… continuer une boucle, en repartant directement à la ligne du while ou for.

#5. La modularité
-----------------
5.1. Les fonctions

Définir une fonction : 

    def nomFonction(param1, param2, param3=10):
        """ Docstring/aide de la fonction
        c'est le texte qui s'affichera si on fait 'help(nomFonction"""
        #Bloc d'instructions
Dans ce cas on utilise des paramètres sans les nommer, il faut alors respecter l'ordre des paramètres !

Dans l'exemple ci-dessous, param3=10. C'est la valeur qu'il prendra par défaut si l'utilisateur oublie de le mentionner.

On peut utiliser le mot clé **return** pour renvoyer une valeur.

5.2. Les modules
Un module est un bout de code qu'on importe contenant de nombreuses fonctions qui nous permet de les utiliser dans notre code.Par exemple le module *math*
Deux méthodes pour importer des modules.

5.2.1. La méthode import

    import math
    
Une fois le module *math* importé, on peut utiliser ses fonctions telles que la racine carré :

    math.sqrt(25)
    
Pour savoir quelles fonctions sont dispo dans le module *math*, il suffit d'utiliser :

    help("math")

Note : on peut créer une fonction s'appelant *sqrt*, il n'y aura pas de conflit avec *math.sqrt*

Il est possible de changer l'espace de nom "math" si on le désire :

    import math as mathematiques #on change le nom de l'espace des fonctions
    mathematiques.sqrt(25)  #on peut utiliser les fonctions initialement contenues dans "math"
    
5.2.2. La méthode from ... import ...

Si on a uniquement besoin de la fonction sqrt contenue dans math on peut l'importer elle seule de la manière suivante : 

    from math import sqrt
    sqrt(25) 

La fonction sqrt sera alors contenue dans le même espace que print (etc) et celles qu'ont crée.

5.3. Modules (=Plusieurs fichiers)
Admettons que l'on souhaite mettre nos fonctions dans un module/fichier *fichier_fonctions.py* et appeler les fonctions qui y sont dans un programme principal *fichier_main.py*. Dans ce cas il suffit d'importer le fichier *fichier_fonctions.py* au début du fichier main. Ce qui donne (si les fichiers sont dans le même repertoire :

    #a ecrire dans le fichier main
	from fichier_fonctions import * 

5.4. Tester le module dans le même fichier
Cette méthode est utile pour ne pas avoir à créer de deuxième fichier si on veut juste tester les fonctions du module/fichier correspondant *fichier_fonctions.py* : 

    if __name__ == "__main__":
    #instructions
    
5.5. Packages (=répertoire)
Les packages sont des répertoires contenant pleins de modules python. C'est utile quand il y en a beaucoup pour être bien organisé. 
Lire les informations complémentaires à l'adresse suivante, en bas de la page rubrique "Les packages" : [SiteDuZero](https://openclassrooms.com/courses/apprenez-a-programmer-en-python/pas-a-pas-vers-la-modularite-2-2)
