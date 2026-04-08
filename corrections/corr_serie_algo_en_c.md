Exercice 1 :

```c
#include <stdio.h>

int main() {
    FILE *fichier;
    int nombre, somme = 0, count = 0;

    fichier = fopen("NOMBRES.BIN", "rb");

    if (fichier == NULL) {
        printf("Erreur lors de l'ouverture du fichier.\n");
        return 1;
    }

    while (fread(&nombre, sizeof(int), 1, fichier)) {
        printf("%d ", nombre);
        somme += nombre;
        count++;
    }

    fclose(fichier);

    printf("\nSomme : %d\n", somme);
    printf("Moyenne : %.2f\n", (float)somme / count);

    return 0;
}
```

Exercice 2 :

```c
#include <stdio.h>
#include <string.h>

#define MAX_LENGTH 20

int main() {
    FILE *fichier;
    char mot[MAX_LENGTH + 1];
    int count = 0, totalLength = 0;

    fichier = fopen("MOTS.TXT", "w");

    if (fichier == NULL) {
        printf("Erreur lors de la création du fichier.\n");
        return 1;
    }

    printf("Saisissez les mots (max 20 caractères) :\n");

    while (1) {
        scanf("%s", mot);

        if (mot[0] == '*') {
            break;
        }

        fprintf(fichier, "%s\n", mot);
        count++;
        totalLength += strlen(mot);
    }

    fclose(fichier);

    printf("Nombre de mots : %d\n", count);
    if (count > 0) {
        printf("Longueur moyenne des mots : %.2f\n", (float)totalLength / count);
    }

    return 0;
}
```
Exercice 2 (suite) :

```c
#include <stdio.h>
#include <string.h>

#define MAX_LENGTH 20

int main() {
    FILE *fichier, *fichier10;
    char mot[MAX_LENGTH + 1];

    fichier = fopen("MOTS.TXT", "r");
    fichier10 = fopen("MOTS10.TXT", "w");

    if (fichier == NULL || fichier10 == NULL) {
        printf("Erreur lors de l'ouverture/création des fichiers.\n");
        return 1;
    }

    while (fscanf(fichier, "%s", mot) == 1) {
        if (strlen(mot) > 10) {
            fprintf(fichier10, "%s\n", mot);
        }
    }

    fclose(fichier);
    fclose(fichier10);

    return 0;
}
```

Exercice 3 :

```c
#include <stdio.h>

typedef struct {
    int matricule;
    char nom[50];
    char prenom[50];
    float moyenne;
} Etudiant;

int main() {
    FILE *fichierAdmis;
    Etudiant T[100];
    int i, nbAdmis = 0;

    // Remplir le tableau T (vous devez le remplir avec des données)

    fichierAdmis = fopen("ADMIS", "wb");

    if (fichierAdmis == NULL) {
        printf("Erreur lors de la création du fichier ADMIS.\n");
        return 1;
    }

    for (i = 0; i < 100; i++) {
        if (T[i].moyenne >= 10) {
            fwrite(&T[i], sizeof(Etudiant), 1, fichierAdmis);
            nbAdmis++;
        }
    }

    fclose(fichierAdmis);

    printf("Nombre d'etudiants admis : %d\n", nbAdmis);

    return 0;
}
```
Exercice 4 :

```c
#include <stdio.h>

typedef struct {
    int jour, mois, annee;
} TDate;

typedef struct {
    char discipline[50];
    char faculte[50];
} TDiscipline;

typedef struct {
    char nom[50];
    char prenom[50];
    TDate dateN;
    TDiscipline filiere;
} TEtudiant;

int main() {
    FILE *fichierEtudiant, *fichierF1, *fichierF2;
    TEtudiant etudiant;
    char faculteRecherche[50];

    // Remplir le fichier FEtudiant (vous devez le remplir avec des données)

    fichierEtudiant = fopen("FEtudiant", "wb");

    if (fichierEtudiant == NULL) {
        printf("Erreur lors de la création du fichier FEtudiant.\n");
        return 1;
    }

    // Code pour remplir le fichier FEtudiant (vous devez le remplir avec des données)

    fclose(fichierEtudiant);

    // Eclater le fichier FEtudiant en deux fichiers, F1 et F2

    fichierEtudiant = fopen("FEtudiant", "rb");
    fichierF1 = fopen("F1", "wb");
    fichierF2 = fopen("F2", "wb");

    if (fichierEtudiant == NULL || fichierF1 == NULL || fichierF2 == NULL) {
        printf("Erreur lors de l'ouverture/création des fichiers.\n");
        return 1;
    }

    printf("Entrez le nom de la faculté de recherche : ");
    scanf("%s", faculteRecherche);

    while (fread(&etudiant, sizeof(TEtudiant), 1, fichierEtudiant) == 1) {
        if (strcmp(etudiant.filiere.faculte, faculteRecherche) == 0) {
            fwrite(&etudiant, sizeof(TEtudiant), 1, fichierF1);
        } else {
            fwrite(&etudiant, sizeof(TEtudiant), 1, fichierF2);
        }
    }

    fclose(fichierEtudiant);
    fclose(fichierF1);
    fclose(fichierF2);

    return 0;
}
```
Exercice 5 :

```c
#include <stdio.h>

int main() {
    FILE *fichierF1, *fichierF2, *fichierG;
    int valeurF1, valeurF2;

    fichierF1 = fopen("F1", "rb");
    fichierF2 = fopen("F2", "rb");
    fichierG = fopen("G", "wb");

    if (fichierF1 == NULL || fichierF2 == NULL || fichierG == NULL) {
        printf("Erreur lors de l'ouverture/création des fichiers.\n");
        return 1;
    }

    while (fread(&valeurF1, sizeof(int), 1, fichierF1) == 1) {
        fseek(fichierF2, 0, SEEK_SET); // Rembobiner le fichier F2 au début pour chaque valeur de F1

        while (fread(&valeurF2, sizeof(int), 1, fichierF2) == 1) {
            if (valeurF1 % valeurF2 == 0) {
                fwrite(&valeurF1, sizeof(int), 1, fichierG);
                break; // Sortir de la boucle intérieure une fois trouvé un multiple
            }
        }
    }

    fclose(fichierF1);
    fclose(fichierF2);
    fclose(fichierG);

    return 0;
}
```

Exercice 6 :

```c
#include <stdio.h>
#include <string.h>

int main() {
    FILE *fichierF1, *fichierF2, *fichierF3;
    char motF1[50], motF2[50];

    fichierF1 = fopen("F1", "r");
    fichierF2 = fopen("F2", "r");
    fichierF3 = fopen("F3", "w");

    if (fichierF1 == NULL || fichierF2 == NULL || fichierF3 == NULL) {
        printf("Erreur lors de l'ouverture/création des fichiers.\n");
        return 1;
    }

    while (fscanf(fichierF1, "%s", motF1) == 1) {
        fseek(fichierF2, 0, SEEK_SET); // Rembobiner le fichier F2 au début pour chaque mot de F1

        int motExiste = 0;

        while (fscanf(fichierF2, "%s", motF2) == 1) {
            if (strcmp(motF1, motF2) == 0) {
                motExiste = 1;
                break; // Sortir de la boucle intérieure si le mot existe dans F2
            }
        }

        if (!motExiste) {
            fprintf(fichierF3, "%s\n", motF1);
        }
    }

    fclose(fichierF1);
    fclose(fichierF2);
    fclose(fichierF3);

    return 0;
}
```
