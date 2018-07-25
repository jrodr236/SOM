Administració de màquines virtuals
==================================

[//]: https://www.udemy.com/oracle-virtualbox-administration-for-absolute-beginners/

* [Resum](https://gitpitch.com/jrodr236/som/master?p=AdministracioDeMaquinesVirtuals)
* Exercicis teòrics: *No n'hi ha*
* [Exercicis pràctics](ExercicisAdministracioDeMaquinesVirtuals.md)

Instal·lar les guest additions
------------------------------

Les *Guest Additions* s'han d'instal·lar dins la màquina virtual després d'instal·lar el sistema operatiu. Consisteixen en els controladors dels dispositius i aplicacions del sistema que optimitzen el sistema operatiu convidat per millorar el rendiment i la usabilitat.

Procediment per instal·lar les *Guest Additions*:
1. Iniciar la màquina virtual.
2. Clicar a `Dispositius > Insereix la imatge de CD de les Guest Additions`.
3. Si no s'ha iniciat automàticament, anar al CD i executar el programa `VBoxWindowsAdditions.exe`.
4. Fer servir l'assistent per instal·lar les *Guest Additions*.

Les *Guest Additions* ofereixen les següents funcionalitats:
* Integració del punter del ratolí
* Carpetes compartides
* Millor suport de vídeo
* *Seamless windows*
* Canal de comunicació genèric entre el *host* i el *guest*
* Sincronització del rellotge
* Portapapers compartit
* Inici de sessió automatitzat (passant les credencials)


Augmentar mida de la RAM
---------------------------

Cal fer-ho quan el rendiment de la màquina virtual es redueix per manca de memòria.

**Important!** La RAM assignada a la màquina virtual es reduirà de la màquina real.

Procediment:
1. Parar la màquina virtual.
2. Obrir el menú `Paràmetres`.
3. Escollir la pestanya `Sistema`.
4. Modificar la `Memòria base`.


Augmentar la mida del disc dur
---------------------------

Amb l'espai sobrant del disc dur creat, podem:
* Augmentar la mida del volum
* Crear un nou volum

Procediment:
1. Para la màquina virtual.
2. Entra al menú `Fitxers > Gestor de suports virtuals`.
3. Selecciona el disc que vols augmentar.
4. Selecciona el botó `Propierties`.
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

La gestió de *snapshots* es fa des de la pestanya `Machine Tools > Captures`.

Exportar i importar VMs en el format OVF
---------------------------
[OVF](https://en.wikipedia.org/wiki/Open_Virtualization_Format) (Open Virtualization Format) és un format estàndard per l'intercanvi de màquines virtuals, que és compatible amb els principals gestors de màquines virtuals: VirtualBox, VMWare, etc...

La gestió d'importacions i exportacions es fa des del menú `Fitxers > Importa una aplicació virtual / Exporta una aplicació virtual`

Clonar màquines virtuals
---------------------------
Clonar màquines virtuals ens permet fer còpies exactes d'una màquina virtual.

Per a fer les clonacions, seleccionar `Màquina > Clona`. Es recomana fer amb la màquina virtual aturada.

Seleccionar *Reinicialitza l'adreça MAC de totes les targetes de xarxa* en cas que necessitem tenir la màquina original i la clonació engegades alhora, per evitar problemes amb la xarxa.


Trobar màquines virtuals ja preparades
---------------------------
A Internet podem trobar màquines virtuals de tota mena ja preparades, per exemple a https://www.osboxes.org/ o a https://bitnami.com/.

Copiar fitxers des de la màquina real a la màquina virtual
---------------------------
Per intercanviar fitxers entre la màquina real i la virtual cal fer servir Carpetes compartides. Les *Guest Additions* han d'estar instal·lades.

Procediment:
1. Obrir el menú `Paràmetres` de la màquina virtual.
2. Seleccionar la pestanya `Carpetes compartides`.
3. Afegir la nova carpeta, escollint les opcions addients.
4. Accedir al *servidor d'arxius virtual* `\\VBOXSVR`.


Configuració de la xarxa
---------------------------

Es tractarà al proper tema.
