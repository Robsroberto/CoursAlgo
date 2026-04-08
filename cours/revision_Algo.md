---
marp: false
size: 4:3
style: |
  h2, h3, p {
    font-size: 20px;
  }
  li {
    font-size:20px
  }
headingDivider: 1
header: 
paginate: true
# footer: Licence 2 Informatique &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ISI (Institut Supérieur D'Informatique) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RD
---
<img src="../isi.png" alt="ISI" width="100px">

---

# Chapitre : Révision Algorithmie
- ### Tableau
- ### Matrice
- ### Structure
- ### Tableau enregistrement
- ### Procédure
- ### Fonction
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ

---

## Tableau
### Définition
Un tableau est une structure de données qui stocke une collection d'éléments de même type, accessibles par leur indice.Pour les tableaux a une dimension c'est a dire dont les colonnes sont numérotées de 1 à N, on les appellent des vecteurs.
### Syntaxe (en pseudo-code)
1- syntaxe1
```pseudo-code
Const taille = N
Type NomVecteur = tableau[1..N] TypeVecteur
Var NomVarVect : NomVecteur
```
2- syntaxe2
```pseudo-code
Const taille = N
Var NomVarVect : tableau[1..N] TypeVecteur
```
### Exemple
```pseudo-code
Const taille = 5
Type Tableau = tableau[1..5] TypeVecteur
Var T : Tableau
Var element:entier
T[1]=10
T[2]=20
element = T[2]
```
Dans cet exemple, nous déclarons un tableau d'entiers de taille 5, y stockons des valeurs et accédons à l'élément à l'indice 2 (qui est 20).

- Écrire un programme qui permet de remplir un vecteur d'entier de 125 cellules. Le programme affiche toutes les valeurs du vecteur, ainsi que la somme de ses nombres pairs.

```pseudo-code
Programme Creation
Const N=125
Type Vecteur = tableau [1 ... N] entier
Var T: Vecteur
1, sp : entier
DEBUT
    Ecrire ("Remplissage du vecteur :")
    Pour i allant de 1 à N faire
        Ecrire ("Entrez la valeur à la cellule ", i," :")
        Lire (T[i])
    FinPour
    Ecrire ("Affichage du contenu du vecteur :")
    Pour i allant de 1 à N faire   
        Ecrire ("La valeur à la cellule ", i," du vecteur est ',T[i])
    FinPour
    Ecrire ("Calcul de la somme des nombres pairs :")
    sp <- 0
    Pour i allant de 1 à N faire
        Si (T[i] mod 2 = 0) Alors
            sp<-sp+T[i]
        FinSi
    FinPour
    Ecrire ("La somme des nombres pairs est ", sp)
FIN
```
---

## Matrice
### Définition
Une matrice est un tableau bidimensionnel, généralement utilisé pour stocker des données tabulaires ou des données à deux dimensions.Chaque ligne de la matrice se comporte comme un vecteur
### Syntaxe

```pseudo-code
Const Nombre_Lignes = valeur 1
Const Nombre_Colonnes = valeur 2
Type NomMatrice = tableau[1...Nombre_Lignes,1...Nombre_Colonnes] TypeDeDonnées
```
### Exemple
```pseudo-code
Const N = 3
Const M = 3
Type Mat = tableau[1..5] entier
Var m : Mat
Var element:entier
m[1,1]=10
m[2,2]=20
element = m[2,2]
```
Dans cet exemple, nous déclarons une matrice d'entiers de taille 3x3, y stockons des valeurs et accédons à un élément spécifique (ligne 2, colonne 2).
- Écrivez un algorithme pour additionner deux matrices.
```pseudo-code
Programme Addition Matrice
Const N = 3
Const M = 4
Matrice = tableau[1...N,1...M] entier
matrice1,matrice2, matrice_resultat: Matrice
Début
   //  les deux matrices ont la même taille
   // renseigner les valeurs de la première matrice
   Pour i allant de 1 à N Faire
      Pour j allant de 1 à M Faire
            Ecrire ("Entrez la valeur à la cellule ", i,j" :")
            Lire matrice1[i,j]
      Fin Pour
   Fin Pour

   // renseigner les valeurs de la première matrice
   Pour i allant de 1 à N Faire
      Pour j allant de 1 à M Faire
            Ecrire ("Entrez la valeur à la cellule ", i,j" :")
            Lire matrice2[i,j]
      Fin Pour
   Fin Pour

   // Additionner les matrices
   Pour i allant de 1 à N Faire
      Pour j allant de 1 à M Faire
         matrice_resultat[i,j] <- matrice1[i,j] + matrice2[i,j]
      Fin Pour
   Fin Pour

   // Afficher la matrice résultat
   Pour i allant de 1 à n Faire
      Pour j allant de 1 à m Faire
         Afficher matrice_resultat[i,j]
      Fin Pour
   Fin Pour
Fin

```
---
## Structure
### Définition
Une structure est une manière de regrouper plusieurs variables de types différents sous un même nom, permettant de créer un nouveau type de données.

### Syntaxe 
```pseudo-code
Type NomEnregistrement = Structure
    DEBUT
        champ(s):type(s)
    FIN
```
### Exemple
```pseudo-code
Type Etudiant = Structure 
    DEBUT
        nom: Chaine
        age: Entier
        note: Réel
    FIN
```
La structure "Étudiant" est définie avec des champs comme le nom, l'âge et la note. Elle peut être utilisée pour représenter des informations sur un étudiant.
- Creer un programme qui recupére les informations de 2 personnes(nom,age,pays) puis les affichent.
```pseudo-code
Programme Exemple_utilisation
Type Personne = Structure 
    DEBUT
        nom: Chaine
        age: Entier
        pays: Chaine
    FIN
Var p1,p2: Personne
DEBUT
    // Remplissage des informations pour la première personne
   p1.nom <- "Alice"
   p1.age <- 25
   p1.pays <- "France"

   // Remplissage des informations pour la deuxième personne
   p2.nom <- "Bob"
   p2.age <- 30
   p2.pays <- "États-Unis"
   // Affichage des détails des deux personnes
   Afficher "Détails de la première personne :"
   Afficher "Nom : " + p1.nom
   Afficher "Âge : " + p1.age
   Afficher "Pays d'origine : " + p1.pays

   Afficher "Détails de la deuxième personne :"
   Afficher "Nom : " + p2.nom
   Afficher "Âge : " + p2.age
   Afficher "Pays d'origine : " + p2.pays
FIN
```
---
## Tableau d'enregistrement
### Définition
Un tableau d'enregistrement est un tableau dans lequel chaque cellule est scindée (divisée) en sous-cellule et chacune d'elle peut contenir une valeur.
Le nombre de sous-cellules dépend du nombre de champs de l'enregistrement.
### Syntaxe
```pseudo-code
Type NomEnregistrement = Structure
    DEBUT
        champ(s):type(s)
    FIN
Const taille = valeur
Var NomVar : tableau [NomEnregistrement
```
### Exemples
```pseudo-code
Programme Type de Fruit
Type Fruit = structure
DEBUT
    nom:Chaine
    poids:Reel
    origine:chaine
FIN
Const nb_fruits = 5
Var tableau_de_fruits:tableau[1..nb_fruits] Fruit
```
Dans cet exemple, nous commençons par définir une structure "Fruit" qui a trois champs : nom, poids et origine. Ensuite, nous déclarons un tableau de fruits appelé "tableau_de_fruits" qui peut contenir jusqu'à 5 fruits. 
- Creer un programme qui défini la structure d'un tableau de 75 produits, puis déclarer la variable à l'associer. (Un produit est caractérisé par son code, sa référence, son prix et sa quantité). le Programme permet de remplir le tableau de produit puis l'affiche.

```pseudo-code
Programme Ges_Produit
Type Produit = structure
DEBUT
    code:entier
    ref:chaine
    pu:reels
    qte:entiers
FIN
Const nb=75
Var tab_produits:tableau[1..nb] Produit
Var i,j : entier
DEBUT
    Afficher("Remplir le tableau de produits")
    Pour i de 1 a nb FAIRE
        Afficher("Donner le code")
        Saisir(tab_produits[i].code)
        Afficher("Donner la reference")
        Saisir(tab_produits[i].ref)
        Afficher("Donner le prix unitaire")
        Saisir(tab_produits[i].pu)
        Afficher("Donner la quantité")
        Saisir(tab_produits[i].qte)
    FinPour
    Afficher("le tableau de produits")
    Pour i de 1 a nb FAIRE
        Afficher(" le code",tab_produits[i].code)
        Afficher(" la reference",tab_produits[i].ref)
        Afficher(" le prix unitaire",tab_produits[i].pu)
       Afficher(" la quantité",tab_produits[i].qte)
    FinPour
FIN
```
---
## Proccedure
### Définition
Une procédure est un bloc de code autonome qui peut recevoir des paramétresen entrée et effectue une tâche spécifique.

### Syntaxe 
```pseudo-code
Procédure nom_procedure ( types de parametres argument:type(s))
DEBUT
//corps de la procedure
FIN

```
### Exemple
```pseudo-code
Procedure afficher_nombre (Donnees/Resultat n:entier)
DEBUT
    Ecrire ("Le nombre est ",n,".")
FIN
```
- Écrire une procédure qui reçoit 2 valeurs entières et qui détermine leurs sommes

```pseudo-code
Procedure somme (Donnees x,y:entier Resultat s:entier)
DEBUT
    s <- x+y
FIN
```
---
## Fonction
### Définition
Une fonction et un module qui peut recevoir des paramètres en donnée, mais elle a une obligation de renvoyer un seul résultat.
### Syntaxe
```pseudo-code
Fonction nom_fonction (Donnees arguments : type(s)): TypeDeRetour
DEBUT
    // corps de la fonction
    retourner(expression)
FIN
```
### Exemple
```pseudo-code
Fonction addition (x, y:entier):entier
Var S:entier
DEBUT
    S = x + y
    RETOURNER(S)
FIN
```
- Écrire une fonction qui reçoit une valeur entière puis détermine son factoriel.
```pseudo-code
fonction facto (Donnees N: entier):entier
Var i, f:entier
DÉBUT
    f <- 1
    POUR i allant de 1 à N Faire
        f<-f* i
    FINPOUR
    Retourner (f)
FIN
```
