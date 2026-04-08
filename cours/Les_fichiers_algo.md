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
# Chapitre : Les Fichiers

### Introduction aux fichiers
### 


---


## Introduction

Les fichiers sont essentiels pour stocker et manipuler des données de manière persistante en informatique. Ce cours détaillera la création et la manipulation de fichiers en utilisant les fonctions de base : `Ouvrir`, `Fermer`, `Lire`, `Ecrire`, `Supprimer`, `Reecrire`, et `EOF` (Fin de Fichier).

## Utilité des Fichiers en Algorithmie

Les fichiers sont utilisés pour stocker des données de manière permanente. Ils permettent de :

- Sauvegarder des informations entre différentes exécutions d'un programme.
- Partager des données entre différentes parties d'un programme.
- Importer/exporter des données depuis/vers d'autres programmes.

## Concept de Base : Ouverture et Fermeture de Fichiers

### Ouverture de Fichier

La fonction `Ouvrir` permet d'ouvrir un fichier avant de travailler avec lui. On spécifie le nom du fichier, le mode d'ouverture (lecture, écriture, ou lecture/ecriture).

**Exemple :**
```pseudo-code
fichier <- Ouvrir("exemple.txt")
```

### Fermeture de Fichier

Une fois les opérations terminées, le fichier doit être fermé à l'aide de la fonction `Fermer`.

**Exemple :**
```pseudo-code
Fermer(fichier)
```
## Syntaxe de déclaration d'un fichier

## Écriture et Lecture de Fichiers

### Écriture dans un Fichier

Pour écrire dans un fichier, on utilise la fonction `Ecrire` qui prend un tampon (chaîne de caractères) et le fichier.

**Exemple :**
```pseudo-code
tampon <- "Nouvelle ligne à écrire"
Ecrire(fichier, tampon)
```

### Lecture d'un Fichier

Pour lire depuis un fichier, on utilise la fonction `Lire` qui lit une ligne à la fois dans un tampon.

**Exemple :**
```pseudo-code
tampon <- ""
Lire(fichier, tampon)
```

### Fin de Fichier (EOF/FF)

La condition `EOF` (End of File) est utilisée pour vérifier si la fin du fichier est atteinte.

**Exemple :**
```pseudo-code
TantQue Non EOF(fichier) Faire
    Lire(fichier, tampon)
    Afficher tampon
FinTantQue
```

## Manipulation de Fichiers

### Réécriture dans un Fichier

La fonction `Reecrire` permet de réécrire un tampon dans un fichier existant.

**Exemple :**
```pseudo-code
Reecrire(fichier, "Nouveau contenu du fichier")
```

### Suppression d'une Ligne dans un Fichier

La fonction `Supprimer` permet de supprimer une ligne spécifique d'un fichier.

**Exemple :**
```pseudo-code
Supprimer(fichier, "Ligne à supprimer")
```

## Exercices Corrigés

### Exercice 1 : Écriture et Lecture

Écrire un programme qui demande à l'utilisateur de saisir une phrase, l'écrit dans un fichier, puis lit le fichier et affiche la phrase.

**Solution :**
```pseudo-code
fichier <- Ouvrir("exemple.txt", "ECRITURE", "SEQUENTIEL")

tampon <- Saisir("Saisissez une phrase : ")
Ecrire(fichier, tampon)

Fermer(fichier)

fichier <- Ouvrir("exemple.txt")LECTURE

TantQue Non EOF(fichier) Faire
    Lire(fichier, tampon)
    Afficher "Phrase lue depuis le fichier : " + tampon
FinTantQue

Fermer(fichier)
```

### Exercice 2 : Réécriture de Fichier

Écrire un programme qui réécrit le contenu d'un fichier avec une nouvelle ligne.

**Solution :**
```pseudo-code
fichier <- Ouvrir("exemple.txt", "REECRITURE", "SEQUENTIEL")

Reecrire(fichier, "Nouveau contenu du fichier")

Fermer(fichier)
```

### Exercice 3 : Suppression de Ligne

Écrire une fonction qui supprime une ligne spécifique d'un fichier.

**Solution :**
```pseudo-code
fonction SupprimerLigneSpecifique(fichier, ligne_a_supprimer)
    temp <- Ouvrir("temp.txt", "ECRITURE", "SEQUENTIEL")

    TantQue Non EOF(fichier) Faire
        Lire(fichier, tampon)
        Si tampon ≠ ligne_a_supprimer Alors
            Ecrire(temp, tampon)
        Fin Si
    FinTantQue

    Fermer(fichier)
    Fermer(temp)

    Renommer("temp.txt", "exemple.txt")
Fin fonction
```

Ce cours détaillé sur la création et la manipulation de fichiers en pseudo-code utilise les fonctions de base pour assurer la clarté et la compréhension. Les exemples et exercices corrigés vous permettront de pratiquer ces concepts et d'améliorer vos compétences en manipulation de fichiers en algorithmie.