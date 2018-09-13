# Configuració de la xarxa a les màquines virtuals

[//]: https://www.virtualbox.org/manual/ch06.html

* [Resum](https://gitpitch.com/jrodr236/som/master?p=XarxesMaquinesVirtuals)
* Exercicis teòrics: *moodle*
* [Exercicis pràctics](ExercicisXarxaMaquinesVirtuals.md)

[//]: https://pubs.vmware.com/workstation-9/index.jsp?topic=%2Fcom.vmware.ws.using.doc%2FGUID-BAFA66C3-81F0-4FCA-84C4-D9F7D258A60A.html

VMWare Workstation permet escollir els següents tipus d'adaptadors de xarxa:

- Bridged
- Nat
- Host-only
- Custom
- LAN segment

Bridged (Pont)
-------
La màquina virtual es connecta a la xarxa utilitzant l'adaptador de xarxa del sistema host, intercanviant paquets amb la xarxa real directament. La màquina virtual té una identitat única a la xarxa, separada i no relacionada amb el sistema host.

![Bridged Networking](https://pubs.vmware.com/workstation-9/topic/com.vmware.ws.using.doc/GUID-8AB8E6E2-E16F-4E60-8421-669C96E6BF38-high.png)

És útil per instal·lar sistemes que han de ser visibles per les màquines que estan connectades a la xarxa real.

NAT
----
Aquest mode funciona de manera similar a un *router* domèstic, agrupant els sistemes que l'utilitzen en una xarxa i evitant que els sistemes fora d'aquesta xarxa accedeixin directament als sistemes dins d'ell, però deixant que els sistemes interconnectin entre si.

![NAT](https://pubs.vmware.com/workstation-9/topic/com.vmware.ws.using.doc/GUID-4C1FE8E1-9C52-4A43-9C36-97AEC38C737B-high.png)

És útil per tenir sistemes amb connexió a la xarxa, però que no siguin visibles per les màquines de la xarxa real.

Host-only (només host)
--------
Els adaptadors de xarxa virtual de la màquina virtual i del hoste estan connectades a una xarxa Ethernet privada. Aquesta xarxa està completament contenida dins el sistema hoste.

![Host-Only](https://pubs.vmware.com/workstation-9/topic/com.vmware.ws.using.doc/GUID-B8B0D851-3DF2-4999-AE86-9059AE017A9C-high.png)

És útil per tenir sistemes aïllats, sense connexió a la xarxa real.

Custom (personalitzat)
------
Permet escollir configuracions de xarxa personalitzades.

Encara que VMnet0, VMnet1, i VMnet8 son accessibles a la llista, aquestes xarxes usualment s'utilitzen per les xarxes bridged, host-only, i NAT.


LAN Segment
-----------
És una xarxa privada que es comparteix amb altres màquines virtuals.

Pot ser útil per proves _multitier_, anàlisi de rendiment de la xarxa, i situacions a on l'aïllament de la màquina virtual és important.


Resum
-----

&nbsp;|VM ↔ Host|VM1 ↔ VM2|VM → Internet|VM ← Internet
---------|:---------:|:-------------:|:-------------:|:-----:
Bridged|+|	+|	+|	+
NAT|	+|	+|	+|	Port forwarding
Host-only|+|+|–|–

![Resum networking](https://img-16.ccm2.net/8emiYyGU-cMoBjDSxzM8hA0QZ0g=/ee98a57cbb9e4db08a5e4dbd86c078c6/ccm-faq/0-xOzTOwr6-untitled-s-.png)


