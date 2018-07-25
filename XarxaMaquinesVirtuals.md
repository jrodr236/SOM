# Configuració de la xarxa a les màquines virtuals

[//]: https://www.virtualbox.org/manual/ch06.html

* [Resum](https://gitpitch.com/jrodr236/som/master?p=XarxesMaquinesVirtuals)
* Exercicis teòrics: *No n'hi ha*
* [Exercicis pràctics](ExercicisXarxesMaquinesVirtuals.md)

## Hardware virtual
VirtualBox té els següents tipus de targetes de xarxa virtual:

* AMD PCNet PCI II (Am79C970A);
* AMD PCNet FAST III (Am79C973, the default);
* Intel PRO/1000 MT Desktop (82540EM);
* Intel PRO/1000 T Server (82543GC);
* Intel PRO/1000 MT Server (82545EM);
* Paravirtualized network adapter (virtio-net).

Cada targeta indica quin hardware serà presentat a la màquina virtual.

Es recomana escollir correctament el tipus de sistema operatiu en la creació de la màquina virtual. Això farà que s'esculli la millor targeta pel sistema a instal·lar.

## Modes de Xarxa

### No connectat
En aquest mode, VirtualBox informa al convidat que hi ha una targeta de xarxa, però que no hi ha cap connexió, com si el cable cable Ethernet no estigués connectat a la targeta. D'aquesta manera, es pot "desendollar" el cable Ethernet virtual i interrompre la connexió. Això pot ser útil per informar un sistema operatiu convidat que no hi ha cap connexió de xarxa disponible i fer una reconfiguració.

### NAT

![](https://cdn.app.compendium.com/uploads/user/e7c690e8-6ff9-102a-ac6d-e4aebca50425/f2e3e7b6-c53b-4457-85e9-49625315791a/Image/90093dc07a2e9cb7d93bf7a3fa8f8c19/nat.png)
*Les VM estan desconnectades entre si*

Si tot el que voleu és navegar per la Web, baixar fitxers i visualitzar correus electrònics a l'interior del client, aquest mode predeterminat hauria de ser suficient.

### Xarxa NAT

![](https://cdn.app.compendium.com/uploads/user/e7c690e8-6ff9-102a-ac6d-e4aebca50425/f2e3e7b6-c53b-4457-85e9-49625315791a/Image/04856a6937656d8c2a2e0dd30855f3ba/nat_port_forward.png)
*Les VM estan connectades entre si*

Aquest mode funciona de manera similar a un *router* domèstic, agrupant els sistemes que l'utilitzen en una xarxa i evitant que els sistemes fora d'aquesta xarxa accedeixin directament als sistemes dins d'ell, però deixant que els sistemes interconnectin entre si.

*No confondre amb NAT*

### Adaptador pont

![](https://cdn.app.compendium.com/uploads/user/e7c690e8-6ff9-102a-ac6d-e4aebca50425/f2e3e7b6-c53b-4457-85e9-49625315791a/Image/5e1da37f793c380abd4375ff64b21c70/bridged.png)

Això és per a necessitats de xarxes més avançades, com ara simulacions de xarxa i servidors en funcionament en un hoste. Quan està habilitat, VirtualBox es connecta a una de les seves targetes de xarxa instal·lades i intercanvia paquets de xarxa directament, evitant la pila de xarxa del sistema operatiu principal.

### Xarxa interna

![](https://cdn.app.compendium.com/uploads/user/e7c690e8-6ff9-102a-ac6d-e4aebca50425/f2e3e7b6-c53b-4457-85e9-49625315791a/Image/d16091a2abef68694625196dd18f588a/internal.png)

Això es pot utilitzar per crear un tipus diferent de xarxa basada en programari que sigui visible per a màquines virtuals seleccionades, però no per a aplicacions que s'executin a l'amfitrió o al món exterior.

### Adaptador de només amfitrió

![](https://cdn.app.compendium.com/uploads/user/e7c690e8-6ff9-102a-ac6d-e4aebca50425/f2e3e7b6-c53b-4457-85e9-49625315791a/Image/1ae51906a03cffa842010fd6d6937c61/host_only.png)

Això es pot utilitzar per crear una xarxa que contingui l'amfitrió i un conjunt de màquines virtuals, sense necessitat de la interfície de xarxa física de l'amfitrió. Al contrari, es crea una interfície de xarxa virtual (similar a una interfície *loopback*) al host, proporcionant connectivitat entre les màquines virtuals i el host.

### Mòdul genèric

Es tracta d'uns modes poc utilitzat, que comparteixen la mateixa interfície de xarxa genèrica, permetent a l'usuari seleccionar un controlador que es pugui incloure amb VirtualBox o que es distribueixi en un paquet d'extensió.

### Resum

|VM ↔ Host|VM1 ↔ VM2|VM → Internet|VM ← Internet
---------|---------|-------------|-------------
Host-only|+|+|–|–
Internal|–|+|–|–
Bridged|+|	+|	+|	+
NAT|	–|	–|	+|	Port forwarding
NAT Network|	–|	+|	+|	Port forwarding
