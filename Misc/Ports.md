## Vlan
sh vlan brief (access ports und zu welchem vlan sie assigned sind)
sh int trunk (trunk ports und wie sie konfiguriert sind)

switchport mode access vlan [vlan id]
swichport mode trunk
switchport trunk allowed vlan [vlan id],[vlan id],...
## DHCP
sh ip dhcp pools
ip dhcp pool [pool name]
default-gateway A.B.C.D
?

ip dhcp excluded address A.B.C.D
## RIP
sh ip Route
sh run (und dann bei rip nachschauen ob es konfiguriert ist oder nicht, wenn ja vielleicht auch falsch?)
router RIP
passive-interface [int name]
?

## NAT
### Interfaces
ip nat inside
ip nat outside
### Allgemein
ip nat inside source list 1 interface [outside interface] overload
access-list 1 permit A.B.C.D D.C.B.A
### Show
show ip nat translations 