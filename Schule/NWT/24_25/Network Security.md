---
noteID: 4d2616e3-9146-496c-be35-0d0902b9e59c
---
![[Drawing 2025-01-13 13.44.22.excalidraw|1000]]

## LAN Security

| Bedrohung                 | Maßnahmen                                                                      |
| ------------------------- | ------------------------------------------------------------------------------ |
| MAC Address Table Attacks | Port Security                                                                  |
| Vlan Hopping Attack       | DTP disabling, shutdown unused ports, explicit access ports, native vlan shift |
| DHCP Spoofing Attack      | DHCP Snooping                                                                  |
| DHCP Starvation Attack    | Port Security                                                                  |
| ARP Attack                | Dynamic ARP Inspection                                                         |
| STP Attack                | Portfast, BPDU Guard                                                           |
| Unauthorized Access       | SSH / local user-database                                                      |


### SSH Konfiguration
```bash
R1(config): ip domain name example.com
R1(config): crypto key generate rsa general-keys modulus 2048
R1(config): username Admin secret Str0ng3rPa55w0rd
R1(config): username Admin privilege 15
R1(config): ip ssh version 2
R1(config): line vty 0 4
R1(config-line): transport input ssh
R1(config-line): login local
```

## Port Security
>  Port Security ist für Switches
>  Auf einem Port darf sich nur jemand mit einer bestimmten MAC-Adresse anmelden sonst wird sofort ausgesperrt

#### Arten
1. **Sticky**: Erster der sich anmeldet ist registriert
2. **Manuell**
#### Violation Modes
- 