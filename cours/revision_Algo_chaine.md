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
paginate: 
# footer: Licence 2 Informatique &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ISI (Institut Supérieur D'Informatique) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RD
---
<img src="../isi.png" alt="ISI" width="100px">

---

# Chapitre : Révision Les chaines de Caractéres
- ### Définition
- ### Fonctions dédiée aux chaines
    - ### Longueur
    - ### Extraction
    - ### Concaténation
    - ### Recherche
    - ### Conversion
    - ### Caractére et code ASCII

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ


# Révision Algorithmique : Chaînes de Caractères

## Définition

 Une chaîne de caractères est une séquence de caractères, tels que du texte, utilisée pour stocker et manipuler des données textuelles. Les chaînes de caractères sont largement utilisées en programmation pour représenter du texte, des noms, des messages, etc.

## Syntaxe 

- **Déclaration** : Une chaîne de caractères est déclarée en utilisant le mot-clé approprié, par exemple :
```pseudo-code
 chaine: Chaine 
 chaine <- "Bonjour"
```


## Fonctions Dédiées aux Chaînes de Caractères

### fonction de Longueur 
`Long(chaine)` ou `longueur(chaine)`

- **Fonction** : `Long(chaine)` retourne la longueur de la chaîne (le nombre de caractères qu'elle contient).

- **Exemple** : 
   ```pseudo-code
   texte <- Long("Bonjour")
   // texte contiendra la valeur 7
   ```

### Fonction d'extraction
`Souschaîne(chaine_principale,chaine_secondaie)` ou `SSchaine(chaine_principale,chaine_secondaie)`
- **Fonction** : `SSchaine(chaine, debut, longueur)` extrait une sous-chaîne de la chaîne, en commençant à partir de la position de départ pour une certaine longueur.

- **Exemple** : 
   ```pseudo-code
   sous_chaine <- SSchaine("Exemple", 3, 4)
   // sous_chaine contiendra "empl"
   ```

###  Fonction de Concaténation
`+` ou `||` ou `Concat( chaine)`
- **Opérateurs** : Les opérateurs `+`, `||`, ou la fonction `Concat(chaine1, chaine2)` sont utilisés pour concaténer(fusionner) des chaînes.

- **Exemple** : 
   ```pseudo-code
   chaine_concatenee <- "Bonjour" + "Monde"
   // chaine_concatenee contiendra "BonjourMonde"
   ```

### Fonction de Recherche
`Rang(chaine, sous_chaine)`
- **Fonction** : `Rang(chaine, sous_chaine)` renvoie la position de la première occurrence de la sous-chaîne dans la chaîne.

- **Exemple** : 
   ```pseudo-code
   position <- Rang("Bonjour", "jour")
   // position contiendra la valeur 4
   ```

### Fonction de Conversion de Chaînes

- **Fonction** : Les fonctions `CvChaine(valeur)` convertissent une valeur en chaîne de caractères, et `CvNombre(chaine)` convertissent une chaîne en valeur numérique.

- **Exemple** : 
   ```pseudo-code
   chaine_numero <- CvChaine(42)
   // chaine_numero contiendra "42"
   ```

### Code et Caractère

- **Fonctions** : `Code(caractere)` renvoie le code ASCII d'un caractère, et `Car(code)` renvoie le caractère correspondant à un code ASCII donné.

- **Exemple** : 
   ```pseudo-code
   code_a <- Code('A')
   // code_a contiendra la valeur 65
   ```

## Exercices

**Exercice 1 : Longueur**

Calculer et afficher la longueur de la chaîne "Exercice".

**Solution** :
```pseudo-code
longueur <- Long("Exercice")
Afficher(longueur)
```

**Exercice 2 : Concaténation**

Concaténer les chaînes "Bonjour" et "Monde" et afficher le résultat.

**Solution** :
```pseudo-code
resultat <- "Bonjour" + " " + "Monde"
Afficher(resultat)
```

**Exercice 3 : Extraction de Sous-chaîne**

Extraire et afficher la sous-chaîne "monde" de la chaîne "Bonjour, monde".

**Solution** :
```pseudo-code
sous_chaine <- SSchaine("Bonjour, monde", 9, 5)
Afficher(sous_chaine)
```

**Exercice 4 : Conversion de Chaînes**

Convertir la chaîne "42" en nombre et l'afficher.

**Solution** :
```pseudo-code
nombre <- CvNombre("42")
Afficher(nombre)
```

**Exercice 5 : Recherche dans une Chaîne**

Rechercher la position de la sous-chaîne "abc" dans "defabcgh".

**Solution** :
```pseudo-code
position <- Rang("defabcgh", "abc")
Afficher(position)
```

**Exercice 6 : Code ASCII**
Obtenir le code ASCII du caractère 'X' et afficher le résultat.

**Solution** :
```pseudo-code
code_x <- Code('X')
Afficher(code_x)
```

**Exercice 7 : Caractère à partir du Code ASCII**
Obtenir le caractère correspondant au code ASCII 97 et l'afficher.

**Solution** :
```pseudo-code
caractere_a <- Car(97)
Afficher(caractere_a)
```
