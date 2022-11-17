### Kernel ou noyau 
- Séparation entre espace user et espace noyau 
  - Partitionnement virtuel de la RAM
  - Limitation des droits des services et applications 
  - appels système (via IRQ) 
- Noyau monolithique : rassemblement de toutes les fonctionnalités sur un seul logiciel
  - Conception simple 
  - Bonne vitesse d'exécution 
  - Difficulté de maintenance 
- Noyau monolithique modulaire : système de fichiers virtuels
  - Gestion plus simple du hotplug (chargement dynamique) 

#### Gestion des modules du kernel
- commande pour lister les modules : 
```
lsmod
```
- Charger un seul et unique module (pas très partique car ne gère pas les dépendances)
```
insmode <module_path>
```
- Récupérer des infos sur un module donné
```
modinfo
```
- Charger et gérer les dépendances 
```
modprobe <module_name>
```
  - Options : 
  - ```-v``` : verbose 
  - ```-l``` : lister les modules disponibles
  - ```-r``` : décharger un module
  - ```-n``` : test
  - ```--show-depends``` : Afficher les dépendances

- Décharger un module 
```
rmmod <module_name>
```
  - Options : 
  - ```-f``` : forcer le déchargement 
  - ```-w``` : wait (attendre que le module dépendant finisse son travail)
