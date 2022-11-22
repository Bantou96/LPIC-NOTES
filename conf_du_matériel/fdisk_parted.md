### fsdisk (fixed disk)
Outil de partitionnement en mode texte et interactif

### Commandes
Syntaxe : fdisk <option> <périphérique>
- Affichage des partitions
```
fdisk -l 
```
- Partitionnement
  ```
  fdisk /dev/sda
  ```
  - n : créer une partition
  - p : afficher les partitions
  - d : supprimer une partition
  - t : modifier le type de partition 
  - v : vérification de la table de partition
  - q : quitter sans sauvegarder
  - w : quitter et enregistrer
  - l : lister les codes de partition
  
### GNU Parted
Outil plus complet que fdisk 
- Affichage des partitions
```
parted -l 
```
- Partitionnement
  ```
  parted /dev/sda
  ```
  - mkpart : créer une partition
  - rm : supprimer une partition
  - resize : redimensionner une partition
  - move : déplacer une partition
  - print : afficher la table de partition
  
