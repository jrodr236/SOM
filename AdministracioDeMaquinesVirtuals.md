Administració de màquines virtuals
==================================

* [Resum](https://gitpitch.com/jrodr236/som/master?p=AdministracioDeMaquinesVirtuals)
* Exercicis teòrics: *No n'hi ha*
* [Exercicis pràctics](ExercicisAdministracioDeMaquinesVirtuals.md)

Easy Install
------------
_VMWare Workstation_ permet automatitzar la instal·lació de determinats sistemes operatiu amb la opció _Easy Install_. Amb aquesta opció, només se'ns demana les dades més bàsiques (clau de llicència, contrasenya, etc...).

![Easy Install](https://geek-university.com/wp-content/images/vmware-player/vmware_player_easy_install.jpg?x13092)

> Per tal de practicar les instal·lacions reals, en aquesta matèria, **NO** utilitzarem aquesta opció. Ara, però, farem una excepció: comença a fer l'exercici pràctic 1.


Disc en un o en múltiples fitxers
---------------------------

En el moment de fer la instal·lació, VMWare ens demana si volem que el fitxer del disc virtual estigui en un sol fitxer o _"trosejat"_ en múltiples fitxers.

![Split disk](https://i.stack.imgur.com/76ObU.png)

> En aquesta matèria, per simplificar el moviment de màquines virtuals, escollirem **SEMPRE** un sol fitxer.


Modificar la imatge ISO de la unitat de CD/DVD
------------------------------------------------
Per a fer una instal·lació a partir d'un CD/DVD, cal indicar a la màquina virtual a on es troba la imatge ISO. Per fer-ho cal:
1. Obrir el menú `VM > Settings`.
2. Escollir la opció `CD/DVD`.
3. Assegurar-nos que la opció `Connected` està seleccionada.
4. Seleccionar `Use ISO image file`, i clicar el botó `Browse...` per indicar la ruta del fitxer ISO.

![CD/DVD settings](http://www.techulator.com/attachments/Resources/5081-14750-VMWare-Workstation-options.png)




Instal·lar les _VMWare Tools_
------------------------------

Les _VMWare Tools_ s'han d'instal·lar dins la màquina virtual després d'instal·lar el sistema operatiu. Consisteixen en els controladors dels dispositius i aplicacions del sistema que optimitzen el sistema operatiu convidat per millorar el rendiment i la usabilitat.

Procediment per instal·lar les _VMWare Tools_:
1. Iniciar la màquina virtual.
2. Clicar a `VM > Install VMWare Tools`.
3. Si no s'ha iniciat automàticament, anar al CD i executar el programa `setup.exe` que hi ha dins la carpeta `setup`.
4. Fer servir l'assistent per instal·lar les *VMWare Tools*.

Les *Guest Additions* ofereixen les següents funcionalitats:
* Rendiment de gràfics considerablement més ràpid i _Windows Aero_ en els sistemes operatius compatibles amb _Aero_.
* La funció _Unity_, que permet que una aplicació de màquina virtual aparegui en l'escriptori del host, com qualsevol altra finestra d'aplicació.
* Carpetes compartides entre els sistemes d'arxius del _host_ i el _guest_.
* Funció de copiar i enganxar text, gràfics i arxius entre la màquina virtual i l'escriptori del host o del client.
* Millora del rendiment del ratolí.
* Sincronització del rellotge de la màquina virtual amb el rellotge de l'escriptori del host o del client.
* Ús de _scripts_ que ajuden a automatitzar les operations del sistema operatiu _guest_.



Augmentar mida de la memòria principal (RAM)
---------------------------

> La **memòria principal** és a on s'emmagatzemen temporalment les dades i les programes que la CPU està processant o ha de processar en un moment determinat.

Cal fer-ho quan el rendiment de la màquina virtual es redueix per manca de memòria.

**Important!** La RAM assignada a la màquina virtual es reduirà de la màquina real.

Procediment:
1. Parar la màquina virtual.
2. Obrir el menú `VM > Settings`.
3. Escollir la pestanya `Memory`.
4. Modificar la `Memory for this virtual machine`.


Augmentar la mida de la memòria secundària (disc dur)
---------------------------

> La **memòria secundària** és un tipus d'emmagatzemament permanent (no volàtil), amb més capacitat que la memòria primària però més lenta.

>El tipus principal és el disc dur, però n'hi ha molts més: DVD, pendrive, SSD, etc...


Un cop augmentem l'espai del disc dur podem:
* Augmentar la mida del volum/partició
* Crear un nou volum/partició

Procediment:
1. Para la màquina virtual.
2. Entra al menú `VM > Settings`.
3. Escollir la pestanya `Hard Disk`.
3. Selecciona el disc que vols augmentar.
4. Selecciona el botó `Expand`.
5. Modifica la mida del disc.
6. Obrir la màquina virtual i crear/modificar la mida del volum.
  * Windows: eina *Disk Management*.
  * Linux: eina *GParted*.


Crear snapshots i realitzar rollbacks
---------------------------
Els *snapshots* (instantànies) permeten desar desar un estat particular d'una màquina virtual. És especialment útil per fer proves:
1. Creen una instantània.
2. Fem la prova.
3. Si la prova ha sortit malament, restaurem la instantània per tornar a l'estat anterior.

És recomanable fer instantànies després d'instal·lar el sistema operatiu, i abans d'iniciar qualsevol procediment delicat.

Per crear un nou _snapshot_, seleccionar `VM > Snapshots > Take Snapshot...`.

La gestió de *snapshots* es fa des de `VM > Snapshots > Snapshot Manager`.

Localització de les màquines virtuals
--------------------------
Les màquines virtuals creades es poden trobar a:
- Sistemes Windows: `C:\Users\nom_usuari\Documents\Virtual Machines`
- Sistemes GNU/Linux: `/home/nom_usuari/vmware`

Exportar i importar VMs en el format OVF
---------------------------
[OVF](https://en.wikipedia.org/wiki/Open_Virtualization_Format) (Open Virtualization Format) és un format estàndard per l'intercanvi de màquines virtuals, que és compatible amb els principals gestors de màquines virtuals: VirtualBox, VMWare, etc...

La importació es fa obrint el fitxer (`File > Open`), i la exportació a `File > Export to OVF...`.


Clonar màquines virtuals
---------------------------
Clonar màquines virtuals ens permet fer còpies exactes d'una màquina virtual.

Per a fer les clonacions, seleccionar `VM > Manage > Clone...`. Cal fer-ho amb la màquina virtual aturada.

Cal fixar-se en la diferència entre:
- crear una clonació _linkada_ a la màquina original, o 
- una clonació completa, independent de la màquina original.


Trobar màquines virtuals ja preparades
---------------------------
A Internet podem trobar màquines virtuals de tota mena ja preparades, per exemple a https://www.osboxes.org/ o a https://bitnami.com/.

Copiar fitxers des de la màquina real a la màquina virtual
---------------------------
Per intercanviar fitxers entre la màquina real i la virtual cal fer servir Carpetes compartides. Les *VMWare Tools* han d'estar instal·lades.

Procediment:
1. Obrir el menú `VM > Settings` de la màquina virtual.
2. Seleccionar la pestanya `Options`.
3. Escollir la opció `Shared Folders`.
4. Escollir `Always enabled` o `Enabled until next power off or suspend`, segons convingui.
5. Clicar el botó `Add` i afegir la carpeta compartida, escollint les opcions addients.
4. Accedir al *servidor d'arxius virtual* `\\.host\Shared Folders\`.


Configuració de la xarxa
---------------------------

Es tractarà al proper tema.
