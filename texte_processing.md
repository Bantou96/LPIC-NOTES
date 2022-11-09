### Combinaison 
- cat file1 file2 : concaténer
- join -t':'(délimiteur) -i(ignorer la casse) -num_col_file1 num -num_col_file2 num file1 file2 : jointure ou fusion de colonne
- paste file1 file2 : regroupement ligne par ligne

### Transformation 
- expand -t 1(nombre d'espaces) file : convertir les tabulations par des espaces
- unexpand -a file : convertir les espaces en tabulation
- sort -t':' -k 7d -k 3n file (d : dictionnaire, n : numérique, M : ordre chronologique) : trier les lignes d'un fichier texte
- split -l (nombre de lignes) file prefix : découper un fichier (option -C découper en octects -b découper en bits)
- tr M m < file : traduire les caractères sur un fichier 
- sort file | uniq : éliminer les doublons sur un fichier trier 

### Formatage
- fmt -w 100 file : découper en fonction des mots (exemple 100 caractères max par ligne)
- nl -b (a ou t : numéroter toute les lignes ou exclure les lignes vides) -n (ln ou rn ou rz : choisir l'alignement du numérotage ) : numéroter les lignes

### Visualiser un fichier texte
- head -n 10 file : visualiser les premières lignes  
- tail -n 10 file | tail -f file (vérifier les modifications sur un fichier en temps réel) : visualiser les dernières lignes 
- less : visualiser page par page (/chaine : faire une recherche ; ?chaine : faire une recherche inversée  ; q : quitter)

### Résumer
- cut -d':' -f 1 : extraire des colonnes
- wc -l file : compter le nombre de lignes / wc -w file : compter le nombre de mots / wc -c file : la taille du ficher en octect

