Codificació de la informació - Exercicis pràctics
=================================================

Exercici de grup
----------------

> Segueix les instruccions del professor per fer les següents pràctiques:

1. Codifica una pregunta sobre informàtica en codi ASCII. Escriu-la en un paper indicant el teu nom i cognoms.

2. Decodifica la pregunta codificada en ASCII que el professor et farà arribar. Contesta-la al paper, indicant també el teu nom i cognoms.


Exercicis de base
-----------------

> Aquestes pràctiques es corregiran a classe. Cada pràctica l'explicarà un/a alumne/a escollit aleatòriament.

1. Calcula el nombre de kB, GB i PB que corresponen a 234.987.000 bits.
   * kB són kiloBytes o kilobits?

2. Tenim un fitxer que ocupa just la meitat d'un disc de Blu-Ray. Volem fer-ne una còpia però no ens queda cap més disc Blu-Ray. Calcula quants discos DVD necessitaríem si podem fer trossos del fitxer de la mateixa mida. Fes el càlcul també amb CDs.
   * Capacitats: Blu-Ray 25GB; DVD 4,7GB; CDs 700MB.

3. Tenim una connexió de fibra òptica de 5 Gigues. Tenint en compte que aquesta és la velocitat màxima teòrica (5 Giga**bits**), fes els càlculs per saber:
   * Quant de temps, com a mínim, trigarà en baixar-se un fitxer de 5 Gigabits?
   * Quant de temps, com a mínim, trigarà en baixar-se un fitxer de 5 GigaBytes?
   * Quant de temps, com a mínim, trigarà en baixar-se un fitxer de 18 GigaBytes?
   * Quant de temps, com a mínim, trigarà en baixar-se un fitxer de 512 MegaBytes?

4. Omple la següent taula de conversions:

   | Decimal | Hexadecimal | Binari |
   |:-------:|:-----------:|:------:|
   |0|0|0000|
   |1|1|0001|
   |2
   |3|3| |
   |4| |
   | |5
   | | 6
   |7
   |8
   | |9
   |10
   | |B
   |12
   |13
   | |E
   | | |1111

5. Sense utilitzar calculadora ni cap eina per ajudar-te, converteix el número hexadecimal F87A02 a binari. Explica pas a pas com ho has fet.

6. Sense utilitzar calculadora ni cap eina per ajudar-te, converteix el número binari 1111001 a hexadecimal. Explica pas a pas com ho has fet.

7. Utilitzant una calculadora, converteix els números decimals 255 i 256 a hexadecimal i a binari.

8. Quina és la mida de paraula dels següents sistemes?
   - Nintendo NES
   - Intel 80386 (i386)
   - Intel Core i7

8. Quin és el número més gran que es pot emmagatzemar utilitzant la mida de paraula dels sistemes de l'exercici anterior? Indica els números en binari, en hexadecimal i en decimal.

9. Els següents son exemples de detecció d'errors "Two-dimensional parity-check code", com els vists a classe. Indica si tenen o no errors, i on són: 
   ```
   a)
   0 0 1 0 1 0 1 | 1
   1 0 1 1 0 1 0 | 0
   0 0 0 1 1 0 0 | 0
   1 1 1 1 0 1 1 | 0
   1 1 1 1 0 1 1 | 0
   0 0 0 1 0 0 1 | 0
   0 0 0 1 1 1 1 | 0
   --------------+--
   1 0 0 0 1 0 1 | 1


   b)
   0 0 1 0 1 0 1 | 1
   1 0 1 1 0 1 0 | 0
   0 0 0 1 1 0 0 | 0
   1 1 1 0 0 1 1 | 0
   1 1 1 1 0 1 1 | 0
   0 0 0 1 0 0 1 | 0
   0 0 0 1 1 1 1 | 0
   --------------+--
   1 0 0 0 1 0 1 | 1

   c)
   0 0 1 0 1 0 1 | 1
   1 0 1 1 0 1 0 | 0
   0 0 0 1 1 0 0 | 0
   1 1 1 1 0 1 1 | 0
   1 1 1 1 0 1 1 | 0
   0 0 0 1 0 0 1 | 0
   0 0 0 1 1 1 1 | 0
   --------------+--
   1 0 0 0 1 0 1 | 0
   ```

10. Intenta escriure un caràcter UNICODE a l'editor de textos *notepad* de Windows. Per exemple, aquest: https://emojipedia.org/penguin/
   Es pot escriure? Creus que té suport de UNICODE? Creus que té suport per ASCII?

11. A l'editor de textos *gedit*, intenta escriure un caràcter UNICODE. Funciona? Perquè?

Grimpades
----------
>Les següents pràctiques son especialment difícils. La correcció a classe serà voluntària, però seran avaluades quan es lliurin al moodle.

1. Explica els càlculs que realitza un sistema informàtic per sumar els següents números en decimal: 63 + 19, començant passant els números a binari.

2. Com s'emmagatzema el número 0,000000000000000000000000000038746 utilitzant una codificació del tipus coma flotant?