Instal·lació de sistemes operatius propietaris
======================================================

* [Resum](https://gitpitch.com/jrodr236/som/master?p=InstallacioSistemesPropietaris)
* Exercicis teòrics: Pendent
* Exercicis pràctics: Pendent

Requisits tècnics del sistema operatiu que s’ha d’instal·lar
------------------------------------------------------------

Els requisits tècnics del sistema operatiu que s’ha d’instal·lar són tot
allò que volem que tingui el nostre sistema operatiu, és a dir, tots els
serveis que necessitem en el nostre sistema informàtic per poder-lo
utilitzar d’una manera còmoda i eficient.

Selecció del sistema operatiu que s’ha d’instal·lar
---------------------------------------------------

La selecció del sistema operatiu que s’ha d’instal·lar és el procés
mitjançant el qual s’avaluen les característiques dels diferents
sistemes operatius disponibles en cada moment, i en el qual es
contrasten les seves característiques amb els requeriments tècnics
establerts.

Mètodes d’instal·lació i de planificació dels paràmetres bàsics d’un disc dur
-----------------------------------------------------------------------------

### Partició d’un disc dur

Una partició del disc dur és el nom de qualsevol divisió d’un disc dur.

Cada partició pot tenir el seu propi sistema de fitxers i, d’aquesta
manera, tenir un disc dur físic que funciona en realitat com a diverses
unitats d’emmagatzematge independents. Això és útil en els usuaris que
necessiten o volen tenir diversos sistemes operatius en una mateixa
màquina o en un mateix disc dur.

Inicialment, els primers PCs estàven limitats a 4 particions. Això es va solucionar amb el particionament MBR, a on hi havien tres tipus de particions:

-   Partició primària. Són les divisions primeres del disc i només n’hi
    pot haver quatre. Seran el lloc on instal·larem el sistema operatiu.
-   Partició secundària o estesa. És un altre tipus de partició que
    actua com una partició primària; serveix per contenir moltes unitats
    lògiques en el seu interior. És l’únic tipus de partició que no
    suporta un sistema de fitxers directament.
-   Partició lògica. Ocupa un tros de la partició estesa o la seva
    totalitat, la qual s’ha formatat amb un tipus específic de sistema
    de fitxers (FAT32, NTFS, EXT, etc.).

Actualment, el particionament GPT no hi han aquestes limitacions.

> VirtualBox utilitza el particionament MBR per defecte.


### Sistema de fitxers d’un sistema operatiu Windows

Un sistema d’arxius és una estructura que permet desar la informació
d’una partició. Aquesta estructura la creem quan es formata la partició.
Hi ha diferents sistemes d’arxius i, molts cops, un mateix sistema
operatiu és capaç de reconèixer múltiples sistemes d’arxius.

Com a sistemes de fitxers, en podem indicar els següents:

-   FAT16. Va aparèixer l’any 1987. El principal defecte del FAT16 és
    que en crear particions de disc molt grans es perd molt espai.
-   FAT32. Aquest sistema d’arxius va ser introduït en Windows 95 OSR2.
    És la resposta per superar el límit de FAT16, al mateix temps que es
    manté la compatibilitat amb FAT16. Permet una grandària
    d’emmagatzematge de l’ordre de TB, i arxius de fins a 4 GB.
-   NTFS (new technology file system). És un sistema de fitxers
    dissenyat per a Windows NT, utilitzat també del Windows 2000 en
    endavant, amb l’objectiu de crear un sistema de fitxers eficient. És
    un sistema adequat per a les particions molt grans.

### Formatació d’un disc dur

La formatació és un procés mitjançant el qual es crea el sistema de
fitxers corresponent mitjançant el qual el sistema operatiu podrà
gestionar les dades de la partició.

### Clonació d’un disc dur

La clonació informàtica és el procés que consisteix a fer una còpia
exacta de la informació d’una màquina en una altra màquina. L’objectiu
d’aquest procés és salvaguardar la informació, o bé utilitzar la
informació clonada per poder-ne disposar d’una manera ràpida i còmoda en
altres equipaments informàtics.

Instal·lació de sistemes operatius i configuració de paràmetres bàsics
----------------------------------------------------------------------

### Instal·lació del sistema operatiu

La instal·lació d’un sistema operatiu és un procediment mitjançant el
qual situem el sistema operatiu prèviament seleccionat en el disc dur
d’un ordinador.

Hi ha diversos mètodes d’instal·lació d’un sistema operatiu. En funció
del dispositiu de destinació:

-   Instal·lació nova en un disc dur buit o en una màquina virtual que
    no conté cap sistema operatiu, o bé en un disc dur o en una màquina
    virtual que ja contenen altres sistemes operatius.
-   Actualització d’un sistema operatiu ja existent.
-   Migració d’un sistema operatiu a un altre sistema operatiu.

En funció de l’origen del sistema operatiu que s’ha d’instal·lar:

-   instal·lació a partir de CD/DVD
-   via disc dur
-   via xarxa
-   a partir de dispositius clonats
-   etc...

Per instal·lar un sistema operatiu seleccionat en un equipament
informàtic en general cal seguir les etapes següents:

1.  Establir els objectius del procediment.
2.  Fer una anàlisi inicial del procediment que cal dur a terme. En
    aquesta fase, cal definir si no s’ha fet en les etapes prèvies els
    aspectes següents, entre d’altres:

    a)  La classe d’instal·lació que volem aplicar al sistema operatiu        seleccionat (per exemple, una instal·lació nova, una actualització, una migració, etc.).

    b)  L’origen del procés d’instal·lació que estableix la font a partir de la qual instal·larem el sistema operatiu (per exemple, format CD/DVD, via xarxa, via clonació, etc.).

    c)  La destinació de la instal·lació estableix on es farà (per exemple, en un disc dur, en una màquina virtual, etc.).

    d)  L’existència d’escenaris duals de sistemes operatius instal·lats o per instal·lar.

    e)  La necessitat de fer còpies de seguretat.

    f)  La preparació del sistema de partició i del sistema de fitxers.

    g)  La certesa de tenir la capacitat per poder desenvolupar el procés d’instal·lació.

3.  Executar el procés d’instal·lació. En aquesta fase es posa en
    pràctica el procés d’instal·lació del sistema operatiu seleccionat.
    Per poder-la fer, cal disposar i saber interpretar la documentació
    tècnica i el manual d’instal·lació del sistema operatiu.
4.  Comprovar el resultat de la instal·lació.
5.  Documentar el procés dut a terme.

### Comprovació de la instal·lació del sistema operatiu

La comprovació del funcionament del sistema operatiu instal·lat és la
fase en la qual podem comprovar i avaluar el funcionament del sistema
operatiu instal·lat i actuar en conseqüència.

### Configuració del sistema operatiu instal·lat

La configuració del sistema operatiu és la fase del procés
d’instal·lació del sistema operatiu mitjançant la qual podem adaptar el
funcionament del sistema operatiu a les necessitats dels usuaris i també
a la millora del rendiment del sistema informàtic en general.

Creació d’escenaris duals amb els diferents sistemes operatius instal·lats
--------------------------------------------------------------------------

La doble arrencada o l’arrencada dual són diferents maneres d’anomenar
la capacitat d’un ordinador per poder tenir i iniciar més d’un sistema
operatiu que funciona en un mateix disc dur o equip.

La capacitat de poder escollir el sistema operatiu d’arrencada és
possible gràcies al carregador de l’arrencada o ***bootloader***. El
carregador de l’arrencada o bootloader és un programa informàtic que té
com a finalitat preparar tot el que necessita el sistema operatiu per
funcionar. Normalment s’utilitzen els carregadors d’arrencada
multietapes, en què diversos programes petits se sumen els uns als
altres, fins que l’últim carrega el sistema operatiu.

Podem indicar com a avantatges principals en la utilització de sistemes
operatius duals:

-   L’execució de diverses aplicacions informàtiques en diferents
    sistemes operatius.
-   Una configuració d’arrencada dual permetrà a un usuari utilitzar
    totes les seves aplicacions en un únic ordinador.
-   L’aprenentatge en la utilització d’un nou sistema operatiu sense
    abandonar el sistema operatiu antic.

    -   L’arrencada dual permet a un usuari conèixer un sistema operatiu
        nou, configurar totes les aplicacions necessàries i migrar les
        dades abans de fer el pas final d’eliminar el sistema operatiu
        antic.

-   L'arrencada dual també pot ajudar als desenvolupadors de programari
    en situacions que requereixen utilitzar diversos sistemes operatius
    per al desenvolupament i per a l’execució de les proves de
    funcionament. Això pot ajudar a reduir costos de maquinari.

Actualment, la utilització de màquines virtuals està reduïnt l'ús de sistemes amb arrencada dual, ja que també permeten executar més d'un sistema operatiu en un equip.


Normes d’utilització del programari
-----------------------------------

El manual d’usuari o la documentació de la utilització del sistema
operatiu instal·lat i configurat és un conjunt de normes o de propostes
dirigides als futurs usuaris del sistema operatiu i que tenen com a
objectiu principal donar a conèixer la manera d’utilitzar aquest
programari amb la finalitat que els usuaris en puguin obtenir el màxim
rendiment d’una manera còmoda i eficient.

Documentació del procés d’instal·lació i incidències
----------------------------------------------------

La documentació del procés d’instal·lació i de configuració d’un sistema
operatiu és el conjunt d’informació que diu què fa el sistema operatiu,
com ho fa i per a què serveix. Aquesta documentació no s’ha de deixar per
al final del procés sinó que s’ha de fer durant el mateix.

Una documentació adequada i completa del procés d’instal·lació i de
configuració d’un sistema operatiu que es vol implantar, mantenir i
actualitzar d’una manera satisfactòria, és essencial en qualsevol
sistema d’informació; no obstant això, freqüentment i erròniament és la
part a la qual es dedica menys temps i atenció.

Els estàndards bàsics de disseny de la documentació proposen seguir les
pautes següents:

-   Ha de ser clara i ben organitzada, amb seccions clarament indicades
    i estructurades en blocs.
-   Els diagrames, si n’hi ha, han de ser clars i entenedors.
-   La documentació ha de ser completa.
-   La documentació sempre s’ha de conservar actualitzada.

La documentació del sistema informàtic pot contenir, entre d’altres, les
informacions següents:

1.  La documentació del cicle de vida del sistema informàtic conté tota
    la documentació que fa referència a l’historial del sistema
    informàtic. Una manera d’organitzar aquesta informació pot ser de la
    manera següent:

    a)  El bloc general descriptiu del sistema informàtic (documentació general del sistema informàtic) conté la informació que fa referència a les característiques generals del sistema.

    b)  El bloc general descriptiu dels dispositius del sistema informàtic (documentació del maquinari) conté les característiques generals dels dispositius del sistema (per exemple, els ordinadors, les impressores, els commutadors   –switches–, els encaminadors –routers–, etc.).

    c)  El bloc general descriptiu del programari del sistema informàtic (documentació del programari corresponent al sistema operatiu instal·lat i configurat) conté les característiques generals del sistema operatiu instal·lat i configurat.

2.  La documentació o manual d’usuari del sistema operatiu conté tota la
    informació que necessita l’usuari per poder utilitzar de manera
    correcta el sistema operatiu instal·lat i configurat. Aquesta
    informació es pot fer arribar als usuaris mitjançant cursos de
    formació sobre el funcionament de determinats aspectes del sistema
    informàtic o mitjançant la documentació corresponent en què
    s’explica el funcionament del sistema que s’ha d’utilitzar.
3.  La documentació d’incidències, de solucions i les propostes de
    millora del sistema operatiu instal·lat i configurat conté
    informació de les situacions especials succeïdes en el sistema i que
    han provocat modificacions en el rendiment del mateix sistema. També
    contenen les possibles propostes de solucions i la justificació de
    l’opció adoptada. Aquesta documentació també pot contenir estudis
    referents a la viabilitat en un moment determinat del sistema i
    avaluar-ne la continuïtat. Moltes vegades la documentació d’aquest
    apartat pot ser inclosa en la documentació del cicle de vida d’un
    sistema informàtic (documentació general del sistema informàtic,
    documentació del maquinari i documentació del programari).
