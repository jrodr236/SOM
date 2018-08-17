Codificació de la informació
============================

[Veure Teoria](https://jrodr236.github.io/SOM/CodificacioDeLaInformacio.html)

---

Definició de la informació
--------------------------

La **informació** és el resultat de la manipulació de les *dades*.

+++

![Data vs. Informació](https://cdn.business2community.com/wp-content/uploads/2014/08/data-funnel.png)


---


Elements de la informació
-------------------------

La **informació** és formada per les dades. 

Les **dades** són fets o objectes que no han estat manipulats.

+++

Els tipus de dades *bàsics* utilitzats pels ordinadors son:

* **Numèriques**.
* **Alfabètiques**.
* **Alfanumèriques**.

+++

![Tipus de dades bàsics](https://i2.wp.com/www.datanumen.com/blogs/wp-content/uploads/2017/02/data-characters.jpg)

+++

Els ordinadors també emmagatzemen dades complexes: *imatges, audio, vídeo, etc...*

![Dades complexes](https://img.haikudeck.com/mi/b0751b83c68906f93540993bb5792659.jpeg)


+++

Un **codi** és la manera diferent d’interpretar una mateixa informació.


![Números romans](https://teachables.scholastic.com/content/dam/scholastic/teachables/products/25/9780439732925_004/9780439732925_004_xlg.jpg)

---

El sistema binari
-----------------

A l'ordinador, qualsevol quantitat, frase o dada s’emmagatzema en forma de zeros i uns: **binari**.

![binari](https://img-aws.ehowcdn.com/340x221p/photos.demandstudios.com/getty/article/129/2/78468231.jpg)


---

Mesura de la informació
-----------------------
![bit vs. byte](http://www.circuitgrove.com/sites/default/files/tutorial_photos/bitbyte.svg)

---

Prefixos d’ús convencional en informàtica
-----------------------------------------


<img src="http://fossbytes.com/wp-content/uploads/2016/08/bytes-kilobyte-megabyte-representation.jpg" height="400px">

+++

![Prefixos](img/prefixos.png)


+++



* 1.024 (2¹⁰) no és 1.000 (10³).
  * preferència 1.024
* 1 kilobyte és diferent de 1 kilobit.
  * B=byte, b=bit

+++

![1024 vs. 1000](https://qph.fs.quoracdn.net/main-qimg-1535fd9d2793c45bc8b4a73782e8b489-c)

+++

> Exemple:fitxer de 250 GB. Bytes? bits?

![Conversió bytes](img/conversio-byte.png)

---

Sistemes de representació de la informació numèrica
------------------------------------------

**Sistema de numeració** = símbols + normes per representar info numèrica.

+++

* Sistemes amb base, notació: *(base* .
  * decimal (10)
  * binari (2)
  * octal (8)
  * hexadecimal (16)
  * etc...
* Sistemes de numeració sense base:
  * romà (utilització més complicada).

+++

**Magnitud analògica** vs  **representació digital**.

> Exemple: velocitat vs. rellotge digital.

<img src="http://i2.wp.com/www.droneuplift.com/wp-content/uploads/2016/03/Analog-digi.png" height="400px">



+++

**Sistema digital**: dispositiu que manipula informació digital.

> Exemples: ordinadors, smartphones, etc...

+++

Sistemes de nombres:

* binari (base 2)
  * El més utilitzat pels ordinadors
* decimal (base 10)
  * El més utilitzat per les persones
* hexadecimal (base 16)
  * Molt útil per representar binari de forma compacta

---

Conversió entre sistemes de numeració
----------------------------------

* **Teorema fonamental de la numeració** (TFN).

> Exemple: 
> passar 4123(5 a base 10
>
> Solució: 4123(5 = 4 x 5³ + 1 x 5² + 2 x 5¹ + 3 x 5⁰ = 500 + 25 + 10 + 3 = 538(10

+++

* Regla de Ruffini
* Divisions successives per la base.
* Conversió directa utilitzant taula (binari-hexadecimal).

+++

```
0 0000        8 1000
1 0001        9 1001
2 0010        A 1010
3 0011        B 1011
4 0100        C 1100
5 0101        D 1101
6 0110        E 1110
7 0111        F 1111
```

Exemple: `A4(16 =  1010 0100(2`

---

Operacions bàsiques amb sistemes de numeració
---------------------------------------------

Es poden fer operacions (+ - * / ...) amb els diferents sistemes de numeració (binari, hexadecimal, etc...)

---

Representació dels nombres enters
---------------------------------

Mètodes destacats: 
-   Decimal empaquetat (més senzills per a les persones)
-   Mòdul i signe.
-   Complement a 1.
-   Complement a 2.
-   Excés a 2<sup>n</sup>–1. (simplifiquen operacions aritmètiques a l'ordinador)

+++

**Paraula** = nombre de bytes que pot gestionar l’ordinador

>   Exemple:
> * un ordinador amb paraula de 8 bits pot treballar amb 2⁸
    = 256 combinacions diferents
> * un ordinador de 32 bits amb 2³² =
    4.294.967.200.

---

Representació dels nombres amb xifres decimals
-----------------------------------

Mètodes principals:

-   En coma fixa.
-   En coma flotant.

---


Sistemes de representació de la informació alfanumèrica
----------------------------------------

L’ordinador només entén la informació en forma de senyals elèctrics que
nosaltres representem mitjançant dos símbols, el 0 i l’1. 

+++

En la transmissió de la informació hi ha un sistema de control d'errors:

>   Exemple: control de paritat parella.  El nombre total de bits 1 en cada byte ha de
        ser parell.

+++

![control de paritat](https://image.slidesharecdn.com/dcchapter-10-140704010417-phpapp02/95/error-detection-and-correction-21-638.jpg?cb=1404436011)

---

Codificació interna de les dades
------------------------------

Codis més utilitzats:
- **ASCII**. Clàssic. Cada caràcter 1 byte. Només lletres angleses.
- **Unicode**. Modern. Codi de 32 bits. Tots
    els idiomes, i emojis, símbols matemàtics, tècnics, musicals, etc...

+++

![ascii](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/USASCII_code_chart.png/361px-USASCII_code_chart.png)

+++

![unicode emoji](https://amp.businessinsider.com/images/567ea534e6183e26008b4f0e-750-405.png)