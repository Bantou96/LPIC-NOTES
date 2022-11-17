### Sysfs
- Système de fichier vituel permettant de récolter des infos essentiellement sur le matériel. 
- Plus simple que procfs et hiérarchisé
- Fichiers ```/sys/devices``` , ```/sys/bus``` , ```/sys/class``` (très pratique pour la partie admin)


NB : Commande pour se déplacer d'un lien symbolique vers le vrai chemin. 

```
cd `realpath $PWD`
```
