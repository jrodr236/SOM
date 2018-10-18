Conceptes del sistema operatiu
================

[Veure Teoria](https://jrodr236.github.io/SOM/ConceptesDelSistemaOperatiu.html)

---

Definició de sistema operatiu
-----------

Sistema operatiu és un programari que:

+++

* administra els recursos oferts pel maquinari per a obtenir un rendiment eficient,
+++
* controla l’execució de programes d’aplicació,
+++
* amaga els detalls del maquinari de manera que donen a l’usuari i a les aplicacions un camí senzill i flexible d’accés al sistema.

+++ 

![Operating System](https://www.supraits.com/wp-content/uploads/2018/01/Operating-Systems.png)

---

Funcions principals del sistema operatiu
------------

+++

* Administra el processador.
* Administra la memòria.
* Comunica els dispositius amb els usuaris.
* Organitza les dades per a un accés ràpid i segur.
* Gestiona les comunicacions en xarxa.

+++

* Facilita les entrades i sortides.
* Dóna tècniques de recuperació d’errors.
* Evita que altres usuaris interfereixin.
* Genera estadístiques.
* Comparteix el maquinari i les dades entre els usuaris.

---

Arquitectura del sistema operatiu
----------------

Alguns elements importants:

+++

### Nucli _(kernel)_

Controla la resta dels mòduls.

Es troba permanentment a memòria: ofereix servei inmediat.

Hi ha la part del codi del SO que s'útilitza més.

+++

![Kernel](https://ugc.kn3.net/i/origin/http://nexolinux.com/wp-content/uploads/2013/02/explore_linux_kernel.png)

+++

### Planificador del processador:

![Processor](https://i.ebayimg.com/images/g/yjkAAOSwowxZdf7j/s-l300.jpg)

+++

Controla l'accés al processador per part dels processos.

(**Procés** = programa en execució).


+++

### Administrador de memòria

![Memory](https://www.southerncomputerservices.com.au/wp-content/uploads/2018/06/RAM.jpg)

+++

Assigna RAM als programes.

Vigila que els processos no accedeixin a l'espai de memòria dels altres.


+++

### Sistema d’entrada/sortida,

Gestió dels dispositius.

Controladors _(drivers)_ permeten la comunicació entre els dispositius i el sistema operatiu.

+++

![Input/Output management](http://blog.drivethelife.com/wp-content/uploads/2015/12/device-driver.png)

+++

### Administrador d’arxius.

Estructura d'arxius habitual:

Fitxers + Directoris

+++

> Conceptes importants:
> * Camí relatiu: des de la posició actual.
> * Camí absolut: des de la posició de l'arrel.

+++

![Relative & Absolute Paths](https://automatetheboringstuff.com/images/000032.jpg)

+++

### La interfície d'usuari _(shell)_

Permeten comunicació entre usuari i sistema operatiu.

Dos tipus:
- Línia de comandes (CLI): ordres escrites.
- Interfície gràfica d'usuari (GUI): eines gràfiques.

+++

![CLI vs. GUI](http://www.itrelease.com/wp-content/uploads/2017/11/GUI-vs-CLI.png)