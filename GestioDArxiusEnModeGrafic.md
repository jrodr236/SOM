Gestió d'arxius en mode gràfic
====================================


* [Resum](https://gitpitch.com/jrodr236/som/master?p=GestioDArxiusEnModeGrafic)
* Exercicis teòrics: _moodle_
* [Exercicis pràctics](ExercicisGestioDArxiusEnModeGrafic.md)

Per a la gestió dels directoris i dels fitxers en mode gràfic, els sistemes Windows disposen d’eines gràfiques que podem utilitzar per gestionar tots els aspectes relacionats amb aquest tema, per exemple, l'explorador d'arxius.

Aquestes eines gràfiques que permeten fer les accions següents:
* Gestió dels directoris: crear-los, visualitzar-los, eliminar-los, moure’ls, canviar-los el nom, desplaçar-los per l’estructura d’arbre, etc.
* Gestió dels fitxers: crear-los, visualitzar-los, copiar-los, eliminar-los, canviar-los el nom, etc.
* Gestió dels permisos: la creació, la modificació, la gestió del propietari, del grup del propietari i dels altres usuaris.

![File Explorer](https://kbdevstorage1.blob.core.windows.net/asset-blobs/11934_en-us_2)

Gestió dels permisos d’accés a fitxers i directoris
------------------------------

L'element bàsic per a articular la seguretat d'arxius i directoris son els permisos d'accés als usuaris o grups. El propietari de cada arxiu o directori serà l'encarregat de concedir-los.

Els tipus d’accés bàsics que es poden donar són els següents: llegir, escriure, executar, afegir, esborrar, etc.

El procés per a la gestió dels permisos es realitza des de la opció Propietats del menú contextual (botó dret del ratolí) dels arxius i carpetes, a la pestanya Seguretat.

En Windows, aquest tipus de permisos es concedeixen a dos nivells:
* Els permisos per compartir en xarxa (No entra al temari d'aquest mòdul professional).
* Els permisos locals. Estan disponibles per a unitats formatades amb el sistema NTFS (no existeixen en unitats FAT).

Permisos estàndards NTFS per a fitxers:
* **Lectura**: Veure el contingut del fitxer, les seves dades, els seus atributs i permisos, i tenir-hi accés.
* **Escriptura**: Afegir dades al fitxer, escriure’n els atributs i visualitzar-ne els permisos.
* **Lectura i execució**: Veure el contingut del fitxer, els seus atributs i permisos, executar-lo i tenir-hi accés.
* **Modificació**: Llegir, escriure i/o eliminar el fitxer.
* **Control total**: Llegir, escriure, modificar i/o eliminar el fitxer, a més de canviar permisos i prendre la possessió del fitxer.



Permisos estàndards NTFS per a directoris:
* **Lectura**: Veure els fitxers i subdirectoris del directori corresponent i fer-ne una llista.
* **Escriptura**: Afegir fitxers i subdirectoris al directori corresponent.
* **Lectura i execució**: Veure fitxers i subdirectoris del directori corresponent i fer-ne una llista, a més d’executar fitxers.
* **Modificació**: Escriptura, lectura i execució, a més de poder eliminar el directori.
* **Llistar el contingut**: Veure fitxers i directoris i fer-ne una llista.
* **Control total**: Totes les acciones permeses per a la resta de permisos; a més, pot canviar els permisos del directori, prendre possessió de qualsevol subdirectori o fitxer i eliminar-los.

![Permisos NTFS de directori estàndards](https://www.sqa.org.uk/e-learning/ClientOS02CD/images/pic002.jpg)

Alguns aspectes a tenir en compte respecte als permisos:
* Els permisos es poden concedir, denegar o simplement no preveure’ls i sempre preval la denegació.
    - Si, per exemple, un usuari no té concedit el permís de lectura sobre un arxiu, ni com a usuari ni com a grup, no podrà accedir al contingut.
    - Així mateix, si, d’una banda, té concedit el permís i, de l’altra, el té denegat explícitament, tampoc no podrà accedir al fitxer.
* Els permisos de directoris i fitxers poden ser contradictoris, en cas que prevalgui el permís sobre el fitxer.
    - De totes maneres, si un usuari pot eliminar arxius d’una carpeta, els permisos sobre el fitxer no ho podran impedir.
* Per defecte, els permisos s’hereten des del directori pare.
    - Això provoca que s’alterin en copiar un arxiu o directori, encara que es conserven si es tracta de canviar-los d’ubicació dins de la unitat lògica.

Generalment, tot el que necessitarem per protegir els directoris i els fitxers són els permisos estàndard (indicats anteriorment). No obstant això, si volem poder crear un sistema personalitzat de permisos, podem utilitzar els permisos avançats.

Els permisos avançats per a directoris i arxius són:
* Recórrer carpetes / executar arxiu
    - El permís recórrer carpeta (només afecta els directoris) implica el desplaçament per les carpetes.
    - El permís executar arxiu implica l’execució d’arxius de programa.
* Fer una llista de carpetes / llegir dades
    - El permís fer una llista de carpetes (només afecta els directoris) implica visualitzar els noms dels arxius i directoris de la carpeta.
    - El permís llegir dades implica visualitzar les dades dels arxius.
* Atributs de lectura
    - Implica visualitzar els atributs d’un arxiu o directori.
* Atributs estesos de lectura
    - Implica visualitzar els atributs estesos d’un arxiu o directori.
* Crear arxius / escriure dades
    - El permís crear arxius (només afecta els directoris) implica la creació d’arxius dins de carpetes.
    - El permís escriure dades (només afecta els fitxers) implica els canvis en els arxius.
* Crear carpetes / annexar dades
    - El permís crear carpetes (només afecta els directoris) implica la creació de directoris dins de la carpeta.
    - El permís annexar dades (només afecta els arxius) implica afegir contingut a l’arxiu però no canviar, eliminar ni sobreescriure les dades existents.
* Atributs d’escriptura
    - Implica el canvi dels atributs d’un arxiu o directori.
* Atributs estesos d’escriptura
    - Implica el canvi dels atributs estesos d’un arxiu o directori.
* Eliminar subcarpetes i arxius
    - Implica l’eliminació de subcarpetes i arxius.
* Eliminar
    - Implica l’eliminació de l’arxiu o directori.
* Permisos de lectura
    - Implica visualitzar els permisos de l’arxiu o directori.
* Canviar els permisos
    - Implica el canvi dels permisos dels arxius o directoris.
* Prendre possessió
    - Implica agafar la possessió de l’arxiu o directori.

![Permisos NTFS avançats](http://www.petenetlive.com/wp-content/uploads/2015/11/005-Add-NTFS-Permission-Everyone.png)

![Relació entre permisos avançats i estàndards](http://www.idp.net/ntfs/Table5.gif)

Compressió i descompressió de fitxers
-------------------------------

La compactació o l’empaquetament de fitxers i/o directoris és una tècnica que consisteix a agrupar en un únic fitxer diversos arxius i/o directoris. El procés contrari s’anomena descompactació o desempaquetament.

La compressió de fitxers i/o directoris és una tècnica basada a aplicar un algorisme que farà que l’arxiu i/o directori ocupi menys espai en el suport. El procés contrari s’anomena descompressió.

![Comprimir](http://cdn2.windows10themes.net/pics/create-a-zip-file-for-single-item.jpg)