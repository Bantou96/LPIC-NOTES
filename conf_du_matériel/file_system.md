### FHS (File system Hierarchy Standard)
Le but principal est d'apporter plus de simplicité et de cohérence dans l'organisation des fichiers
- Les apports du FHS
  - partageabilité (shareable, unshareable)
  - Static ou variable (modificabilité)

- Exemples
  - Programmes : ```/bin``` , ```/sbin``` , ```/lib``` 
  - Système : ```/boot``` , ```/etc```
  - Données utilisateurs : ```/home``` , ```/root```
  - Données variables : ```/var``` , ```/tmp```
  - Montage : ```/mnt``` , ```/media```
  - FS virtuels : ```/dev``` , ```/proc```  

### Système de fichiers 
Structure de données de bas niveau qui permet au système de lire et modifier sa structure afin d'accèder et de stocker des fichiers via un chemin. 
- Journalisation : concept de traçage des opérations d'écriture en cours
- fragmentation : écriture dans plusieurs endroits de l'espace disque 

### Les types 
- EXT 
  - ext2 : pas de journalisation
  - ext3 : Compatible avec ext2
  - ext4 : Ajoute un espace réservé en fin de fichiers (gestion de disque de grande capacité)
- JFS (Journaling FS) : Rapide, stable et faible utilisation du processeur (meilleur option pour les bases de données)
- XFS (Extended FS) : Très haute performance particulièrement sur les E/S (big data et fibre optique)
- FAT (File Allocation Table)
- NTFS (New Technology FS) : Windows
- HFS (Hierarchical FS) : mac-os 

### Informations sur les FS
3 outils pour gérer les systèmes de fichiers
- dumpe2fs : recupérer les infos
- tune2fs : modifier certains paramètres
- debugfs

#### Récupérer les informations générales
- EXT (l'option -h permet de récuperer des informations sur le super bloc qui sont plus faciles à lire)
```
dumpe2fs -h /dev/sda
```
- XFS 
```
xfs_info /dev/sda
```
Pour exporter les données (format binaire)
```
xfs_metadump /dev/sda export_file
```

#### Ajuster les paramètres d'un FS
Il ne faut jamais apporter des modifications sur un système de fichier déjà monté.
- EXT
```
tune2fs <options> <partition> 
```
Options : 
  - ``` -c ``` : modifier le nombre de montage avant vérification
  - ``` -C ``` : modifier le compteur de montage
  - ``` -i ``` : modifier la valeur du "check-interval" (day/week/month). Exemple : ```tune2fs -i 6w /dev/loop0 ```
  - ``` -j ``` : ajouter une fonctionnalité de journalisation
  - ``` -m ``` : modifier le pourcentage d'espace reservé
  - ``` -r ``` : spécifier le nombre de blocs réservé

- XFS
```
xfs_admin <options> <partition> 
```
Options : 
  - ``` -j ``` : activer la journalisation
  - ``` -L ``` : modifier le label (nom de la partition)
  - ``` -U <uid> ``` ou ``` -U generate ``` : modifier l'uid ou le générer de façon automatique
  - ``` -u ``` : Vérifier l'UID
  - ``` -l ``` : vérifier le nom de la partition

