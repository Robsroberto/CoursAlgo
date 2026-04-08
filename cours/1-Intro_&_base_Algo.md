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
footer: Licence 2 Informatique &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ISI (Institut Supérieur D'Informatique) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RD
---
<img src="../isi.png" alt="ISI" width="100px">

# **Résumé  Cours1 – Algorithmique (Licence 1)**

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

<img src="../Algorithms.jpg" alt="ISI" width="200px">



### *Document de rappel*

---

# **1. Introduction à l’Algorithmique**

L’informatique étudie le **traitement automatique de l’information** à l’aide d’un ordinateur.
Un **algorithme** est une suite finie et ordonnée d’instructions permettant de **résoudre un problème** de manière **claire, efficace et non ambiguë**.

### Propriétés d’un bon algorithme :

* **Précis** : chaque étape est clairement définie.
* **Fini** : il se termine après un nombre limité d’opérations.
* **Correct** : produit un résultat juste.
* **Général** : fonctionne pour n’importe quelles données valides.

Exemple simple :

```pseudo
Saisir a, b
s ← a + b
Afficher s
```

---

# **2. Structure d’un programme (en algorithmique)**

Un programme algorithmique est généralement structuré en trois parties :

### **1) Partie entête**

Nom du programme (identificateur).

### **2) Partie déclarative**

On y déclare :

* des **constantes**,
* des **types**, **Prototypes**
* des **variables**,
* des **modules** (procédures ou fonctions).

### **3) Corps du programme principal**

Contient les instructions exécutées par le programme.

Modèle :

```pseudo
Programme NomProgramme

// Déclarations
Constante(s)
Type(s)
Variable(s)

Debut
    // Instructions
Fin
```

---

# **3. Types de données et Identificateurs**

## **3.1. Notion de type**

Chaque variable possède un **type**, qui définit :

* la **nature** de la donnée (entier, réel…)
* les **valeurs autorisées**,
* la **taille mémoire** associée.

### **Types élémentaires en algorithmique**

* **entier**
* **réel**
* **caractère**
* **chaîne**
* **booléen**

### **Types composés**

(Ils seront étudiés plus tard) :

* énumération
* intervalle
* enregistrement (structure)

---

## **3.2. Identificateurs**

Un identificateur est un **nom symbolique** donné à une variable, constante, type ou module.

### Règles :

1. Doit être **alphabétique ou alphanumérique**.
2. **Ne commence jamais par un chiffre**.
3. Ne contient **ni espaces**, ni tiret `-`.
   (On utilise `_` pour séparer des mots).
4. Ne doit pas être un **mot réservé**.

Exemples **corrects** :

```
age, Nom, moyenne_finale, X2
```

Exemples **incorrects** :

```
4exo   (commence par un chiffre)❌
test-note (tiret interdit)❌
mon nom  (espace interdit)❌
```

---

# **4. Constantes**

Une constante est un identificateur dont la **valeur ne change pas** durant l’exécution.

Syntaxes :

```pseudo
Const NomConst = valeur
Const type NomConst = valeur
```

Exemples :

```pseudo
Const Pi = 3.14
Const Nom = "ISI"
Const Taux = 0.18
```

---

# **5. Variables**

La variable peut changer de valeur pendant le programme.

Syntaxes :

```pseudo
Var identificateur : type
Var ident1, ident2 : type
```

Exemples :

```pseudo
Var age : entier
Var nom : chaîne
Var x, y : réel
Var test : booléen
```

---

# **6. Instructions d’entrée / sortie**

## **6.1. Entrée (lire / saisir)**

Permet d’entrer des valeurs dans le programme.

Syntaxe :

```pseudo
Lire(variable)
Saisir(variable)
```

Exemple :

```pseudo
Saisir(a, b)
```

## **6.2. Sortie (affichage)**

Pour afficher sur l’écran :

```pseudo
Afficher("Bonjour")
Afficher(x)
```

---

# **7. Opérateurs**

## **7.1. Arithmétiques**

| Symbole | Signification  |
| ------- | -------------- |
| +       | Addition       |
| -       | Soustraction   |
| *       | Multiplication |
| div     | Division Entiere|
| /       | Division Réelle|
| mod     | Modulo (reste) |
| sqr     | Carré          |
| sqrt    | Racine Carré   |
| abs     | Valeur Absolue |

## **7.2. Opérateurs de comparaison**

| Opérateur | Signification     |
| --------- | ----------------- |
| =         | égal              |
| <> ou !=  | différent         |
| >         | supérieur         |
| <         | inférieur         |
| >=        | supérieur ou égal |
| <=        | inférieur ou égal |

## **7.3. Opérateurs logiques**

| Opérateur | Signification |
| --------- | ------------- |
| ET        | et logique    |
| OU        | ou logique    |
| NON       | négation      |

Exemple :

```pseudo
Si (age >= 18 ET carte = vrai) Alors
    Afficher("Autorisé")
FinSi
```

---

# **8. Affectation**

L’affectation consiste à donner une valeur à une variable.

Syntaxe :

```pseudo
variable ← expression
```

Exemples :

```pseudo
x ← 5
y ← x + 3
msg ← "Bonjour"
```

---

# **9. Exemple complet**

```pseudo
Programme Somme

Var a, b, s : entier

Début
    Afficher("Entrer deux nombres :")
    Saisir(a, b)
    s ← a + b
    Afficher("La somme est : ", s)
Fin
```

---

# **Résumé pour mémorisation**

* Un **algorithme** = suite d’instructions pour résoudre un problème.
* Un programme a 3 parties : **entête, déclarations, corps**.
* Types élémentaires : entier, réel, caractère, chaîne, booléen.
* Un identificateur ne commence jamais par un chiffre.
* Constante : valeur fixe.
* Variable : valeur qui change.
* `Saisir()` : entrée.
* `Afficher()` : sortie.
* `←` : affectation.
* Opérateurs : arithmétiques, comparaisons, logiques.
