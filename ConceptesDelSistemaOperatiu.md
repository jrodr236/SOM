Conceptes del sistema operatiu
================

Definició de sistema operatiu
-----------

Un sistema operatiu és un conjunt de programes i funcions que:
* administren els recursos oferts pel maquinari per a obtenir un rendiment eficient,
* controlen l’execució de programes d’aplicació,
* amaguen els detalls del maquinari de manera que donen a l’usuari i a les aplicacions un camí senzill i flexible d’accés al sistema.

Funcions principals del sistema operatiu
------------

Les funcions més importants que té encomanat el sistema operatiu són les següents:

* Administra el processador.
* Administra la memòria.
* Comunica els dispositius amb els usuaris.
* Organitza les dades per a un accés ràpid i segur.
* Gestiona les comunicacions en xarxa.
* Facilita les entrades i sortides.
* Dóna tècniques de recuperació d’errors.
* Evita que altres usuaris interfereixin.
* Genera estadístiques.
* Comparteix el maquinari i les dades entre els usuaris.



Arquitectura del sistema operatiu
----------------
Els següents són alguns dels elements principals dels sistemes operatius:

### Nucli _(kernel)_

S’encarrega de controlar la resta dels mòduls i sincronitzar-ne l’execució.

És la part del sistema operatiu que es troba permanentment carregada a la memòria i, per tant, pot oferir un servei d'una manera inmediata.

És la part del codi del sistema operatiu que s'utilitza més àmpliament, i algunes de les parts dels següents elements s'hi troben integrats.

### Planificador del processador:

Getiona el processador i la manera com poden accedir al processador els diferents processos (un **procés** és programa en execució).

### Administrador de memòria

S’encarrega d’assignar certes porcions de la memòria principal (RAM) als diferents programes.

També vigila que els diferents processos no puguin accedir a l'espai de memòria dels altres processos.

### Sistema d’entrada/sortida,

S'encarrega de la gestió dels dispositius. Els controladors _(drivers)_ són els que permeten la comunicació entre els dispositius i el sistema operatiu.

### Administrador d’arxius.

S’encarrega de mantenir l’estructura de les dades dels sistemes d'emmagatzemament massius. Habitualment aquesta estructura utilitza:
- Fitxers (arxius): grups d'informació relacionades.
- Directoris (carpetes): agrupació d'arxius i altres directoris

### La interfície d'usuari _(shell)_

Les interfícies d’usuari són tots els procediments que dóna el sistema operatiu per a facilitar el treball entre els usuaris i el sistema.

Rep totes les ordres de l’usuari i dóna el control als diferents programes del sistema o a les funcions del nucli, segons les necessitats i les peticions de l’usuari.

La interfície que es vol definir entre l’usuari i el sistema pot ser de dos tipus:
- Línia de comandes (CLI): es basen en ordres escrites.
- Interfície gràfica d'usuari (GUI): es basen en la selecció d'eines gràfiques (botons, icones, etc...)