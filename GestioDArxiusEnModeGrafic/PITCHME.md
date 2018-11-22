Gestió d'arxius en mode text
====================================

[Veure Teoria](https://jrodr236.github.io/SOM/GestioDArxiusEnModeGrafic.html)

---

Eines gràfiques per la gestió de directoris i fitxers en mode gràfic. Accions que podem fer:
* Gestió de directoris
* Gestió de fitxers
* Gestió de permisos

+++

![File Explorer](https://kbdevstorage1.blob.core.windows.net/asset-blobs/11934_en-us_2)

---

Gestió dels permisos d’accés a fitxers i directoris
------------------------------

Element bàsic per la seguretat d'arxius i directoris: permisos d'accés.

El propietari és l'encarregat de concedir els permisos.

On? Arxius i carpetes > menú contextual > Propietats > Seguretat.

---

A Windows, dos nivells de permisos:
* Compartir en xarxa (no els veurem)
* Permisos locals: només NTFS

+++

Permisos estàndars NTFS per a **fitxers**:
* Lectura
* Escriptura
* Lectura i execució
* Modificació
* Control total

+++

Permisos estàndars NTFS per a **directoris**:
* Lectura
* Escriptura
* Lectura i execució
* Modificació
* Llistar el contingut
* Control total

+++

![Permisos NTFS de directori estàndards](https://www.sqa.org.uk/e-learning/ClientOS02CD/images/pic002.jpg)

---

Aspectes a tenir en compte
---------------------------

+++

* Els permisos es poden concedir, denegar o simplement no preveure’ls i sempre preval la denegació.
    - Si, per exemple, un usuari no té concedit el permís de lectura sobre un arxiu, ni com a usuari ni com a grup, no podrà accedir al contingut.
    - Així mateix, si, d’una banda, té concedit el permís i, de l’altra, el té denegat explícitament, tampoc no podrà accedir al fitxer.

+++

* Els permisos de directoris i fitxers poden ser contradictoris, en cas que prevalgui el permís sobre el fitxer.
    - De totes maneres, si un usuari pot eliminar arxius d’una carpeta, els permisos sobre el fitxer no ho podran impedir.

+++

* Per defecte, els permisos s’hereten des del directori pare.
    - Això provoca que s’alterin en copiar un arxiu o directori, encara que es conserven si es tracta de canviar-los d’ubicació dins de la unitat lògica.

---

Permisos avançats
------------------

Normalment amb els permisos estàndard en tenim prou. Si no, cal utilitzar els avançats.

+++

![Permisos NTFS avançats](http://www.petenetlive.com/wp-content/uploads/2015/11/005-Add-NTFS-Permission-Everyone.png)

+++

![Relació entre permisos avançats i estàndards](http://www.idp.net/ntfs/Table5.gif)

---

Compressió i descompressió de fitxers
-------------------------------

Compactació: agrupar en un únic fitxer diversos arxius i/o directoris.

+++

Compressió: aplicar un algorisme que farà que l’arxiu i/o directori ocupi menys espai en el suport.

+++

![Comprimir](http://cdn2.windows10themes.net/pics/create-a-zip-file-for-single-item.jpg)