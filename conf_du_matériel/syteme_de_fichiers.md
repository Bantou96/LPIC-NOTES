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
