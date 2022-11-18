### Créer un faux disque dur
- Créer un fichier rempli de zéro et lui donner une taille de 100MB
```
dd if=/dev/zero of=mon-loop bs=1024 count=102400
```
- Lister les périphériques loop existant
```
losetup -f
```
- Créer le faux disque dur 
```
losetup /dev/loop0 /mon-loop
```
- Lister les disques loop
```
losetup -a
```
