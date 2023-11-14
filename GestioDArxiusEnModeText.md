Gestió d'arxius en mode text
====================================


Tipus d'entorn en mode text del Windows
---------------------------------------

Les versions actuals de Microsoft Windows compten amb dues interfícies
d'usuari en mode text:

-   El símbol del sistema (**cmd.exe**): està basat en l'antic sistema
    operatiu **MS-DOS**.

    -   DOS és una família de sistemes operatius per a PC, monousuari i
        monotasca. El nom són les sigles de disk operating system
        (sistema operatiu de disc). Va ser creat originalment per als
        ordinadors de la família IBM PC, que utilitzaven els
        microprocessadors Intel 8086/8088 de 16 bits, i va ser el primer
        sistema operatiu popular en aquesta plataforma.
    -   Hi ha diverses versions de DOS. La més coneguda és l’MS-DOS, de
        Microsoft. Altres sistemes són el PC-DOS, el DR-DOS i més
        recentment el FreeDOS.

        ![cmd](http://fossbytes.com/wp-content/uploads/2016/04/speed-up-internet-connection-using-cmd.jpg)

-   Windows **PowerShell**: s'ha creat per substituïr el símbol del sistema; és molt més potent i modern.
    -   Està dissenyat per al seu us per part dels administradors de
        sistemes, amb el propòsit d'automatitzar tasques o realitzar-les
        de forma més controlada.
    - Per facilitar el seu ús, permet utilitzar-hi algunes comandes bàsiques de cmd i de Unix (Linux, Mac OS X...)

      ![PowerShell](https://stackify.com/wp-content/uploads/2017/04/Powershell-commands-1.png)

Unitats
-------

Les unitats són els dispositius d’emmagatzematge no volàtil de
la informació. Aquestes unitats poden ser internes, com el disc dur, o
externes, com els pendrives, DVDs o cintes magnètiques.

Les unitats es representen de la manera següent:

-   Unitat de disquets: A: (unitat principal de disquets).
-   Unitat de disquets: B: (unitat secundària de disquets).
-   Unitat de discos durs: C: (primera partició de la unitat de disc
    dur).

A les altres particions, unitats magnètiques, òptiques, flash... se’ls
assignen les lletres següents per ordre alfabètic.

![lletres d'unitat](http://www.partitionwizard.com/images/tu3001/drive-letter-is-missing-in-windows.jpg)

Fitxers
-------

Un fitxer és el nom que donem a un conjunt d’informació relacionada, és
a dir, a una col·lecció d’informació homogènia, amb un distintiu comú de
referència.

A Windows el distintiu consta de nom i extensió. L'extensió indica el
tipus de fitxer (exe, docx, pdf...).

![extensions](https://i1.wp.com/www.tapscape.com/wp-content/uploads/2017/12/Extensions.jpg?fit=768%2C428&ssl=1)

Directoris
----------

Un directori és un contenidor, a on hi poden haver fitxers o altres directoris a dins. S'emmagatzema internament en forma de taula de fitxers en què cadascuna de les entrades
desa informació referida a aquests fitxers.

Una unitat d’emmagatzematge comença per un directori arrel, que contindrà fitxers i/o directoris.

Igual que en els fitxers, els directoris han de tenir un nom, i les
regles d’assignació són les mateixes que les indicades en el cas dels fitxers, però no és normal assignar
extensions als directoris.

![directori](https://uis.georgetown.edu/sites/uis/files/files/upload/win10-fileexplorer-display9.jpg)

Format de les ordres
--------------------

Tota ordre és formada per:

-   Nom de l’ordre.
-   Paràmetres. En algunes ordres no hi ha paràmetres. Són opcionals.
    Indiquen a una ordre sobre què ha d’actuar.
-   Opcions. Les opcions indiquen a una ordre com volem que s’executi;
    això ho podem interpretar en el sentit que hi ha ordres que podem
    ordenar que s’executin de maneres diferents en funció de les nostres
    necessitats. Són opcionals. S’identifiquen, perquè
      * comencen pel
    caràcter `/` **(cmd)**
      * comencen pel caràcter `-` **(PowerShell)**

      
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

Sistema d’ajuda
---------------

### PowerShell

L'ordre `Get-Help` mostra ajuda de les comandes de PowerShell. En el cas de necessitar ajuda sobre una ordre completa, es pot utilitzar el paràmetre `-?`.

Executar `Update-Help` per actualitzar el sistema d'ajuda de PowerShell.


### cmd

L'ordre `help` ens mostra ajuda de les comandes. En cas de necessitar
ajuda sobre una ordre completa podem utilitzar el paràmetre `/?`.



Comodins
--------

Si volem fer una mateixa tasca per a un conjunt de fitxers, no és
necessari repetir l’ordre corresponent una vegada per a cada fitxer,
sinó que podem utilitzar els comodins per especificar el conjunt de
fitxers. Es poden utilitzar tant per representar els noms de fitxers com
per a l’extensió dels fitxers. Hi ha dos caràcters que actuen com a
comodins:

-   Interrogació (**?**). Aquest símbol s’utilitza per substituir un sol
    caràcter i qualsevol caràcter.
-   Asterisc (**\***). Aquest símbol s’utilitza per substituir una
    cadena de caràcters.

Gestió de directoris
--------------------

Per organitzar les dades en els discos els sistemes de Microsoft fan
servir una estructura en arbre. Aquesta estructura té com a base: les
unitats, els directoris i els fitxers.

La posició que adopten les unitats, els directoris i els fitxers dins de
l’organització de les dades recorda un arbre al revés, en el qual tenim
les unitats (arrels), el directori principal o arrel (tronc), format per
alguns subdirectoris (branques) en què es troben els arxius (fulles).

Unitats
-------

Les **unitats** són els suports en què s’emmagatzema la informació. Es
representen per una lletra.

L'ordre `unitat:` permet canviar la unitat activa (per exemple, `C:`).

Una **unitat física** és la que podem veure i tocar, és a dir, té una
existència física real. 

Una **unitat lògica** és la que s’obté a partir d’una unitat física per
successives divisions (particions). Pot ser que una unitat física tingui només una partició i, per tant, una sola unitat lògica. Per identificar les unitats lògiques s’utilitzen lletres. Podem utilitzar fins a la
lletra Z. Per exemple, primera partició del disc dur (C:), segona partició del disc dur (D:), primera partició del segon disc dur (E:), etc...

La **unitat activa** és aquella unitat en la que estem situats en el
moment d’executar una ordre. Una manera de saber-ho cal només observar
l’indicador del sistema. La primera lletra que s’indica en ell es
correspon amb la unitat activa (`C:\>` aquest indicador del sistema
operatiu ens informa que tenim com a unitat activa la C).

Directoris i subdirectoris
--------------------------

Un **directori** és una taula de fitxers en què cadascuna de les
entrades desa informació relacionada amb aquests fitxers. Cada unitat
activa té una zona situada en el primer sector d’arrencada en què se
situa el directori arrel a partir del qual s’organitza l’estructura en
arbre.

**Directori arrel o principal.** Aquest directori es crea en el moment
de formatar el disc, és únic i és el directori principal dels discos. Hi
podem posar altres directoris i/o fitxers dins. El directori arrel es
representa pel símbol \\.

**Subdirectori.** És un directori creat dins d’un altre directori. S’hi
poden emmagatzemar fitxers i/o subdirectoris nous.

**Directori actiu.** És el punt de l’estructura en arbre on se situa
l’usuari, preparat per executar una ordre. El directori actiu canviarà
segons anem navegant per l’estructura en arbre. L’indicador del sistema
informa de la unitat i del directori actiu en cada moment.

Hi ha dos directoris especials: el directori `.` (punt, representa el
directori actiu) i el directori `..` (punt-punt, representa el pare del
directori actiu).

Desplaçament en l'estructura d'arbre
------------------------------------

El **camí** en una estructura en arbre fa referència a la trajectòria
que cal seguir per arribar a un determinat lloc d’aquesta organització.

Per fer referència al camí cal indicar: el nom de la unitat, els noms
dels diferents directoris pels quals hem de passar amb el símbol \\ com
a separació entre cadascun d’ells i el nom del fitxer.

Hi ha dues maneres d’indicar el camí en una estructura d’arbre:

-   Mitjançant el **camí absolut**. És el camí en què sempre es comença
    en el directori arrel o principal de l’estructura en arbre.

-   Mitjançant el **camí relatiu**. És el camí en què sempre es comença
    a partir del lloc on som situats en l’estructura en arbre.

![Relative & Absolute Paths](https://automatetheboringstuff.com/images/000032.jpg)

Manipulació de directoris
-------------------------

Tots els directoris tenen l’origen en el directori arrel i dins dels
directoris i subdirectoris s’emmagatzemen els fitxers.

Algunes de les ordres que permeten manipular directoris son:

|PowerShell|abreviació|cmd|Unix|
|---|---|---|---|
|New-Item -ItemType Directory|ni -ItemType Directory|md|mkdir|
|Set-Location|sl|cd|cd|
|Remove-Item|ri|rd|rmdir|
|Get-ChildItem|gci|dir|ls|
|Move-Item|mi|move|mv|
| | |xcopy| |
| | |tree|?|


Gestió de fitxers
-----------------

Un fitxer o arxiu és un conjunt d’informació homogènia emmagatzemada en
un directori del disc.

Podem diferenciar els tipus de fitxers:

-   **Fitxers executables**. Són un tipus de fitxers que el sistema és
    capaç d’executar. Són els que tenen l’extensió COM, EXE i BAT.

<!-- -->

-   **Fitxer d'usuari**. Són fitxers creats pels usuaris i que el
    sistema no pot manipular d’una manera directa, cal utilitzar
    programes de suport. Per exemple, els fitxers amb l’extensió DOCX, ODT, HTML, etc...

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
