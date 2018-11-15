Gestió d'arxius en mode text
====================================

[Veure Teoria](https://jrodr236.github.io/SOM/GestioDArxiusEnModeText.html)

---

Tipus d'entorn en mode text del Windows
---------------------------------------

- **CMD**, basat en l'antic MS-DOS

+++

![cmd](http://fossbytes.com/wp-content/uploads/2016/04/speed-up-internet-connection-using-cmd.jpg)

+++

- **PowerShell**, més potent
  * Dissenyat per automatitzar tasques de l'administrador
  * Permet utilitzar comandes de cmd i Unix (Linux, Mac OS X...)

+++

![PowerShell](https://stackify.com/wp-content/uploads/2017/04/Powershell-commands-1.png)

---

Unitats
-------

Dispositius d’emmagatzematge no volàtil de
la informació.

Poden ser internes (exemple HDD) o externes (exemple pendrive).

+++

Les unitats es representen de la manera següent:

- A: i B: antics disquets
- C: i següents, disc dur i altres.

+++

![lletres d'unitat](http://www.partitionwizard.com/images/tu3001/drive-letter-is-missing-in-windows.jpg)

---

Fitxers
-------

Conjunt d’informació relacionada.

Consta de nom i extensió (indica el
tipus de fitxer).

+++

![extensions](https://i1.wp.com/www.tapscape.com/wp-content/uploads/2017/12/Extensions.jpg?fit=768%2C428&ssl=1)

---

Directoris
----------

Contenidor amb fitxers i altres directoris a dins.

Hi ha un directori arrel a la unitat.

+++

![directori](https://uis.georgetown.edu/sites/uis/files/files/upload/win10-fileexplorer-display9.jpg)

---

Format de les ordres
--------------------

-   Nom
-   Paràmetres.
    * En algunes ordres no hi ha paràmetres.
    * Són opcionals.
    * Indiquen a una ordre sobre què ha d’actuar.
-   Opcions.
    * Indiquen a una ordre com volem que s’executi.
    * S'identifiquen perquè comencen per
      * `/` **(cmd)**
      * `-` **(PowerShell)**


---

Sistema d’ajuda
---------------

+++

### PowerShell

- Ordre `Get-Help`
- Paràmetre `-?`


Executar `Update-Help` per actualitzar el sistema d'ajuda de PowerShell.

+++

### cmd

- L'ordre `help`
- Paràmetre `/?`

---

Comodins
--------

Per fer una mateixa tasca en un conjunt de fitxers.

-   **?** substituir un sol caràcter
-   **\*** substituir una
    cadena de caràcters.
---

Gestió de directoris
--------------------

Utilitzen una estructura en forma d'arbre al reves.

---

Unitats
-------

`unitat:` permet canviar la unitat activa (per exemple, `C:`).

+++

Una **unitat física** és la que podem veure i tocar, és a dir, té una
existència física real. 

+++

Una **unitat lògica** son particions de la unitat física (potser una unitat física només té una partició). S'identifiquen per lletres.

Per exemple, primera partició del disc dur (C:), segona partició del disc dur (D:), primera partició del segon disc dur (E:), etc...

+++

La **unitat activa** és aquella unitat en la que estem situats en el
moment d’executar una ordre. Ho indica l'indicador del sistema (`C:\>`).

---

Directoris i subdirectoris
--------------------------

Recordem conceptes:
- **directori**
- **directori arrel o principal**
- **subdirectori**

+++

**Directori actiu.** directori a on es situa l'usuari.

+++

Directoris especials:
- `.` directori actiu
- `..` pare del
directori actiu

---

Desplaçament en l'estructura d'arbre
------------------------------------

**Camí**: com arribar a un directori

+++

Tipus:

-   **absolut**. Des de l'arrel.
-   **relatiu**. Des del directori actual.

+++

![Relative & Absolute Paths](https://automatetheboringstuff.com/images/000032.jpg)

---

Manipulació de directoris
-------------------------

Algunes de les ordres que permeten manipular directoris son:

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|New-Item -ItemType Directory|ni ItemType Directory|md|mkdir|
|Set-Location|sl|cd|cd|
|Remove-Item|ri|rd|rmdir|

+++

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|Get-ChildItem|gci|dir|ls|
|Move-Item|mi|move|mv|
| | |xcopy| |
| | |tree|tree|

---

Gestió de fitxers
-----------------

Tipus de fitxers:
- **Executables**
- **D'usuari**

+++

Algunes de les ordres que permeten gestionar fitxers son:

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|Copy-Item|cp|copy|cp|
| | |xcopy| |
|Remove-Item|ri|del|del|

> Fixa't en que, a cmd i unix, rd/rmdir != del

+++

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|Rename-Item|rni|ren|mv|
| Move-Item|mi|move|mv|
| Get-Content|gc|type|cat|


> Fixa't que, a Unix, mv serveix per moure i per reanomenar
