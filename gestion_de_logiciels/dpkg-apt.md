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
#### Recherche de paquets déjà installés
```
apt-cache pkgnames
```
#### Recherche de paquets dans les dépôts
```
apt-cache search <expression>
```


## APT-GET
#### Mettre à jour
```
apt-get update 
``` 
#### Recherhe des dépendances défectueuses
```
apt-get check 
``` 
#### Nettoyer le référentiel local des paquets récupérés
```
apt-get clean 
``` 
#### Installer
```
apt-get install paquet 
``` 
- Options ```-f``` : permet de réparer les dépendances insatisfaites
#### Désinstaller
```
apt-get remove paquet
```
#### Supprimer les paquets orphelins ne répondant à aucune dépendances
```
apt-get autoremove 
```
#### Récuperer un paquet source  
```
apt-get source package
```
- Option ```-b``` : permet de compiler après récupération du fichier source
#### upgrade
```
apt-get upgrade
```
On peut aussi utiliser le système intelligent de résolution de conflit
```
apt-get dist-upgrade
```
### Configuration de APT
#### fichier /etc/apt/sources.list  
deb link (distribution_code_name || catégories_version) section 
