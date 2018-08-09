Utilització del sistema operatiu
========================================

[Veure Teoria](https://jrodr236.github.io/SOM/UtilitzacioSistemesPropietaris.html)

Comptes d'usuari
----------------

Identifiquen a l'usuari.

Els gestiona l'administrador.

L'administrador té tots els drets, permisos i atributs del sistema. No fer-lo servir per tasques convencionals.

+++

Informació compte d'usuari:
- login
- password
- tipus (administrador, convidat, etc...)

---


Arrencada i parada del sistema.
-------------------------------

+++

### Sessions

Iniciar sessio = accedir al sistema per utilitzar-lo.

Sessió = estat en què s'utilitza el sistema.

+++

### Procés d'arrencada del sistema informàtic

Responsable de posar en marxa un sistema informàtic:
- Servidor = administrador
- Estació de treball = usuari

+++

Procés arrencada:
+ Sistemes **BIOS**:
    * **POST**: test
    * Buscar unitat arrencable
    * Buscar 1r sector (**MBR**) del disc arrencable o 1r sector de CD/DVD.
* Sistemes **UEFI**: procés molt més ràpid i complex.
* Després (**BIOS & UEFI**)
    - Càrrega nucli (***kernel***) del sistema operatiu
    - Arrencada mode text / entorn gràfic
    - Inici de sessió
    - Execució de diferents fitxers

+++

### Tancar el sistema

No acabar sessió apagant directament l'ordinador, ni la màquina virtual.

---

Utilització del sistema operatiu
--------------------------------

Interfície d'usuari: entorn de treball per interaccionar amb el sistema operatiu.

Modes bàsics:
* Menús
* Gràfics (*GUI*)
* Text