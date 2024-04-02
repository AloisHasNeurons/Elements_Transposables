README module Projet Bioinformatique 2023-2024 Partie Projet
NOM : VINCENT
PRENOM : Aloïs

**************************
*  Vendredi 22 mars 2024 *
**************************
Début du projet : 

$ cd Bureau/Projet-Bio_Info/Projet/ 

Téléchargement des deux fichiers :
- /TAIR10_TE.fas
- /TAIR10_Transposable_Elements.txt

Détermination du nombre de séquences dans le fichier, en comptant le nombre d'en-têtes de Fasta '>' :

$ grep '>' TAIR10_TE.fas | wc -l
31189

Pour le 05/04 : faire le tableau bilan numérique (finir l'étape 1)

**************************
*  Mardi 02 avril 2024   *
**************************
- Quelle est la liste des familles des éléments transposables ?
- Combien y-a-t-il de copies par famille d’ET ?

$ awk '{print $5}' TAIR10_Transposable_Elements.txt  |sort| uniq -c

cette commande permet d'afficher la liste des familles, ainsi que leur nombre d'occurences
On crée un tableau bilan numérique : 	

$ awk '{print $5}' TAIR10_Transposable_Elements.txt  |sort| uniq -c | sort -k 1,1 -n -r > tabRecap.txt

On utilise 'sort -k 1,1 -n -r' pour trier par la première colonne et ainsi avoir les familles les plus récurrentes en premier dans le tableau








