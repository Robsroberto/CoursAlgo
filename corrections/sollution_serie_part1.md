### Exercice 1 :

```pseudo-code
Algorithme AfficherNombres
Var
    Fe: F_Entier
    somme, nombre, moyenne: réel

Debut
    somme <- 0
    nombre <- 0
    
    Ouvrir(Fe) Lecture
    
    TantQue Non FinDeFichier(Fe) Faire
        Lire(nombre, Fe)
        Afficher nombre
        somme <- somme + nombre
        nombre <- nombre + 1
    FinTantQue
    
    Fermer(Fe)
    
    Si nombre > 0 Alors
        moyenne <- somme / nombre
        Afficher "Somme : " + somme
        Afficher "Moyenne : " + moyenne
    Sinon
        Afficher "Le fichier est vide."
    FinSi
Fin
```

### Exercice 2 :

#### 1) Création du fichier MOTS.TXT :

```pseudo-code
Algorithme CreerFichierMots
Var
    Fe: F_Entier
    mot: chaine

Debut
    Ouvrir(Fe) Ecriture
    
    Repeter
        Saisir(mot)
        Si mot ≠ "*" Alors
            Ecrire(mot, Fe)
        FinSi
    Jusqu'a mot = "*"
    
    Fermer(Fe)
Fin
```

#### 2) Affichage du nombre de mots et de la longueur moyenne :

```pseudo-code
Algorithme StatistiquesFichierMots
Var
    Fe: F_Entier
    mot: chaine
    nombreMots, sommeLongueurs: entier
    longueurMoyenne: réel

Debut
    Ouvrir(Fe) Lecture
    
    nombreMots <- 0
    sommeLongueurs <- 0
    
    TantQue Non FinDeFichier(Fe) Faire
        Lire(mot, Fe)
        nombreMots <- nombreMots + 1
        sommeLongueurs <- sommeLongueurs + Longueur(mot)
    FinTantQue
    
    Fermer(Fe)
    
    Si nombreMots > 0 Alors
        longueurMoyenne <- sommeLongueurs / nombreMots
        Afficher "Nombre de mots : " + nombreMots
        Afficher "Longueur moyenne : " + longueurMoyenne
    Sinon
        Afficher "Le fichier est vide."
    FinSi
Fin
```

#### 3) Création du fichier MOTS10.TXT :

```pseudo-code
Algorithme CreerFichierMots10
Var
    Fe1, Fe2: F_Entier
    mot: chaine

Debut
    Ouvrir(Fe1) Lecture
    Ouvrir(Fe2) Ecriture
    
    TantQue Non FinDeFichier(Fe1) Faire
        Lire(mot, Fe1)
        Si Longueur(mot) > 10 Alors
            Ecrire(mot, Fe2)
        FinSi
    FinTantQue
    
    Fermer(Fe1)
    Fermer(Fe2)
Fin
```

### Exercice 3 :

```pseudo-code
Algorithme CopierAdmisDansFichier
Var
    FeEntree, FeSortie: F_Entier
    etudiant: Etudiant

Debut
    Ouvrir(FeEntree) Lecture
    Ouvrir(FeSortie) Ecriture
    
    TantQue Non FinDeFichier(FeEntree) Faire
        Lire(FeEntree, etudiant)
        Si etudiant.Moyenne >= 10 Alors
            Ecrire(FeSortie, etudiant)
        FinSi
    FinTantQue
    
    Fermer(FeEntree)
    Fermer(FeSortie)
Fin
```

### Exercice 4 :

#### Remplir le fichier FEtudiant :

```pseudo-code
Algorithme RemplirFichierEtudiant
Var
    Fe: F_Entier
    etudiant: Etudiant

Debut
    Ouvrir(Fe) Ecriture
    
    Repeter
        Saisir(etudiant.Nom, etudiant.Prenom)
        Saisir(etudiant.DateN.Jour, etudiant.DateN.Mois, etudiant.DateN.Annee)
        Saisir(etudiant.Filiere.Discipline, etudiant.Filiere.Faculte)
        
        Ecrire(Fe, etudiant)
        
        Saisir("Voulez-vous ajouter un autre étudiant ? (O/N)", reponse)
    Jusqu'a reponse ≠ "O"
    
    Fermer(Fe)
Fin
```

#### Éclater le fichier FEtudiant :

```pseudo-code
Algorithme EclaterFichierEtudiant
Var
    FeEntree, Fe1, Fe2: F_Entier
    etudiant: Etudiant

Debut
    Ouvrir(FeEntree) Lecture
    Ouvrir(Fe1) Ec

riture
    Ouvrir(Fe2) Ecriture
    
    TantQue Non FinDeFichier(FeEntree) Faire
        Lire(FeEntree, etudiant)
        
        Si etudiant.Filiere.Faculte = "FEI" Alors
            Ecrire(Fe1, etudiant)
        Sinon
            Ecrire(Fe2, etudiant)
        FinSi
    FinTantQue
    
    Fermer(FeEntree)
    Fermer(Fe1)
    Fermer(Fe2)
Fin
```

### Exercice 5 :

#### 1) Construction du fichier G :

```pseudo-code
Algorithme ConstruireFichierG
Var
    F1, F2, G: F_Entier
    valeur, multiple: entier

Debut
    Ouvrir(F1) Lecture
    Ouvrir(F2) Lecture
    Ouvrir(G) Ecriture
    
    TantQue Non FinDeFichier(F1) Faire
        Lire(F1, valeur)
        
        TantQue Non FinDeFichier(F2) Faire
            Lire(F2, multiple)
            Ecrire(G, valeur)
            Ecrire(G, multiple)
        FinTantQue
        
        RetournerDebut(F2)
    FinTantQue
    
    Fermer(F1)
    Fermer(F2)
    Fermer(G)
Fin
```

#### 2) Générer le fichier H :

```pseudo-code
Algorithme GenererFichierH
Var
    G, H: F_Entier
    valeur, occurrences, valeurPrecedente: entier

Debut
    Ouvrir(G) Lecture
    Ouvrir(H) Ecriture
    
    occurrences <- 0
    
    TantQue Non FinDeFichier(G) Faire
        Lire(G, valeur)
        
        Si valeur ≠ valeurPrecedente Alors
            Si occurrences > 0 Alors
                Ecrire(H, valeurPrecedente)
                Ecrire(H, occurrences)
            FinSi
            
            occurrences <- 1
            valeurPrecedente <- valeur
        Sinon
            occurrences <- occurrences + 1
        FinSi
    FinTantQue
    
    Fermer(G)
    Fermer(H)
Fin
```