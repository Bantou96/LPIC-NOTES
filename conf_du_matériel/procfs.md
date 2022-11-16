### Procfs 
Système de fichier virtuel destiné à la gestion des processus.
#### Objectifs : récupérer des informations sur
- les processus
- le matériel 

#### Alimentation 
- Alimentation générale : ```/proc/acpi```
- Alimentation du processeur : ```/proc/acpi/processor```
- Alimentation zones thermiques : ```/proc/acpi/thermal_zone```

### BUS
- Fichiers correspondant à chaque périphérique USB : ```/proc/bus/usb``` 
- liste des périphériques PCI : ```/proc/acpi/pci``` (difficile à lire) 
  - utiliser la commande pour avoir un listing complet : 
    ```
    lspci -vb
    ``` 
### Processeur
Informations sur les différents processeurs : ```/proc/cpuinfo```

### Mémoire
- Alias vers les informations sur la mémoire vive : ```/proc/kcore```
- Informations sur l'état courant de la mémoire : ```/proc/meminfo```
- Résumer par disque l'utilisation de la SWAP
  ```
  swapon -s 
  ```
- Afficher la quantité totale de mémoire et swap (libre et utilisée)
  ```
  free
  ```
### Kernel
- Paramètres du kernel au lancement : ```/proc/sys```
- Liste des modules chargés en mémoire 
  ```
  lsmod
  ```
- Informations sur l'activité du kernel
  ```
  dmesg
  ```
- Informations sur la version : ```/proc/version``` et ```/proc/sys/kernel/version```
  ```
  uname -a
  ```
- Temps d'utilisation du système : ```/proc/loadavg``` (difficile à lire ). Utiliser la commande suivante :
  ```
  uptime
  ```
