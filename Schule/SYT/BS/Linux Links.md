#Soft-Link #Hard-Link #Linux-Zugriffsrechte #Linux

## soft link

```bash
Umleitung:   ln -s <target> <link>
Verknüpfung: ln -s /etc/passwd meinedatei
```

## hard link
link auf #Inode Tabelle
```bash
ln file2 testdatei
rm testdatei       #Hardlinks auf Inode Tabelle --
rm file2           #Hardlinks 0 -> Wirkliche löschung

id                 # Benutzer & Gruppen
stat               # Datei Info
```

