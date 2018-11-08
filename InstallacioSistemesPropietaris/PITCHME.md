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

---

Mètodes d’instal·lació i de planificació dels paràmetres bàsics d’un disc dur
-----------------------------------------------------------------------------

+++

### Partició d’un disc dur

* Divisió d'un disc dur.
* Cada partició és una unitat d'emmagatzematge independent.
* MBR (Antic, per defecte a màquines virtuals)
  * 4 particions primàries màxim
  * Les primàries poden ser esteses, que tenen lògiques a dins (tantes com necessitis)
* GPT (Actual): sense aquestes limitacions

+++

### Sistema de fitxers d’un sistema operatiu Windows

És una estructura que permet desar informació a una partició.

NTFS: sistema per defecte a Windows.

+++

### Formatació d’un disc dur

Creació del sistema de fitxers.

+++

### Clonació d’un disc dur

* Fer còpia exacta de la informació d'una màquina a una altra.
  * Salvaguardar informació
  * Replicar sistema ràpidament

---

Instal·lació de sistemes operatius i configuració de paràmetres bàsics
----------------------------------------------------------------------


+++

### Instal·lació del sistema operatiu

Mètodes:
* Instal·lació nova
* Actualització
* Migració

+++

Orígen
-   CD/DVD
-   disc dur
-   xarxa
-   clonació
-   etc...

+++

Etapes:
1. Objectius
2. Anàlisi
   * mètode?, orígen?, destí?, dual?, backup?, particionament?, tot ok?
3. Instal·lar
4. Comprovar resultats
5. Documentar

+++

### Comprovació de la instal·lació del sistema operatiu

Funciona ok?

+++

### Configuració del sistema operatiu instal·lat

* Adaptar funcionament a necessitats dels usuaris
* Millorar rendiment

---

Creació d’escenaris duals amb els diferents sistemes operatius instal·lats
--------------------------------------------------------------------------

Arrencada dual = més d'un sistema operatiu al mateix equip.

Cada sistema operatiu necessita una partició.

+++

***Bootloader***: és un programa que ens deixa escollir entre els diferents sistemes i s'encarrega de carregar-lo.

Actualment, màquines virtuals estan reduïnt l'ús de sistemes amb arrencada dual.

---

Normes d’utilització del programari
-----------------------------------

Manual d'usuari: com utilitzar el programari.

---

Documentació del procés d’instal·lació i incidències
----------------------------------------------------

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
