[[DHCP]]
#DHCP
_Beispiel anhand der Aufgabe vom 25.1.24_
#DHCP-Server-Konfiguration
```CLI
R1(config)# ip dhcp pool LAN1
R1(dhcp-config)# network 172.16.0.0 255.255.255.0
R1(dhcp-config)# default-router 172.16.0.254
R1(dhcp-config)# dns-server 1.2.3.2
R1(dhcp-config)# lease 1 1 1
R1(config)# ip dhcp excluded-address 172.16.0.254
R1(config)# service dhcp
R1(config)# (DHCP läuft und läuft ...)
R1# show ip dhcp ?
  binding  DHCP address bindings
  conflict DHCP address conflicts
  pool     DHCP address conflicts
  relay    Misceallaneous DHCP rely information
R1(config)# ip dhcp pool LAN2
R1(dhcp-config)# network 192.168.1.0 255.255.255.0
R1(dhcp-config)# default-router 192.168.1.254
R1(dhcp-config)# dns-server 1.2.3.2
R1(config)# ip dhcp excluded-address 192.168.1

... Wechsel zu GW ...

GW(config)# int gig 0/1
GW(config-if)# ip helper-address 10.1.1.2
GW(config-if)# exit
GW(config)#
```
`network` … Das Netzwerk für den DHCP-Server
`default-router` … Der Standard-Gateway
`dns-server` … DNS-Server (Kann auch außerhalb des Netzwerkes sein)
`lease D H M` … Die Zeit für die die IP-Adresse "geliehen" wird
