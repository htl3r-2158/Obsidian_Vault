1. Serverrollen:
	- Active Directory Domänendienste
2. Zu Domäncontroller heraufstufen (Oben rechts Info Kasterl)
	1. Hinzufügen (Wenn's schon einen gibt)
	2. Neue Domäne erstellen in einer vorhandenen Gesamtstruktur
	3. Neue Gesamtstruktur hinzufügen (Wenn's gar nix gibt)
		- Kennwort-Wiederhstellungsmodus ganz lang weil komplettes backup
		- Script anzeigen lassen (Für zum Beispiel core)
		- !!! IP-Adresse und Name müssen richtig sein !!! (sonst schwer zu ändern)

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
