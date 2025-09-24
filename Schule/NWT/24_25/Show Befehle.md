---
noteID: 395fb83f-9897-4847-b5f8-006bf35609b2
---
## Access Layer (Access Switches)
```bash
sh ip int brief
sh vlan brief
sh int trunk
sh spanning-tree
sh port-security
sh port-security int [int]
sh port-security address
sh etherchannel summary
sh etherchannel portchannel
```

## Distribution Layer (Core1 und Core 2)
### DHCP
```bash
sh ip dhcp pool     # Konfiguration wie sh run | section dhcp
sh ip dhcp binding  # Vergebene DHCP-IPs
```
### Routing
```bash
sh ip route
sh ip protocols
```
### HRSP
```bash
sh stanby
debug standby
```
## Firewall
### NAT
```bash
sh ip nat translations
debug ip nat
```
### RIP
```bash
debug ip rip
```
### ACL
```bash
sh access-list
clear access-list counters  # Löscht alle matches
```
## Application Layer (Überall)
```bash
sh ssh
```
## Debug
```bash
u all  # Debug von allem ausschalten
```