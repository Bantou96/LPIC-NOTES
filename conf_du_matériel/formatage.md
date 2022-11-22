### Définition 
- Formatage bas niveau : rendre la structure du disque conforme
- Formatage haut niveau : création d'un système de fichier 

### Créer un système de fichier 
Syntaxe : mkfs.<fstype> <partition> ou mkfs -t <fstype> <partition>
  
Exemple :
```
mkfs.ext4 /dev/sda
```
Options : 
  - ``` -c ``` : recherche de secteurs défectueux
  - ``` -m ``` : pourcentage d'espace reservé (5 par défaut). Utilisé par root pour les tâches d'administration

- Formatage pour FAT
```
mkfs.msdos /dev/sda
```
ou
```
mkfs.vfat /dev/sda
```
- Formatage pour swap (extention de la mémoire)
  - formatage
  ```
  mkswap /dev/sda
  ```
  - Utilisation
  ```
  swapon /dev/sda
  ```
  
