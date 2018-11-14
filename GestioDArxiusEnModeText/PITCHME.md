Gestió d'arxius en mode text
====================================

[Veure Teoria](https://jrodr236.github.io/SOM/GestioDArxiusEnModeText.html)

---

Tipus d'entorn en mode text del Windows
---------------------------------------

- CMD, basat en l'antic MS-DOS

+++

![cmd](http://fossbytes.com/wp-content/uploads/2016/04/speed-up-internet-connection-using-cmd.jpg)

+++

- PowerShell, més potent
  * Dissenyat per automatitar tasques de l'administrador
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
- C: i següents: disc dur i altres.

+++

![lletres d'unitat](http://www.partitionwizard.com/images/tu3001/drive-letter-is-missing-in-windows.jpg)

---

Fitxers
-------

Conjunt d’informació relacionada.

Consta de nom i extensió (indica el
tipus de fitxer.

+++

![extensions](https://i1.wp.com/www.tapscape.com/wp-content/uploads/2017/12/Extensions.jpg?fit=768%2C428&ssl=1)

---

Directoris
----------

Contenidor amb fitxers i altres directoris a dins.

Hi ha un directori arrel a la unitat.

+++

![directori](http://computertutorflorida.com/wp-content/uploads/2014/11/folder1.jpg)

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
    * S'identifiquen perquè comencen per...
      * `/` **(cmd)**
      * `-` **(PowerShell)**
<!--

Tipus d'ordres
--------------

Les ordres internes o residents són les que es transfereixen a la
memòria en el moment en què es carrega el sistema operatiu i resideixen
mentre el sistema operatiu DOS està en funcionament. Se situen en el
fitxer command.com. Algunes ordres internes són: del, md, rd, etc.

Les ordres externes són programes que no estan carregats en la memòria
mentre funciona el sistema operatiu DOS. Es troben emmagatzemades en les
unitats de disc per a la seva utilització. Una vegada donada l’ordre de
l’execució es transporten des del suport corresponent a la memòria,
s’executen i es descarreguen de la memòria. Les ordres externes tenen
com a extensió EXE, COM i BAT. Algunes ordres externes són: tree,
chkdsk, etc.

-->

---

Sistema d’ajuda
---------------

+++

### PowerShell

- Ordre `Get-Help`
- Paràmetre `-?`

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

Una **unitat física** és la que podem veure i tocar, és a dir, té una
existència física real. 

Una **unitat lògica** son particions de la unitat física (potser una unitat física només té una partició). S'identifiquen per lletres. Per exemple, primera partició del disc dur (C:), segona partició del disc dur (D:), primera partició del segon disc dur (E:), etc...

La **unitat activa** és aquella unitat en la que estem situats en el
moment d’executar una ordre. Ho indica l'indicador del sistema (`C:\\&gt;`).

---

Directoris i subdirectoris
--------------------------

+++

Un **directori** és una taula de fitxers en què cadascuna de les
entrades desa informació relacionada amb aquests fitxers. Cada unitat
activa té una zona situada en el primer sector d’arrencada en què se
situa el directori arrel a partir del qual s’organitza l’estructura en
arbre.

+++

**Directori arrel o principal.** Aquest directori es crea en el moment
de formatar el disc, és únic i és el directori principal dels discos. Hi
podem posar altres directoris i/o fitxers dins. El directori arrel es
representa pel símbol \\.

+++

**Subdirectori.** És un directori creat dins d’un altre directori. S’hi
poden emmagatzemar fitxers i/o subdirectoris nous.

+++

**Directori actiu.** És el punt de l’estructura en arbre on se situa
l’usuari, preparat per executar una ordre. El directori actiu canviarà
segons anem navegant per l’estructura en arbre. L’indicador del sistema
informa de la unitat i del directori actiu en cada moment.

+++

Hi ha dos directoris especials: el directori `.` (punt, representa el
directori actiu) i el directori `..` (punt-punt, representa el pare del
directori actiu).

---

Desplaçament en l'estructura d'arbre
------------------------------------

El **camí** en una estructura en arbre fa referència a la trajectòria
que cal seguir per arribar a un determinat lloc d’aquesta organització.

Per fer referència al camí cal indicar: el nom de la unitat, els noms
dels diferents directoris pels quals hem de passar amb el símbol \\ com
a separació entre cadascun d’ells i el nom del fitxer.
---

Hi ha dues maneres d’indicar el camí en una estructura d’arbre:

-   Mitjançant el **camí absolut**. És el camí en què sempre es comença
    en el directori arrel o principal de l’estructura en arbre.

-   Mitjançant el **camí relatiu**. És el camí en què sempre es comença
    a partir del lloc on som situats en l’estructura en arbre.

---

Manipulació de directoris
-------------------------

Tots els directoris tenen l’origen en el directori arrel i dins dels
directoris i subdirectoris s’emmagatzemen els fitxers.

---
Algunes de les ordres que permeten manipular directoris son:

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|New-Item -ItemType Directory|ni ItemType Directory|md|mkdir|
|Set-Location|sl|cd|cd|
|Remove-Item|ri|rd|rmdir|
|Get-ChildItem|gci|dir|ls|
|Move-Item|mi|move|mv|
| | |xcopy| |
| | |tree|tree|

---

Gestió de fitxers
-----------------


Podem diferenciar els tipus de fitxers:

-   **Fitxers executables**. Són un tipus de fitxers que el sistema és
    capaç d’executar. Són els que tenen l’extensió COM, EXE i BAT.

<!-- -->

-   **Fitxer d'usuari**. Són fitxers creats pels usuaris i que el
    sistema no pot manipular d’una manera directa, cal utilitzar
    programes de suport. Per exemple, els fitxers amb l’extensió DOCX, ODT, HTML, etc...

+++

Algunes de les ordres que permeten gestionar fitxers son:

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|Copy-Item|cp|copy|cp|
| | |xcopy| |
|Remove-Item|ri|del|del|
|Rename-Item|rni|ren|mv|
 Move-Item|mi|move|mv|
 Get-Content|gc|type|cat|

> Fixa't en que, a cmd i unix, rd/rmdir != del
>
> Fixa't que, a Unix, mv serveix per moure i per reanomenar


<!--

Editors i processadors de textos
--------------------------------

Les eines de què disposa el món informàtic per crear i modificar els
fitxers de tipus text es poden classificar en:

-   Els **processadors de textos** són programes específics per
    dissenyar documents escrits. Utilitzant unes marques internes
    permeten donar format al document (negreta, font, mida del text,
    etc...).
-   Els **editors de textos** són els programes que permeten escriure
    documents de tipus text sense format. Acostumen a utilitzar les
    codificacions ASCII o UNICODE. No utilitzen marques internes per a
    controlar el format d'escriptura.

L’**EDIT** és un editor de textos que permet crear, modificar i imprimir
el contingut dels fitxers de tipus text amb format ASCII d’una manera
ràpida i senzilla.


-->