#DHCP … Dynamic Host Configuration Protocoll
- vergibt einem Client ohne TCP/IP - Konfiguration alle nötigen Infos
	- IP-Adresse + Subnetmask
	- Gateway
	- DNS-Server
	- Erweitert:
		- Timeserver
		- …
```mermaid
graph TD
Client[Client sucht DHCP] -->|DHCPDISCOVER| DHCP-Server1 & DHCP-Server2
DHCP-Server1 & DHCP-Server2 -->|DHCPOFFER| Client2[Client sammelt die
Angebote der DHCP-Server]
Client2 -->|DHCPREQUEST| DHCP-Server1 & DHCP-Server2
DHCP-Server1 -->|DHCPACK| Client3[Client Bekommt
die Grundkonfiguration]
```

