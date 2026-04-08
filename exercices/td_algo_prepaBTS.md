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

# TD : Algo
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

<!-- <img src="js.jpeg" alt="ISI" width="50px"> -->

### **EXERCICE 1 (Liste monodirectionnelle + Tableau)**
Une université souhaite identifier les étudiants nouvellement inscrits à un master. Les anciens inscrits sont référencés dans une liste monodirectionnelle triée par identifiant. Chaque nouvel inscrit est saisi dans un tableau.
Chaque étudiant est caractérisé par :

* un identifiant (entier),
* un nom (chaîne),
* un prénom (chaîne),
* une spécialité (chaîne),
* une moyenne (réel).

1. Écrire un module qui transfère dans une liste les étudiants présents dans le tableau mais absents de la liste existante.
2. Trier la liste obtenue selon l’ordre croissant des moyennes.

---

### **EXERCICE 2 (Matrice + Enregistrements)**

Une entreprise suit l’assiduité de ses salariés sur un mois de travail. Les présences sont notées dans une matrice de 30 lignes et 20 colonnes où chaque valeur vaut 1 si le salarié est présent, 0 sinon.

Chaque salarié est défini par :

* un identifiant (entier),
* un nom (chaîne),
* un poste (chaîne).

1. Écrire un module qui calcule pour chaque salarié le nombre total de jours d’absence.
2. Afficher les salariés ayant manqué plus de 5 jours.

---

### **EXERCICE 3 ( Fichier + Liste monodirectionnelle)**

Une administration veut extraire les dossiers des usagers ayant demandé une aide sociale. Les informations sont conservées dans un fichier d’organisation séquentielle.
Chaque usager est défini par :

* un numéro (entier),
* un nom (chaîne),
* une commune (chaîne),
* un revenu mensuel (réel).

Écrire un module qui construit une liste monodirectionnelle contenant les usagers dont le revenu est inférieur au SMIC(100 000).

---

### **EXERCICE 4 (Tableaux + Traitement croisé)**

Un établissement conserve les données de ses enseignants dans deux tableaux, l’un pour les professeurs titulaires, l’autre pour les vacataires. Chaque enregistrement contient :

* un matricule (entier),
* un nom (chaîne),
* une matière (chaîne).

1. Écrire un module qui construit un nouveau tableau contenant les enseignants figurant dans les deux tableaux.
2. Supprimer les doublons et trier le tableau résultant par ordre alphabétique de la matière.

---

<!-- ### **EXERCICE 5 ( Liste doublement chaînée + Date)**

Un centre de formation souhaite suivre les formations en cours. Chaque formation est enregistrée dans une liste doublement chaînée et caractérisée par :

* un identifiant (entier),
* un thème (chaîne),
* une date de début (jour/mois/année),
* une date de fin (jour/mois/année).

1. Écrire un module qui supprime toutes les formations terminées à la date du jour.
2. Afficher la liste mise à jour par ordre croissant de date de début. -->

---

### **EXERCICE 5 ( Matrice + Liste monodirectionnelle)**

Une banque suit les opérations de ses guichets répartis dans 10 agences sur 7 jours.
Les montants quotidiens sont enregistrés dans une matrice.

1. Construire une liste contenant les agences dont la somme des opérations sur la semaine dépasse un certain seuil fixé.
2. Afficher les agences concernées.

---

### **EXERCICE 6 ( Fichier + Tableau)**

Un cabinet médical gère les données de ses patients dans un fichier séquentiel.
Chaque patient est caractérisé par :

* un numéro (entier),
* un nom (chaîne),
* un prénom (chaîne),
* une date de naissance (jour/mois/année),
* une pathologie (chaîne).

1. Écrire un module qui transfère dans un tableau les patients nés après 1980.
2. Trier ce tableau selon l’ordre alphabétique du nom.

---

### **EXERCICE 7 (Liste circulaire + Enregistrement + tableau)**

Un service d’entretien suit les interventions prévues dans les bureaux. Ces interventions sont stockées dans une liste circulaire.
Chaque intervention est caractérisée par :

* un numéro (entier),
* un libellé (chaîne),
* une date prévue (jour/mois/année),
* un responsable (chaîne).

1. Mettre dans un tableau toutes les interventions dont la date est antérieure à la date du 15/05/2025.
2. Afficher la liste mise à jour.

---

### **EXERCICE 8 (Liste monodirectionnelle + Liste circulaire +Fichier)**

Une agence immobilière stocke les logements déjà loués dans une liste monodirectionnelle triée par code.
Les logements disponibles sont enregistrés dans un fichier séquentiel.

Chaque logement contient :

* un code (chaîne),
* une localisation (chaîne),
* un type (chaîne),
* un prix (entier).
* un statuts : "loués" ,"Non encor loués".

1. Créer un module qui identifie les logements disponibles **non encore loués** et les stocke dans un tableau.
2. Créer un module qui met dans un liste circulaire tout les logements qui se trouve a dakar et dont le prix est d'au moins 150 000

---
<!-- 
### **EXERCICE 9 (Tableau + Fichier)**

Une entreprise conserve ses commandes clients dans un tableau. Un fichier contient les produits livrés.
Chaque commande est définie par :

* un numéro (entier),
* une référence produit (chaîne),
* une quantité (entier).

1. Afficher les commandes non encore livrées.
2. Calculer la valeur totale des commandes restantes.

--- -->

### **EXERCICE 9 (Liste doublement chaînée + Tri)**

Un lycée gère les bulletins trimestriels de ses élèves dans une liste doublement chaînée.
Chaque bulletin contient :

* un identifiant élève (entier),
* un nom (chaîne),
* une moyenne (réel),
* une mention (chaîne).

1. mettre dans une matrice tous les bulletins ayant une moyenne inférieure à 10.
2. Trier les bulletins restants par mention puis par moyenne décroissante.

---

### **EXERCICE 10 ( Liste monodirectionnelle + Fichier)**

Une direction de la jeunesse conserve les bénéficiaires d’un programme d’aide dans un fichier. Une liste chaînée contient les bénéficiaires actifs.

Chaque bénéficiaire contient :

* un code (entier),
* un nom (chaîne),
* un statut (chaîne),
* une date de dernière activité (jour/mois/année).

Écrire un module qui ajoute dans une nouvelle liste les bénéficiaires inactifs depuis plus de 12 mois.

---

<!-- ### **EXERCICE 11 (Matrice + Tableau)**

Une mairie gère la fréquentation de ses bibliothèques via une matrice de 12 lignes (mois) et 10 colonnes (bibliothèques). Chaque case représente le nombre de visiteurs.

1. Afficher la bibliothèque ayant le plus faible total annuel.
2. Créer un tableau des bibliothèques dépassant un seuil fixé. -->

---

<!-- ### **EXERCICE 11 (Liste monodirectionnelle + Tri)**

Un centre social recense les bénéficiaires dans une liste monodirectionnelle. Chaque bénéficiaire est défini par un numéro, un nom, un âge et un type d’aide.

1. Supprimer de la liste les bénéficiaires de moins de 18 ans.
2. Trier la liste restante par type d’aide puis par nom.

--- -->

### **EXERCICE 11(Fichier + Liste)**

Un centre médical conserve les rendez-vous dans un fichier. Chaque rendez-vous contient :

* un identifiant (entier),
* un nom (chaîne),
* une date (jour/mois/année).

1. Extraire dans une liste les rendez-vous prévus pour la semaine du lundi 12/05.
2. Afficher cette liste par date croissante.

---

<!-- ### **EXERCICE 12 ( Liste circulaire + Enregistrement)**

Un responsable de formation suit les évaluations prévues dans une liste circulaire. Chaque évaluation a :

* un code (chaîne),
* une matière (chaîne),
* une date (jour/mois/année).

1. Supprimer toutes les évaluations annulées.
2. Afficher les évaluations restantes, triées par date.

--- -->

### **EXERCICE 12(Tableau + Fusion sans doublons)**

Deux départements d’une entreprise stockent les données de leurs produits dans deux tableaux. Chaque produit contient :

* un code (chaîne),
* un libellé (chaîne),
* un stock (entier).

1. Fusionner les deux tableaux dans un tableau unique sans doublons.
2. Trier le tableau final par code croissant.

---

<!-- ### **EXERCICE 13( Liste doublement chaînée + Condition)**

Un réseau de librairies conserve les commandes dans une liste doublement chaînée. Chaque commande contient un code, un client, un livre, une quantité et un statut.

1. Supprimer toutes les commandes annulées.
2. Afficher la liste mise à jour par nom de client.

--- -->

### **EXERCICE 13(Matrice + Condition de seuil)**

Une usine de production surveille la température de 10 machines sur 30 jours. Chaque température est notée dans une matrice.

1. Déterminer les machines ayant dépassé 80° au moins 5 fois.
2. Afficher leurs indices et leur moyenne.

---

### **EXERCICE 14 (Liste monodirectionnelle + Comparaison)**

Un syndicat enregistre ses membres actifs dans une liste monodirectionnelle et dispose d’un tableau des adhérents à jour de cotisation.
Chaque membre est caractérisé par un identifiant, nom, profession.

1. Écrire un module qui affiche les membres actifs **non à jour** de cotisation.
<!-- 2. Trier ces membres par profession. -->
