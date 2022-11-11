### RPM
- construire 
- installer
- interroger
- vérifier
- mettre à jour
- désinstaller

### Commandes
- rpm -i -v file.rpm  --> -i (install) | -v (verbose) | -vv (debug) | -h (barre de progression) | --test (n'installe pas)
- rpm -U file.rpm  --> mettre à jour un paquet
- rpm -qi prog_name  --> obtenir des informations sur un paquet déjà installé
- rpm -qpi file.rpm  --> obtenir des informations sur un paquet non installé
- rpm -qf /file_path  --> obtenir des informations sur l'appartenance d'un fichier 
- rpm -e prog-name  --> désinstaller un paquet

### YUM
Gestionnaire de téléchargement et résolution de dépendances
- yum update || yum update yum --> mettre à jour 
- yum check-update  --> vérifier les mises à jour disponibles 
- yum localupdate file.rpm --> mise à jour local
- yum upgrade  --> changer de version 
- yum info prog_name  --> obtenir des informations sur un paquet déjà installé
- yum list prog_name  --> obtenir la version et les mises à jour disponible 
- yum install prog_name  --> installer un paquet 
- yum localinstall file.rpm  --> installation à partir d'un fichier stocké en local 
- yum remove prog_name || yum erase prog_name  --> supprimer un programme 
- yum search keyword  --> recherche d'un paquet
- yum clean [option]  --> libérer de l'espace disque (options : headers, packages, metadata, dbcache, plugins, expire-cache, rpmdb, all)
- yum shell  --> obtenir un shell yum 
