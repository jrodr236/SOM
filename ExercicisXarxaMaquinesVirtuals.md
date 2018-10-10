Configuració de la xarxa a les màquines virtuals - Exercicis pràctics
======================================================

> Aquestes primeres pràctiques es corregiran a classe. Cada pràctica l'explicarà un/a alumne/a escollit aleatòriament.

1. Quina és l'adreça de xarxa IP de la màquina real?

   > Per conèixer la IP d'una màquina amb linux, cal obrir el *Terminal* i utilitzar la comanda
   ```console
   ip a
   ```
   > Les IPs estan darrera la paraula `inet`, i son del tipus `192.168.X.X`, `172.X.X.X`, etc... Ignorar la IP de loopback (`127.X.X.X`).

4. Prova la connexió a Internet a la màquina real. Si no funciona, comenta-li al professor.

   > Per fer una prova senzilla, pots fer un *test* de connexió a un servidor d'Internet amb la següent comanda:
   ```console
   ping 8.8.8.8
   ```

4. Apunta el mode en el que està configurada la xarxa de la màquina virtual Ubuntu. Canvia el mode de xarxa de la màquina virtual Ubuntu a *NAT* (si escau). Quina és la seva IP? Prova la connexió a Internet. Explica perquè has obtingut aquests resultats.

5. Canvia el mode de xarxa de la màquina virtual Ubuntu a *Pont (Bridged)*. Quina és la seva IP? Prova la connexió a Internet. Explica perquè has obtingut aquests resultats.

5. Canvia el mode de xarxa de la màquina virtual Ubuntu a *Host-only*. Quina és la seva IP? Prova la connexió a Internet. Explica perquè has obtingut aquests resultats.

* Torna a deixar el mode de xarxa com estava abans de fer els canvis.

Grimpades
----------
>Les següents pràctiques son especialment difícils. La correcció a classe serà voluntària, però seran avaluades quan es lliurin al moodle.

Recorda que el _Firewall_ integrat dels sistemes Windows estan configurats per no respondre els _pings_. Per les següents pràctiques, es recomana deshabilitar el _Firewall_ de Windows.

1. Verifica si dues màquines virtuals configurades amb *NAT* tenen visibilitat de xarxa entre elles.

1. Verifica si dues màquines virtuals, que s'estiguin executant en dos ordinadors diferents, configurades amb *Bridged* tenen visibilitat de xarxa entre elles.

1. Verifica si dues màquines virtuals, que s'estiguin executant en dos ordinadors diferents, configurades amb *Host-only* tenen visibilitat de xarxa entre elles.
