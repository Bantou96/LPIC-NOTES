## RPM
- construire 
- installer
- interroger
- vérifier
- mettre à jour
- désinstaller

### Commandes
#### installation
```
rpm -i -v file.rpm
```
- Options : 
  -  ```-i``` : install  
  -  ```-v``` : verbose  
  -  ```-vv``` : mode debug  
  -  ```-h``` : affiche la barre de progression 
  -  ```--test``` : permet juste d'effectuer un test mais n'installe pas
#### Mettre à jour un paquet
```
rpm -U file.rpm
```
#### Obtenir des informations sur un paquet déjà installé
```
rpm -qi prog_name 
```
#### Obtenir des informations sur un paquet non installé
```
rpm -qpi file.rpm
```
#### Obtenir des informations sur l'appartenance d'un fichier
```
rpm -qf /file_path 
```
#### Désinstaller un paquet
```
rpm -e prog-name 
```
## YUM
Gestionnaire de téléchargement et résolution de dépendances
#### Mettre à jour
```
yum update 
```
Pour une première installation faire :
```
yum update yum 
```
#### Vérifier les mises à jour disponibles
```
yum check-update
```
#### Mise à jour à partir des dépôts stockés en local
```
yum localupdate file.rpm 
```
#### Changer de version
```
yum upgrade
```
#### Obtenir des informations sur un paquet déjà installé
```
yum info prog_name
```
#### Obtenir la version et les mises à jour disponible 
```
yum list prog_name
```
#### Installer un paquet
```
yum install prog_name
```
#### Installation à partir d'un fichier stocké en local 
```
yum localinstall file.rpm
```
#### Supprimer un programme 
```
yum remove prog_name
```
ou 
```
yum erase prog_name
```
#### Rechercher un paquet 
```
yum search keyword
```
#### Libérer de l'espace disque
 ```
 yum clean [option] 
```
- Options : headers, packages, metadata, dbcache, plugins, expire-cache, rpmdb, all
#### Obtenir un shell yum 
```
yum shell  
```
### Configuration de Yum
- fichier de configuration : /etc/yum.conf
- fichier permettant de faire la modification des dépôts : /etc/yum.repos.d

### Options de base dans /etc/yum.conf
- verbosité : ```debuglevel = value```
- exclusion de paquets : ```exclude = package_name ```
- activer / désactiver la vérification des signatures : ```gpgcheck = bool_value```
- nombre d'essais avant de retourner une erreur : ```retries = value```
- prendre en compte le type d'architecture lors de MAJ : ```exactarch = bool_value```

### Gestion des priorités
```
yum install yum-priorities
```
- fichier : etc/yum/pluginconf.d/priorities. conf

### Ajout de dépôts via rpm 
#### Téléchargement du paquet
```
wget https://link
```
#### Importation de la clé GPG
```
rpm --import gpg_link 
```
#### Vérification du checksum
```
rpm -K file.rpm
```
#### Vérification des mises à jour
```
yum check-update
```
