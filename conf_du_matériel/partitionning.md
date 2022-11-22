### les tables de partition
- Table de partition principale (de 1 à 4) dans le MBR
- Table de partition étendue ou logique (à partir de 5) dans le EBR

### Adressage d'un secteur sur un DD
- CHS (Cylinder/Head/Sector) qui se base sur la véritable architecture du disque dur. 
- ECHS qui collabore avec le BIOS
- LBA (Logical Block Adressing) qui lui ne se base pas sur l'architecture du disque dur. 

NB : codes de partition utiles (0x06 FAT ; 0x82 Linux swap)

### Outils de partitionning
- CLI : fdisk/gdisk, GNU parted, cfdisk
- GUI : Gparted, Qtparted, KDE partition manager
