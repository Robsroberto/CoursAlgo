# SERIE EXERCICES SUR LES TABLEAUX ET MATRICES

---

**INSTITUT SUPERIEUR D'INFORMATIQUE**  
Annee academique : 2025/2026  
Classe : LICENCE INFORMATIQUE 1  
Professeur : M. Robert DIASSE  
Contacts : 77 338 64 43 -- ldiasse@groupeisi.com

---

## TABLEAUX A UNE DIMENSION

**Exercice 1 :**
Soit un tableau de N entiers. Ecrire un module qui calcule et affiche la somme, la
moyenne, le plus grand element et le plus petit element du tableau.

```
Const N = 30
```

---

**Exercice 2 :**
Soit un tableau de N entiers. Ecrire un module qui compte et affiche le nombre
d'elements positifs, le nombre d'elements negatifs et le nombre d'elements nuls.
Le module doit egalement afficher le pourcentage de chaque categorie par rapport
au nombre total d'elements.

```
Const N = 25
```

---

**Exercice 3 :**
Soit un tableau de N entiers et une valeur VAL donnee en parametre. Ecrire un
module qui compte le nombre d'occurrences de VAL dans le tableau et affiche
les indices auxquels elle apparait. Si VAL est absente du tableau, le signaler.

```
Const N = 20
```

---

**Exercice 4 :**
Soit un tableau de N etudiants. Ecrire un module qui affiche la liste complete des
etudiants, calcule le nombre d'etudiants ayant la moyenne (moyenne >= 10),
determine l'etudiant ayant la meilleure note et celui ayant la moins bonne note,
et calcule l'ecart entre ces deux notes.

```
Etudiant (matricule, nom, prenom, note)
Const N = 40
```

---

**Exercice 5 :**
Soit un tableau de N produits. Ecrire un module qui calcule la valeur totale du
stock (somme des prix * quantites), determine le produit le plus cher, le produit
dont le stock est le plus eleve et le produit dont la valeur en stock est la plus
faible.

```
Produit (code, libelle, prix, quantite)
Const N = 50
```

---

**Exercice 6 :**
Soit un tableau de N voitures. Ecrire un module qui affiche toutes les voitures,
puis compte le nombre de voitures dont l'annee de mise en circulation est
superieure ou egale a 2020, et calcule la moyenne d'age de toutes les voitures.
On prend 2025 comme annee de reference.

```
Voiture (immatriculation, marque, modele, annee_circulation, prix)
Const N = 30
```

---

**Exercice 7 :**
Soit deux tableaux A et B de respectivement NA et NB entiers. Ecrire un module
qui cree un troisieme tableau C contenant d'abord tous les elements de A suivis
de tous les elements de B, puis compte dans C le nombre d'elements communs
aux deux tableaux initiaux (elements qui apparaissent dans A et dans B).

```
Const NA = 15, NB = 10
```

---

**Exercice 8 :**
Soit un tableau de N employes. Ecrire un module qui calcule le salaire brut de
chaque employe, sachant que le salaire brut = salaire_base + prime_anciennete.
La prime d'anciennete est calculee comme suit :
- anciennete < 3 ans  : 0% du salaire de base
- 3 <= anciennete < 7 ans : 10% du salaire de base
- 7 <= anciennete < 15 ans : 20% du salaire de base
- anciennete >= 15 ans : 35% du salaire de base

Le module doit afficher la liste avec les salaires bruts et determiner l'employe
le mieux remunere.

```
Employe (matricule, nom, prenom, salaire_base, anciennete)
Const N = 35
```

---

## MATRICES A DEUX DIMENSIONS

**Exercice 9 :**
Soit une matrice de L lignes et C colonnes d'entiers. Ecrire un module qui calcule
et affiche la somme de chaque ligne, la somme de chaque colonne, et la somme
totale de tous les elements de la matrice.

```
Const L = 5, C = 6
```

---

**Exercice 10 :**
Soit une matrice carree d'ordre N d'entiers. Ecrire un module qui calcule et
affiche la somme des elements de la diagonale principale, la somme des elements
de la diagonale secondaire, et determine si ces deux sommes sont egales.

```
Rappel : element sur la diagonale principale si (i = j)
         element sur la diagonale secondaire si (i + j = N + 1)
Const N = 6
```

---

**Exercice 11 :**
Soit une matrice de L lignes et C colonnes d'entiers. Ecrire un module qui
determine et affiche :
- l'indice de la ligne dont la somme est la plus elevee
- l'indice de la colonne dont la somme est la plus elevee
- la valeur maximale et sa position (ligne, colonne) dans la matrice

```
Const L = 8, C = 10
```

---

**Exercice 12 :**
Soit une matrice de L lignes et C colonnes d'entiers. Ecrire un module qui affiche
uniquement les elements se trouvant sur les bordures de la matrice (premiere
ligne, derniere ligne, premiere colonne et derniere colonne), en evitant de
compter deux fois les coins.

```
Const L = 6, C = 8
```

---

**Exercice 13 :**
Soit une matrice carree d'ordre N d'entiers. Ecrire un module qui verifie si la
matrice est symetrique par rapport a la diagonale principale, c'est-a-dire si
M[i][j] = M[j][i] pour tout i et j. Le module retourne un booleen.

```
Const N = 5
```

---

**Exercice 14 :**
Soit une matrice de L lignes et C colonnes d'entiers et une valeur VAL donnee
en parametre. Ecrire un module qui recherche VAL dans la matrice et retourne
sa premiere position (numero de ligne et numero de colonne). Si VAL est
absente, le signaler.

```
Const L = 7, C = 9
```

---

**Exercice 15 :**
Soit une matrice A de L lignes et C colonnes d'entiers. Ecrire un module qui
cree une matrice B de C lignes et L colonnes qui est la transposee de A
(B[j][i] = A[i][j]), puis affiche les deux matrices.

```
Const L = 4, C = 6
```

---

**Exercice 16 :**
Soit une matrice carree d'ordre N d'entiers. Ecrire un module qui verifie si la
matrice est un carre magique. Une matrice carree est magique si la somme de
chaque ligne, de chaque colonne et des deux diagonales sont toutes egales.
Le module retourne un booleen et affiche la somme magique si le carre est
valide.

```
Const N = 3
```

---

## TABLEAUX ET MATRICES D'ENREGISTREMENTS

**Exercice 17 :**
Soit un tableau de N classes, chacune representee par un tableau de M etudiants.
Ecrire un module qui calcule la moyenne generale de chaque classe, determine
la classe ayant la meilleure moyenne generale et le nombre total d'etudiants
ayant la moyenne sur l'ensemble des classes.

```
Etudiant (matricule, nom, prenom, moyenne)
Const N = 6, M = 30
```

---

**Exercice 18 :**
Soit une matrice de L lignes et C colonnes de produits. Chaque cellule represente
un produit stocke dans un entrepot. Ecrire un module qui calcule la valeur totale
de chaque ligne (assimilee a une zone de stockage), determine la zone dont la
valeur totale est la plus elevee et compte le nombre de produits en rupture de
stock (quantite = 0) dans l'ensemble de la matrice.

```
Produit (reference, libelle, prix_unitaire, quantite)
Const L = 5, C = 8
```

---

**Exercice 19 :**
Soit un tableau de N employes et un tableau de M projets. Chaque employe
possede un code_projet indiquant le projet auquel il est affecte. Ecrire un module
qui, pour chaque projet, affiche le nombre d'employes affectes et la masse
salariale correspondante (somme des salaires des employes du projet).

```
Employe (matricule, nom, prenom, salaire, code_projet)
Projet (code, intitule, budget)
Const N = 50, M = 8
```

---

**Exercice 20 :**
Soit un tableau de N etudiants et une matrice de notes de dimensions N lignes
et M colonnes, ou chaque ligne i correspond aux M notes de l'etudiant i. Ecrire
un module qui :
- calcule la moyenne de chaque etudiant (moyenne des M notes)
- determine le nombre d'etudiants admis (moyenne >= 10), en rattrapage
  (7 <= moyenne < 10) et redoublants (moyenne < 7)
- affiche le classement de chaque etudiant selon sa moyenne en indiquant
  sa categorie (Admis, Rattrapage, Redoublant)

```
Etudiant (matricule, nom, prenom)
Const N = 30, M = 6
```

---

*M. Robert DIASSE : ENSEIGNANT -- CHERCHEUR -- CONSULTANT EN INGENIERIE, SYSTEMES INFORMATIQUES ET DATA SCIENCE*