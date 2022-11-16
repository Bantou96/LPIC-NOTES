### Commande dpkg
- installer un paquet : dpkg -i file.deb (-R --> mode récursif ; --no-act --> simple test)
- obtenir des informations : dpkg -p paquet  || dpkg -I file.deb  || dpkg -S pattern  || dpkg -L file
- Désinstaller un paquet : dpkg -r paquet || dpkg -P (supprimer les fichiers de configuration)
- relancer le script post-installation : dpkg-reconfigure paquet  || dpkg --configure paquet
- paquets partiellements installés : dpkg -C

### APT-CACHE (Advanced Packaging Tool)
- Manipulation du cache des paquets : apt-cache 
- apt-cache showpkg package_name : informations sur un paquet
- apt-cache stats : afficher statistiques
- apt-cache unmet : afficher les dépendances insatisfaites
- apt-cache depends paquet : afficher les dépendances d'un paquet
- recherche de paquets : apt-cache pkgnames (paquets installés) || apt-cache search expression (recherche dans les dépôts)

### APT-GET
- mettre à jour les informations sur les dépôts : apt-get update
- recherhe des dépendances défectueuses : apt-get check 
- nétoyer le référentiel local des paquets récupérés : apt-get clean
- installer : apt-get install paquet (options -f répare les dépendances insatisfaites)
- désinstaller : apt-get remove paquet  || apt-get autoremove (supprimer les paquets orphelins ne répondant à aucune dépendances)
- récuperer un paquet source : apt-get source package (options -b compile après récupération du fichier source)
- apt-get upgrade || apt-get dist-upgrade (système intelligent de résolution de conflit)

### Configuration de APT
- fichier /etc/apt/sources.list  --> deb link (distribution_code_name || catégories_version) section 
