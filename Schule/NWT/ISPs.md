---
noteID: fe5e406a-b58b-49c0-a924-216e769bea8a
---
![[Drawing 2025-09-26 14.29.34.excalidraw | 500]]
Peering kann sich jeden Tag ändern. Jeden Tag neu verhandelt

AS … autonomes System (Ein Netzwerk das unter einer Administrative ist)

Konvergenz … alle Router haben die gleiche Routingtabelle

## ISP Beispiel
![[Drawing 2025-09-26 14.51.33.excalidraw | 500]]
GRE fügt Header hinzu und schickt von PE1 nach PE2 (Es steht nur PE2 GRE interface drinnen)

BGP (Boarder Gateway Protokoll)


## Grundconfig
```bash
ena
hostname []a
ip domain-name 4AX
no ip domain-lookup
username cisco algorithm-type scrypt secret cisco
username cisco privilege 15 # Rechte an user geben

service password encryption

# SSH
ip ssh version 2
crypto key generate rsa usage-keys modulus 1024

line con 0
logging local
logging sync
execution-timeout 0
exit

line vty 0 996
logging sync
execution-timeout 0
transport input telnet ssh
exit

motd #Hello#
```
## IGP & OSPF
höchste RID wird designated Router
```bash
#OSPF
router osp 1
network [a.b.c.d] [wildcard a.b.c.d] area [alles außer 0(Backbone)]
end

sh ip ospf neighbour
```
```bash
#GRE
int tunnel [tunnel number 1-...]
ip address [a.b.c.d]
tunnel source [interface und interface number (z.b. g0/1)]
tunnel destination [ip address des anderen tunnel endes]

# BGP
 #Loopback interfaces
int lo 1
ip address [a.b.c.d andere als ospf network] [subnetmask a.b.c.d]

router rip
version 2
network [network von loopack interface]

router bgp 100 (100=As-Nummer)
neighbor [a.b.c.d adresse des anderen bgp routers] remote-as 100 (As-Nummer)
network [a.b.c.d addresse] mask [Subnet mask]
```
