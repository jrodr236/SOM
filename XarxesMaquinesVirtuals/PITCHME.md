Configuració de la xarxa a les màquines virtuals
================================================

[Veure Teoria](https://jrodr236.github.io/SOM/XarxaMaquinesVirtualsVirtualBox.html)

---


Tipus
-----

- Bridged
- Nat
- Host-only
- Custom
- LAN segment

+++


### Bridged (Pont)

Màquina virtual connectada directament a la xarxa real.

![Bridged Networking](https://pubs.vmware.com/workstation-9/topic/com.vmware.ws.using.doc/GUID-8AB8E6E2-E16F-4E60-8421-669C96E6BF38-high.png)

+++

### NAT

Màquina virtual amb accés a la xarxa real, però no directament.

![NAT](https://pubs.vmware.com/workstation-9/topic/com.vmware.ws.using.doc/GUID-4C1FE8E1-9C52-4A43-9C36-97AEC38C737B-high.png)

+++

### Host-only (només host)

Xarxa privada

![Host-Only](https://pubs.vmware.com/workstation-9/topic/com.vmware.ws.using.doc/GUID-B8B0D851-3DF2-4999-AE86-9059AE017A9C-high.png)

+++

### Custom (personalitzat)

Avançada.

+++

### LAN Segment

Avançada.

+++

### Resum


&nbsp;|VM ↔ Host|VM1 ↔ VM2|VM → Internet|VM ← Internet
---------|:---------:|:-------------:|:-------------:|:-----:
Bridged|+|	+|	+|	+
NAT|	+|	+|	+|	Port forwarding
Host-only|+|+|–|–

+++

![Resum networking](https://img-16.ccm2.net/8emiYyGU-cMoBjDSxzM8hA0QZ0g=/ee98a57cbb9e4db08a5e4dbd86c078c6/ccm-faq/0-xOzTOwr6-untitled-s-.png)

---

Proxy institut
---------------------

**Automatic**: `http://192.168.0.244/proxy.inf.pac`