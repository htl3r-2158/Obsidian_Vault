---
noteID: 2bfa57f4-2415-4f42-81b1-a22b6beff223
---
1. Serverrollen:
	- Active Directory Domänendienste
2. Zu Domäncontroller heraufstufen (Oben rechts Info Kasterl)
	1. Hinzufügen (Wenn's schon einen gibt)
	2. Neue Domäne erstellen in einer vorhandenen Gesamtstruktur
	3. Neue Gesamtstruktur hinzufügen (Wenn's gar nix gibt)
		- Kennwort-Wiederhstellungsmodus ganz lang weil komplettes backup
		- Script anzeigen lassen (Für zum Beispiel core)
		- !!! IP-Adresse und Name müssen richtig sein !!! (sonst schwer zu ändern)
3. DHCP Server einrichten (Ich glaub auch wieder oben rechts)
	1. Präfix
	2. Ausschlüsse (Excluded Addresses)
	3. Lease Dauer
	4. DNS (Unter DHCP server wahl unter bereich)
		1. DNS Server eingeben

```bash
# Logs anzeigen Linux
tail -50 /var/log/messages

# Ip helper adress auf Linux
dnf install dhcrelay -y

sudo cp /usr/lib/systemd/system/dhcrelay.service /etc/systemd/system/dhcrelay.service
sudo nano 


[Service]
Type=notify
ExecStart=/urs/sbin/dhcrelay -d -6 -l ens224 -u 256
StandardError=null

sudo systemctl daemon-reload
systemctl enable dhcrelay
sudo systemctl restart dhcrelay
```

## Core server
```bash

```