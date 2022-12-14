# Introduction 
### Les distributions Linux
3 grandes familles :
- Debian : Ubuntu, Kali, Debian...
- Redhat : CentOS, Fedora, RHEL...
- Slackware : Suse, OpenSuse...
#### Le Shell
- Interpréteur de commandes interactif et personnalisable
- Deux types (GUI & CLI)
- CLI :  Command Line Interface
  - Bash : Shell de base (le plus répendu et recommandé pour les débutant)
  - C-shell : Shell adapté à la programmation avec le langage C 
  - Z-shell : Shell avec des fonctionnalités avancés comme l'autocomplétion
#### Le prompt
Il fournit les informations sur le système 
- Structure : 
```mame@pc:~$```
  - mame : nom d'utilisateur courant 
  - pc : nom de la machine
  - ~ : Répertoire de travail
  - $ : Caractère de terminaison
- Fichier d'initialisation du shell bash : /etc/profile

# Système de fichiers structurés en arborescence
3 types de fichiers :
- Fichiers ordinaires : mémorisation des données des utilisateurs et du système
- Fichiers répertoires : Contient la liste et la référence des fichiers placés sous son contrôle
- Fichiers spéciaux : désignent les périphériques, les tubes et autres support de communication interprocessus 

### Convention de nommage des fichiers 
- Utiliser le caractère (.) pour les fichiers cachés
- Privilégier les miniscules pour le nommage
- Eviter les caractères spéciaux et les blancs (par exemple créer un fichier ```my_file``` plutôt que ```my file```)

### Types de fichiers
- Fichier de type standard : (-)
- Fichier de type répertoire : (d)
- Fichier de périphérique bloc : (b)
- Fichier de périphérique caractère : (c)
- Fichier socket : (s)
- Lien symbolique sur un fichier : (l)  

### Arborescence
- /     --> Racine du système 
- /bin  --> Commande binaires utilisateurs essentielles 
- /boot --> fichiers statiques du démarrage
- /dev  --> fichiers de périphériques
- /etc  --> fichiers de configuration d'un sytème spécifique
- /lib  --> fichiers des bibliothèques partagés et des modules du noyau
- /home --> répertoires personnels des utilisateurs 
- /root --> répertoire personnel de l'admin 
- /mnt  --> point de montage pour les systèmes de fichiers 
- /proc --> système de fichiers virtuel d'informations du noyau et des processus 
- /sbin --> répertoire contenant les exécutables
- /sys  --> fichiers d'état des périphériques 
- /tmp  --> fichiers temporaires

### Répertoires spéciaux
- Répertoire courant noté .
- Répertoire parent noté ..
- Répertoire utilisateur noté ~
- Répertoire précédent noté -
- Chemin : 
  - Absolu : chemin complet à partir de la racine et commençant toujours par "/"
  - Relatif : chemin partiel d'un répertoire par rapport à l'endroit où l'on se trouve. 

### Les types de commandes 
- Commandes internes au shell 
- Commandes externes (programmes binaires)
- Les alias (raccourcis de commandes)
- Syntaxe d'une commande : 
  - commande -options arg1 arg2

Exemple
``` 
wc -l /etc/passwd
```
