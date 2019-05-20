Projecte UF3: campionats mundials d'esports per a cecs
==================================================

**Notes del professor**

Descripció
----------

Farem el sistema informàtic per al campionat d'un esport per a cecs.

Utilitzarem els servidors enrackables Dell, un rack i dos switchos. Com a recurs secundari, s'utilitzaràn màquines virtuals, Raspberry Pi. També tindrem a l'abast els PCs assignats a cada alumne, cablejat elèctric, de xarxa i de vídeo, monitors extra, CD/DVDs, pendrives, lectors de microSD.

Ho farem en grups. Han de sortir 5 grups per cada classe (~3 persones per grup)

[NO EXPLICAR-HO] Utilitzarem la metodologia [Scrum](https://ca.wikipedia.org/wiki/Scrum) com a metodologia didàctica.

Un cop fets els grups, haureu d'escollir un esport (no es poden repetir). Aquí teniu alguns [exemples d'esports per a cecs](https://www.fcecs.cat/esports/).

Feu-vos un selfie amb els integrants del grup, i envieu-lo per correu al professor, incloent l'esport escollit i els vostres noms.


Pissarra & Post-Its
--------
```
SPRINT 4    dataInici->dataFi    DEMO: data
-------------------------------------------
Requeriments |   To Do   |  Doing  |  Done 
-------------------------------------------
[___]        | [___]     | [___]   | [___]
[___]        | [___]     |         | [___]
[___]        |           |         | [___]
[___]        |           |         | [___]
-------------|           |         | [___]
nom          |           |         | [___]
nom          |           |         | 
nom          |           |         | 
```


```
+-------------------------------+
|                     t.        |
|       NOM           previst   |
|      TASCA                    |
|                     t.        |
| [responsable(s)]    utilitzat |
+-------------------------------+
```

Product Backlog (requeriments)
---------------

Es corresponen, més o menys, amb els continguts i resultats d'aprenentatge d'aquesta UF.

1. Instal·lar el sistema operatiu
   - Competició internacional: idioma anglès, teclat català.
   - Usuaris i tècnics cecs: sense entorn gràfic
   - Sistema operatiu: Ubuntu Server
   - Particions: sistema i dades d'usuaris en particions separades.
2. Crear usuaris de forma massiva
   - A partir d'un excel, s'ha de generar la creació d'usuaris.
   - PISTA: https://www.linuxquestions.org/questions/linux-newbie-8/non-interactive-way-to-set-a-password-825627/
3. Accedir al sistema remotament
   - En mode comandes
4. Crear manual d'ús de comandes de gestió d'arxius.
   - Només text
   - ls, cd, mkdir, rmdir, cp, mv...
5. Afegir informació de benvinguda
   - A tots els usuaris
   - Carpetes i arxius:
     - Benvinguda.txt
     - Manual_sistema
       - Fitxer(s) del manual
     - Reglament
       - Normes.txt
       - Resum.txt
6. Mantenir el sistema actualitzat
7. Configurar xarxa
   - PISTA: >=16.10 (?), netplan; altres clàssic (interfaces)
   - DHCP TI1: 172.21.1.0 -> 172.21.3.255 (255.255.0.0 || /16)
   - DHCP TI2: 172.22.1.0 -> 172.22.3.255 (255.255.0.0 || /16)
8. Fer còpia de seguretat dels arxius dels usuaris.
   - En format tar.gz
9. Recuperar sistema
   - Simular que peta el hardware (no fer-ho, realment) i recuperar el sistema (en una raspberry)
   - Els fallarà pels propietaris
10. Afegir àrbitres
    - Grup àrbitres, grup esportistes
11. Suprimir accés a un usuari
    - L'últim que es va crear.
12. Eliminar Resum.txt per tots els usuaris.
13. Crear una nova partició
    - Redimensionar la partició /
    - Muntar la nova a /var
    - Pista: live-cd/pen & gparted
14. Fer un únic reglament
    - A /var/reglament
    - Permisos: àrbitres tot, esportistes lectura
    - Afegir enllaç simbòlic
15. Bústia de suggeriments
    - A /var/suggeriments.txt
    - Permisos: tothom pot escriure
    - Afegir enllaç simbòlic al directori de **tots** els usuaris
16. Notícies
    - A /var/noticies.txt
    - Permisos: només l'usuari _cm_ (_community manager_) hi pot escriure. Tota la resta han de poder llegir i prou.
    - Afegir enllaç simbòlic al directori de **tots** els usuaris.
17. No permetre accés a arxius de l'usuari esborrat
18. Crear servidor web
    - Instal·lar apache2
    - Afegir una petita web de l'esport escollit a /var/www/html/index.html (\<h1\> i \<p\>)
    - S'hi podrà accedir amb http://IP
19. Gestionar servidor web
    - explicar què és un servei: aplicació en 2n plà, esperant a respondre a peticions
    - systemctl
    - parar servei apache2, perquè encara no està a punt el web
    - Afegir una imatge al web
    - Veure estat del servei
    - Iniciar servei
20. Gestionar processos
    - [jo, creo procès molt costós] while true; do true; done
    - han de trobar comanda per monitoritzar processos (top)
    - han de trobar comanda per matar processos. Llavors, matar el que ocupa molta CPU
21. Automatitzar backups
    - Què s'ha de copiar? Totes les dades dels usuaris
    - Quan? Automàticament, cada dia a les 4:00h
    - On? A /var/backups (suposarem que el pendrive està muntat aquí)
    - Han de desar-se només les últimes 7 còpies de seguretat. Les anteriors s'han de borrar
    - Descarregar backup, utilitzant el protocol sftp (integrat a ssh). Explicar: nautilus, ctrl+l, sftp://IP
    - Com encarar això? Divideix i venceràs
       1. Recuperar la comanda que còpia tot /home
       2. Trobar la manera per esborrar els fitxers amb més de 7 dies.
       3. Crear un shell script: un fitxer amb les comandes a fer, una darrera de l'altre, que es pugui executar.
       2. Investigar el programa cron, per automatitzar tasques.
22. Monitoritzar /home
    - Automàticament, cada hora, escriure l'espai ocupat de /home en un arxiu anomenat /var/www/html/espai-home.html.
    - L'arxiu ha de ser semblant a:
      ```
      <h1>MONITORITZACIÓ DE /HOME</h1>
      <p>
      21:00 - 21MB
      22:00 - 21.5MB
      ...
      ```
    - Pista: trobar per què serveix `<`, `>` i `>>` a Linux.
23. Fitxers amb drets d'escriptura en el seu grup
    - Volem explicar als esportistes que vagin en compte amb els fitxers que deixin obert el permís d'escriptura al seu grup o a tothom.
    - Hem trobat la solució aquí: https://ryanstutorials.net/linuxtutorial/piping.php
      ```
      ls -l ~ | grep '^.....w'
      ```
    - Un cop feta la presentació, un esportista et pregunta com funciona aquesta comanda. Prepara't per respondre.
24. Directori de suggeriments
    - Amb 1 arxiu, els participants es trolegen els suggeriments entre si
    - Utilitzar Sticky Bit a un directori perquè cada participant pugui posar o treure només els seus propis suggeriments.


Reunions
--------
- Daily Scrum -> a l'inici de cada dia
  - Posar post-its
  - Preguntes:
    - Què has fet des d'ahir?
    - Què faràs avui?
    - Quins problemes t'impedeixen arribar als teus objectius del Sprint?
- Sprint review + Scrum Planning Meeting -> cada dos setmanes
   - Quins ítems del backlog han finalitzat + demo + canvis backlog
   - Tasques a fer, hores per cada tasca (3*8=24h)


Planificació
------------
33h total UF

Sprints de 1 setmana: 4h (cada alumne)

33h / {4h/sprint} = 8,25 sprints (seràn menys per vagues, sortides, imprevistos, etc...)

Un grup de 3 alumnes, cada sprint tenen 3*4h de hores de _treballador_.

Exàmen
------
Individuals. Es demanaràn coses relacionades amb el projecte. Mínim nota mitjana de 4 per aprovar UF. Això garantirà que tots els alumnes aprovats han assolit els coneixements mínims.

* 1a prova
  * Instal·lar ubuntu server a una màquina virtual, amb
    * RAM: 1GB
    * idioma anglès, teclat castellà/català
    * particions: principal (10GB), usuaris (15GB), swap (1GB)
  * Crear 2 usuaris nous
  * Crear 4 directoris (2 directoris i 2 subdirectoris)
  * Actualitzar el sistema
* 2a prova; Cal tenir SO a una VM
  * Comprimir (tar.gz)
  * Descomprimir
  * Canviar propietari
  * Afegir contingut a fitxer (nano)
  * Copiar fitxers
  * Moure fitxers
  * Copiar directoris
  * Moure directoris
  * Eliminar fitxers
  * Eliminar directoris buits
  * Eliminar directoris plens
* 3a prova: rutes abs/rel & particions
  * Copiar & moure arxius utilitzant rutes absolutes
  * Copiar & moure arxius utilitzant rutes relatives
  * Crear nou disc a la màquina virtual
  * Crear dues particions del nou disc
  * Visualitzar les particions creades (comanda)
  * Donar format a les particions: ext4
  * Muntar una partició amb comandes
  * Muntar l'altra partició de forma permanent
* 4a prova
  * Crear usuaris
  * Crear grups
  * Afegir usuaris a un grup com a principal
  * Afegir usuaris a un grup com a secundari
  * Fer que un fitxer pugui ser llegit i modificat per tothom
  * Fer que un fitxer pugui ser llegit per tothom, però modificat només pel grup principal del propietari (i també per l'usuari)
  * Fer que un fitxer pugui ser llegit per tothom, però modificat només per l'usuari propietari
  * Fer que un fitxer pugui ser llegit pel grup propietari, llegit i modificat per l'usuari propietari, i la resta res.
  * Fer que un fitxer pugui ser llegit i modificat per l'usuari propietari, i la resta res


Hores
-----

### Grup A
- divendres 1/2 -> Explicat el projecte
- dimarts 5/2 -> _EXAMEN UF2_
- divendres 8/2 -> 2h (6h)
- dimarts 12/2 -> VAGA
- divendres 15/2 -> 2h (6+6=12h)
- dimarts 19/2 -> 2h (12+6=18h)
- divendres 22/2 -> 2h (18h+6=24h)
- dimarts 26/2 -> DEMO1 + 2h (6h)
- divendres 1/3 -> 2+2=4h (6+6=12h)
- dimarts 5/3 -> 4+2=6h (12+6=18h)
- divendres 8/3 -> VAGA
- dimarts 12/3 -> EXAMEN1
- divendres 15/3 -> Barallant-nos amb el rack + tothom IP estàtica + posaproxy (no comptem hores)
- dimarts 19/3 -> 6+2=8h
- divendres -> MARENOSTRUM
- dimarts 26/3 -> DEMO2! i posar examen
- divendres 29/3 -> EXAMEN2
- dimarts 2/4 -> 2h
- divendres 5/4 -> 4h
- dimarts 9/4 -> 6h
- divendres 12/4 -> 7h (no anava la xarxa als servers)
- divendres 23/4 -> 1h (hem anat a veure teatre St. Jordi)
- divendres 26/4 -> DEMO3 (revisar kanban, penjar foto a classroom)
- dimarts 30/4 -> EXAMEN3
- dimarts 7/5 -> 4h
- divendres 10/5 -> 6h
- dimarts 14/5 -> 8h
- divendres 17/5 -> DEMO4 +2h
- dimarts 21/5 -> EXAMEN4
- ...

### Grup B
- dimecres 30/1 -> Explicat el projecte
- dilluns 4/2 -> _EXAMEN UF2_
- dimecres 6/2 -> 2h (6h)
- dilluns 11/2 -> 2h (6+6=12h)
- dimecres 13/2 -> 2h (12+6=18h)
- dilluns 18/2 -> 2h (18+6=24h)
- dimecres 20/2 -> DEMO + 2h (6h)
- dilluns 25/2 -> 2+2=4h (6+6=12h)
- dimecres 27/2 -> 4+2=6h (12+6=18h)
- dilluns 4/3 -> FESTA
- dimecres 6/3 -> 6+2=8h (18+6=24h)
- dilluns 11/3 -> DEMO2 + 2h
- dimecres 13/3 -> EXAMEN1
- dilluns 18/3 -> 2+2=4h + posaproxy
- dimecres 20/3 -> 4+2=6h
- dilluns 25/3 -> hem posat cables al rack, i 2+6=8h
- dimecres -> 27/3 -> DEMO3! i posar examen
- dilluns 1/4 -> EXAMEN
- dimecres 3/4 -> 2h
- dilluns 8/4 -> 4h
- dimecres 10/4 -> 6h
- dimecres 24/4 -> 8h
- dilluns 29/4 -> DEMO4 (revisar kanban, penjar foto a classroom)
- dilluns 6/5 -> EXAMEN3
- dimecres 8/5 > 4h
- dilluns 13/5 -> 6h
- dimecres 15/5 -> 8h
- dilluns 20/5 -> DEMO5 +2h
- dimecres 22/5 -> EXAMEN4
- ...


