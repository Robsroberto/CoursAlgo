
**Exercice  1 :**

Soit le fichier NOMBRES.BIN qui contient une liste de nombres entiers. Écrire un algorithme qui 
affiche les nombres du fichier, leur somme et leur moyenne. 
**Exercice  2 :**    
1) Écrire  un  algorithme  qui  crée  le  fichier  MOTS.TXT  contenant  une  série  de  mots  (longueur 
maximale d'un mot: 20  caractères).  La saisie des  mots se terminera  à l'introduction du symbole 
'*' qui ne sera pas écrit dans le fichier.
2) Écrire  un  algorithme  qui  affiche  le  nombre  de  mots  ainsi  que  la  longueur  moyenne  des  mots 
contenus dans le fichier MOTS.TXT. 
3) Écrire un algorithme qui crée  un deuxième fichier MOTS10.TXT contenant les mots du fichier 
MOTS.TXT de plus de 10 caractères. 

**Exercice  3 :**  


Considérons le type enregistrement suivant : 
```pseudo-code
Type Etudiant = Structure
Debut
    Matricule : entier ;
    Nom, Prenom : chaine ;
    Moyenne : réel ;
Fin;
``` 
Soit T un tableau d’au plus 100 étudiants.  Ecrire un algorithme permettant de recopier tous les étudiants admis appartenant à T dans un fichier 
ADMIS de type étudiant. Un étudiant est admis si sa moyenne est supérieure ou égale 10. 

**Exercice  4 :**

Soient les enregistrements suivants : 
```pseudo-code
Type TDate = Structure 
Debut
    Jour, mois, année : entier ;  
Fin;
TDiscipline = Structure  
debut
    Discipline : chaine ; 
    Faculté : chaine ; 
Fin;  
TEtudiant =  Structure
Debut
    Nom, prenom : chaine ;   
    DateN : TDate ;   
    Filiere : TDiscipline ;   
Fin;
```
 Soit FEtudiant un fichier d’étudiants. Ecrire un algorithme qui permet de : - Remplir le fichier FEtudiant. 
- Eclater le fichier FEtudiant en deux fichiers, F1 (étudiants de la faculté ‘FEI’) et F2 (étudiants 
des autres facultés). 

**Exercice  5 :**    
Soient  F1  et  F2  deux  fichiers  d’entiers  strictement  positifs  et  sans  répétition.  Ecrire un 
algorithme qui construit (crée) un fichier G d’entiers tel que G contient pour chaque valeur de F1 
la valeur et tous ses multiples appartenant à F2 (F1 et F2 sont supposés existants). 

Exemple : 

F1 :   3    10    20    17 

F2 :   3     6   19   60    40    30 

G  :   3    3    6    60    30   10   60   40   30    20    60    40   17 
  
<!-- 2) Ecrire  un  algorithme  qui  permet  à  partir  du  fichier  résultat  (G)  de  générer  un  autre  fichier  (H) 
contenant toutes les valeurs du fichier (G) (sans répétition) avec leur nombre. 

Exemple :

 H :    3  2        6  1        60  3        30  2        10  1        40  2        20  1        17  1  -->
<!-- Exercice  6 :    
Soit F un fichier d’entiers représentant des séquences de nombres séparées par un ou plusieurs zéro. 
Ecrire un algorithme qui réalise les traitements suivants : 
1) A  partir  de  F  (fichier  existant),  crée  un  fichier  G  contenant  pour  chaque  séquence,  la 
moyenne des nombres qui la constituent. 
2) Puis, Supprimer les valeurs nulles du fichier G.

 Exemple : 
 
 F :  0  0  1   4   3   7   0   0   0   6   -9   2   7   -6   0   -10   3  0   0 G :                 3,75                            0,00                  -3,50 
 
 G :                 3,75                                                     -3,50  -->
**Exercice  6 :**  

Soient F1 et F2 deux fichiers de chaînes de caractères. Chaque chaîne représente un mot. Ecrire un 
algorithme qui construit un fichier F3, tel que F3 contient les mots de F1 qui n’existent pas dans F2. 