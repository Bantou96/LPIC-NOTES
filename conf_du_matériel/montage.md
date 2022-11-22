### La commande mount
Associer un système de fichier à un répertoire existant. 

#### Monter 
```
mount <partition> /mnt/point_montage
```
Options : 
  - ``` -a ``` : (all) monter toutes les partitions
  - ``` -w ``` : (write) enregister
  - ``` -r ``` : (read-only) accéder en lecture seule
  - ``` -v ``` : mode verbose
  - ``` -L ``` : modifier le label
  - ``` -U ``` : modifier l'UID
  - ``` -l ``` : lister les partitions montées
  - ``` -o ``` : spécifier les options fstab (default, loop, auto & noauto, user & nouser, users, ro , rw)

#### Démonter 
```
umount <partition> 
```
Options : 
  - ``` -a ``` : (all) démonter toutes les partitions
  - ``` -f ``` : forcer l'opération 
  - ``` -r ``` : remonter en ro (si échec)

Fichier de montage automatique ``` /etc/fstab ```
