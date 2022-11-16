## Commande dpkg
#### installation
```
dpkg -i file.deb
```
- Options : 
  -  ```-i``` : install  
  -  ```-R``` : mode récursif   
  -  ```--no-act``` : permet juste d'effectuer un test mais n'installe pas
#### Désinstallation
```
dpkg -r paquet
```
- Options : 
  -  ```-r``` : désinstaller 
  -  ```-P``` : supprimer les fichiers de configuration  
#### Obtenir des informations sur un paquet déjà installé
```
dpkg -p paquet
```
#### Obtenir des informations sur un paquet non installé
```
dpkg -I file.deb
```
#### Obtenir des informations sur l'appartenance d'un fichier
```
dpkg -S pattern  
```
#### Relancer le script post-installation 
```
dpkg-reconfigure paquet  
```
ou 
```
dpkg --configure paquet  
```
#### Rechercher les paquets partiellements installés 
```
dpkg -C  
```
## APT-CACHE (Advanced Packaging Tool)
### Manipulation du cache des paquets avec la commande : ```apt-cache``` 
#### Informations sur un paquet
```
apt-cache showpkg package_name 
```
#### Afficher les statistiques 
```
apt-cache stats
```
#### Afficher les dépendances insatisfaites
```
apt-cache unmet 
```
#### Afficher les dépendances d'un paquet
```
apt-cache depends paquet
```
#### Recherche de paquets 
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
