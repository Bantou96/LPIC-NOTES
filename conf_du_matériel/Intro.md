### BIOS (firmware)
BIOS (Basic Input Ouput System) est intégré dans la ROM de la carte mère
- Permet le démarrage du système 
- Offre des informations au kernel sur le matériel 

### IRQ
Interruptions matérielles déclenchées par les périphériques afin de prendre la main sur le processeur.
- Mécanisme d'interruption permettant de suspendre le travail en cours
- Architectures x86
- Fichier : ```/proc/interrupts```

### Ports E/S
Espace mémoire fixe et unique allouée à un périphérique afin de permettre la communication avec le CPU
- Fichier : ```/proc/ioports```

### Adresses DMA (Direct Memory Access)
Evite le calcul du processeur pour l'allocation mémoire qui prend du temps. 
- Fichier : ```/proc/dma```
