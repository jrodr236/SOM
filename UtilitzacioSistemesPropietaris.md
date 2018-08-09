Utilització del sistema operatiu
========================================


* [Resum](https://gitpitch.com/jrodr236/som/master?p=UtilitzacioSistemesPropietaris)
* Exercicis teòrics: Pendent
* Exercicis pràctics: Pendent

Comptes d'usuari
----------------

Un compte d’usuari és una identificació que utilitzen els sistemes
operatius per gestionar l’accés dels usuaris al sistema informàtic.
Aquests comptes són gestionats per l’administrador del sistema
informàtic.

Un administrador d’un sistema operatiu és l’usuari que té tots els
drets, permisos i atributs en el sistema en què és definit. Només s'ha
de fer servir per a realitzar tasques administratives; per a l'ús normal
cal fer servir un usuari convencional.

En els sistemes operatius Windows els comptes d'usuari contenen la
següent informació:

-   Nom d'usuari o login
-   Contrasenya o password.
-   Tipus de comptes creat (administrador, convidat, etc...)

Arrencada i parada del sistema.
-------------------------------

### Sessions

Iniciar una sessió en un sistema informàtic és el procés mitjançant el
qual accedim al sistema informàtic per poder-lo utilitzar. Una sessió
representa l’estat en què s’utilitza el sistema informàtic.

### Procés d'arrencada del sistema informàtic

En un servidor, la persona responsable de posar en marxa el sistema
informàtic és l’administrador del sistema. En el cas d’una estació de
treball serà el mateix usuari.

Una vegada activat el procés d’arrencada, s’esdevenen una sèrie de fets
que explicarem tot seguit:

1.  S'executen una sèrie de rutines de la ROM-BIOS. Aquest test
    s'anomena POST (power-on self test) i comprova que tots els
    paràmetres desats en la memòria CMOS coincideixin amb els valors
    detectats en el test (per exemple, la memòria instal·lada, les
    característiques dels discos durs, etc.). Posteriorment es presenten
    aquests valors per pantalla.
2.  El BIOS investiga els dispositius (disqueteres, discos durs, unitats
    de CD/DVD, etc.), per comprovar quines són arrencables en l’ordre
    indicat al *setup* de la BIOS.
3.  Si s'arrenca des del disc dur, es llegeix el seu primer sector (MBR)
    a on està el programa que gestiona l’arrencada del sistema. Aquest,
    al mateix temps, haurà de carregar el sector d’arrencada de la
    partició d’un disc dur, que conté el sistema operatiu. En el cas de
    disquets i CD/DVD, en carregarà directament el sector d’arrencada.

    -   En cas que hi hagi més d'un sistema operatiu instal·lat, el
    carregador de sistemes operatius (com NTLDR, GRUB, etc...) es mostra
    un menú per a escollir amb quin es vol arrencar.

1.  es carrega el nucli (kernel) del sistema operatiu que està situat en
    el sector d’arrencada de la seva partició.
2.  A partir d’aquest moment, el procés d’arrencada pot ser diferent per
    a cada sistema operatiu i també depèn del mode d’arrencada que
    utilitzem (per exemple, el mode text o el mode gràfic).
3.  Al final del procés d’arrencada i si tot ha anat de manera correcta,
    l’usuari pot començar el procediments d’inici d’una sessió en el
    sistema.
4.  Durant la fase d’inici de sessió, s’executen també tot un seguit de
    fitxers entre els quals podem destacar els fitxers relacionats amb
    l’entorn de treball de l’usuari que inicia la sessió.

El procés que s'acaba d'explicar correspon als antic sistemes **BIOS**, utilitzats també pels alguns sistemes de màquines virtuals. Actualment, però, amb l'adopció d'**UEFI** en tots els sistemes moderns, els passos anteriors a la càrrega del sistema operatiu son molt més ràpids i complexos.


### Tancar el sistema

Acabar una sessió en un sistema informàtic consisteix en un procés que
pot ser més o menys complicat que dependrà del sistema operatiu
utilitzat i en el qual no podrem utilitzar el sistema operatiu a partir
d’aquest moment. Mai no es pot acabar una sessió del sistema apagant
directament l'ordinador.

Utilització del sistema operatiu
--------------------------------

La interfície d’usuari en un sistema operatiu és un entorn de treball de
què disposem els usuaris per poder interaccionar amb els sistemes
operatius, és a dir, per poder-nos comunicar i donar ordres als sistemes
operatius.

Actualment, els sistemes operatius tenen els modes bàsics de
funcionament

següents:

1.  Menús. La comunicació entre usuari i sistema es fa mitjançant la
    utilització de diferents menús d’opcions disponibles en el mateix
    sistema operatiu que s’ha d’utilitzar. Només cal seleccionar l’opció
    del menú que interessa perquè el sistema faci una acció determinada
    (per exemple, algunes versions del sistema MS-DOS, etc.).
2.  Gràfics (GUI). La manera més fàcil de comunicació entre usuari i
    sistema es basa en la utilització d’una sèrie d’elements gràfics
    (les finestres, les icones, etc.), a partir dels quals s’executen
    les accions (per exemple, l’entorn Windows de l’empresa Microsoft,
    etc.).
3.  Text. La comunicació amb el sistema es fa mitjançant ordres escrites
    segons un llenguatge determinat. En el cas del sistema operatiu
    MS-DOS, podem utilitzar com a intèrpret d’ordres el fitxer
    command.com i, en els sistemes Windows, podem utilitzar com a
    intèrpret d’ordres el fitxer cmd.exe.

