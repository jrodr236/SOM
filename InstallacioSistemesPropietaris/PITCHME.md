Instal·lació de sistemes operatius propietaris
======================================================

[Veure Teoria](https://jrodr236.github.io/SOM/InstallacioSistemesPropietaris.html)

---

Requisits tècnics del sistema operatiu que s’ha d’instal·lar
------------------------------------------------------------

Son els serveis ha de tenir el sistema informàtic.

<img src="https://images.techhive.com/images/article/2016/08/omg-laptop-computer-crash-wtf-100678098-primary.idge.jpg" height="200">

---

Selecció del sistema operatiu que s’ha d’instal·lar
---------------------------------------------------

Per cada sistema operatiu, es verifica si podria complir els requeriments tècnics.

<img src="https://cdn-images-1.medium.com/max/800/1*ahUuu9SZXa_vbz7Hvl7A1g.jpeg" height="200">

---

Mètodes d’instal·lació i de planificació dels paràmetres bàsics d’un disc dur
-----------------------------------------------------------------------------

+++

### Partició d’un disc dur

* Divisió d'un disc dur.
* Cada partició és una unitat d'emmagatzematge independent.

<img src="https://assets.pcmag.com/media/images/317282-how-to-partition-a-hard-drive.jpg" height="300">

+++

* MBR (Antic, per defecte a màquines virtuals)
  * 4 particions primàries màxim
  * Les primàries poden ser esteses, que tenen lògiques a dins (tantes com necessitis)

+++

<img src="https://2.bp.blogspot.com/-DG6Yu--1O2g/VngL8QBFWII/AAAAAAAAAGw/AqAsecfPza8/s1600/2.png">

+++

* GPT (Actual): sense aquestes limitacions

+++

<img src="https://1.bp.blogspot.com/-lj3hQNq4mNE/VngMLBhnk-I/AAAAAAAAAG4/9VnkYjmq16E/s1600/3.png">

+++

### Sistema de fitxers d’un sistema operatiu Windows

És una estructura que permet desar informació a una partició.

NTFS: sistema per defecte a Windows.

+++

<img src="https://www.muycomputer.com/wp-content/uploads/2015/12/%C2%BFEn-qu%C3%A9-contextos-hay-que-usar-FAT32-NTFS-y-exFAT.jpg">

+++

### Formatació d’un disc dur

Creació del sistema de fitxers.

<img src="https://images.pcworld.com/images/article/2012/01/windows-7-clean-install-a-10829904.jpg" height="350">

+++

### Clonació d’un disc dur

* Fer còpia exacta de la informació d'una màquina a una altra.
  * Salvaguardar informació
  * Replicar sistema ràpidament

<img src="https://www.tecmint.com/wp-content/uploads/2016/08/Select-Disk-to-Clone.png" height="250">

---

Instal·lació de sistemes operatius i configuració de paràmetres bàsics
----------------------------------------------------------------------


+++

### Instal·lació del sistema operatiu

Mètodes:
* Instal·lació nova
* Actualització _(upgrade)_
* Migració

+++

<img src="https://www.wikihow.com/images/thumb/f/f9/Upgrade-from-Windows-Vista-to-Windows-7-Step-9.jpg/aid718976-v4-728px-Upgrade-from-Windows-Vista-to-Windows-7-Step-9.jpg">

+++

Orígen
-   CD/DVD
-   USB
-   disc dur
-   xarxa
-   clonació
-   etc...

+++

<img src="https://www.howtogeek.com/wp-content/uploads/2015/01/sfi_full-650x300.png">

+++

Etapes:
1. Objectius
2. Anàlisi
   * mètode?, orígen?, destí?, dual?, backup?, particionament?, tot ok?
3. Instal·lar
4. Comprovar resultats
5. Documentar

+++

<img src="https://www.wikihow.com/images/thumb/f/fc/Install-Windows-7-%28Beginners%29-Step-13.jpg/aid1733421-v4-728px-Install-Windows-7-%28Beginners%29-Step-13.jpg">

+++

### Comprovació de la instal·lació del sistema operatiu

Funciona ok?

<img src="http://i.imgur.com/J9FVf.png" height="350">

+++

### Configuració del sistema operatiu instal·lat

* Adaptar funcionament a necessitats dels usuaris
* Millorar rendiment

+++

<img src="https://upload.wikimedia.org/wikipedia/en/c/c4/Windows_Control_Panel.png"">

---

Creació d’escenaris duals amb els diferents sistemes operatius instal·lats
--------------------------------------------------------------------------

Arrencada dual = més d'un sistema operatiu al mateix equip.

Cada sistema operatiu necessita una partició.

+++

***Bootloader***: és un programa que ens deixa escollir entre els diferents sistemes i s'encarrega de carregar-lo.

<img src="https://www.groovypost.com/wp-content/uploads/2017/10/Step-10-EasyBCD-623x480.png" height="350">

+++

Actualment, màquines virtuals estan reduïnt l'ús de sistemes amb arrencada dual.

---

Normes d’utilització del programari
-----------------------------------

Manual d'usuari: com utilitzar el programari.

<img src="https://images-na.ssl-images-amazon.com/images/I/51HQk0LuDRL._SX358_BO1,204,203,200_.jpg" height="300">

---

Documentació del procés d’instal·lació i incidències
----------------------------------------------------


<img src="https://devops.com/wp-content/uploads/2015/03/continuious_documentation.jpg" height="300">

+++

Mentre es fa la instal·lació i configuració del sistema, cal documentar-ho.

Ajudarà en la implantació, manteniment i actualització.

+++

Ha de ser:
- Clara i ben organitzada
- Completa
- Sempre actualitzada

+++

Ha de contenir, com a mínim:

1. Historial del sistema informàtic
2. Manual d'usuari
3. Incidències

+++

La documentació de les incidències ha de tenir:
- Incidències
- Solucions
- Propostes de millora

