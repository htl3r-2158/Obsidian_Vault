## Speicher Eigenschaften
* #Speichergröße (Preis pro Byte)
* #Zugriffszeit = #Latenzzeit
* #Volatil / #Persistent
* #Register
* #Cache-Speicher
* #Arbeitsspeicher
* #Laufwerke 

## Raid
#RAID

>Organisation mehrere physikalischer Festplatten eines Computers zu einem logischen Laufwerk

### Ziel
* größere Speicherkapazität, höhere Datensicherheit bei Ausfall einzelner Festplatten, größerer Datendurchsatz
RAID-Systemen erzeugen gezielt redundante Informationen --> Ausfall behält trotzdem die Funktionalität
### Vorteile
* Redundanz (Ausfallsicherheit)
* Performance (Transferraten)
* Aufbau großer logischer Laufwerke
* Austausch von Festplatten und Erhöhung der Speicherkapazität während des Systembetriebes
* Kostenreduktion
* Systemleistungsfähigkeit
*  **Achtung: RAID ersetzt KEINE Datensicherungen**
## RAID 0
#Stripping - Beschleunigung ohne Redundanz
* R. besteht aus mind. 2 Festplatten
* Ziel: gesteigerte Transferraten
* Festplatten werden in zusammenhängende Blöcke gleicher Größe augeteilt
* Bläcke werden zu einer großen Festplatten angeordnet

## Raid 5
* gesteigerter Datendurchsatz beim Lesen von Daten
* Redundanz bei geringen Kosten
	* weit verbreitet
	* Redundanz-Information zu Wiederherstellung
	* Über die Stripes der Platten wird ein Stripe mit Paritätsinformationen gebildet
	* Paritätsinformationen werden nach Round-Robin verteilt
	* Fällt nur eine Platte aus, kann aus den Paritätsinfos der Inhalt des ausgefallenen Stripes wiederhergestellt werden
	* Gesamtkapazität bei $n$ Platten: $(n-1) * Plattengröße$
>[!fail] Nachteil -- schlechte Performance
>Bei Änderung eines Sektors müssen zur neuen Paritätsberechnung alle Stripes gelesen werden
## RAID 6
Block-Level Striping mit doppelt verteilter Paritätsinformation


## Aufbau Magnetplatte
#Magnetplatte ist eingeteilt in:
* tausende konzentrische Kreise #Spuren ( #tracks)
* Spuren in Sektoren zu je `512 Byte` (neuerdings `4096 Byte` = AFD)
* #Sektor kleinste adressierbare Einheit auf einer #Festplatte
* Formatieren erzeugt ein Dateisystem auf einem Speichermedium
* #Cluster (Windows)  = #Blöcke (Linux) = kleinste adressierbare Einheit eines Dateisystems. Mehrere Sektoren sind ein Cluster
* #Zylinder = übereinander liegenden, identischen Spuren einer Festplatte
	* auf daten im Zylinder kann ohne Bewegung des Schreib-Lesekopfes gleichzeitig zugegriffen werden.
	* 



## Datenträger in Linux

### Partitionen anzeigen
>am Beispiel von meiner Ubuntu WSL
```bash
laurin@LaurinsStudio:~$ lsblk
NAME MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
sda    8:0    0 389.8M  1 disk
sdb    8:16   0     4G  0 disk [SWAP]
sdc    8:32   0     1T  0 disk /snap
                               /mnt/wslg/distro
                               /
```
#### UUID aller Partitionen ausgeben
```bash
laurin@LaurinsStudio:~$ blkid
/dev/sdb: UUID="ae47a2c6-a5c1-4c6a-a47a-a343d327c1ee" TYPE="swap"
/dev/sdc: UUID="f7027570-9a1a-4a76-8f41-7a47b2ed28c8" BLOCK_SIZE="4096" TYPE="ext4"
/dev/sda: BLOCK_SIZE="4096" TYPE="ext4"
```
#### Belegung der montierten Partitionen anzeigen
```bash
laurin@LaurinsStudio:~$ df -h
Filesystem      Size  Used Avail Use% Mounted on
none            7.8G  4.0K  7.8G   1% /mnt/wsl
none            953G  701G  253G  74% /usr/lib/wsl/drivers
/dev/sdc       1007G  2.6G  954G   1% /
none            7.8G   88K  7.8G   1% /mnt/wslg
none            7.8G     0  7.8G   0% /usr/lib/wsl/lib
rootfs          7.8G  2.1M  7.8G   1% /init
none            7.8G  848K  7.8G   1% /run
none            7.8G     0  7.8G   0% /run/lock
none            7.8G     0  7.8G   0% /run/shm
tmpfs           4.0M     0  4.0M   0% /sys/fs/cgroup
none            7.8G   76K  7.8G   1% /mnt/wslg/versions.txt
none            7.8G   76K  7.8G   1% /mnt/wslg/doc
C:\             953G  701G  253G  74% /mnt/c
snapfuse        128K  128K     0 100% /snap/bare/5
snapfuse         75M   75M     0 100% /snap/core22/1122
snapfuse         75M   75M     0 100% /snap/core22/1033
snapfuse         92M   92M     0 100% /snap/gtk-common-themes/1535
snapfuse         13M   13M     0 100% /snap/nmap/3226
snapfuse         13M   13M     0 100% /snap/nmap/3262
snapfuse         41M   41M     0 100% /snap/snapd/20671
snapfuse         40M   40M     0 100% /snap/snapd/21184
snapfuse        131M  131M     0 100% /snap/ubuntu-desktop-installer/1284
snapfuse        132M  132M     0 100% /snap/ubuntu-desktop-installer/1286
```
#### Alle Partitionen anzeigen
```bash
laurin@LaurinsStudio:~$ parted -l
Model: Msft Virtual Disk (scsi)
Disk /dev/sda: 409MB
Sector size (logical/physical): 512B/512B
Partition Table: loop
Disk Flags:

Number  Start  End    Size   File system  Flags
 1      0.00B  409MB  409MB  ext2


Model: Msft Virtual Disk (scsi)
Disk /dev/sdb: 4295MB
Sector size (logical/physical): 512B/4096B
Partition Table: loop
Disk Flags:

Number  Start  End     Size    File system     Flags
 1      0.00B  4295MB  4295MB  linux-swap(v1)


Model: Msft Virtual Disk (scsi)
Disk /dev/sdc: 1100GB
Sector size (logical/physical): 512B/4096B
Partition Table: loop
Disk Flags:

Number  Start  End     Size    File system  Flags
 1      0.00B  1100GB  1100GB  ext4
```

### Montieren in Linux
#### Manuelles Montieren
```bash
laurin@LaurinsStudio:~$ mount [-t file-system-type] device target-directory
```

### Master Boot Record (MBR) Partionierung
#MBR
> maximale Partitionsgröße: 2TiB; maximale Datenträgergröße: 4TiB
> 512 Byte groß

#### GPT-Datenträger (Windows)
#GPT 
>Hat einen Schutz-MBR damit das Betriebssystem das vermeintlich unnütze Dateisystem löscht


## SSD
### NVME
#NVME = Nonvolatile Memory Express
* Speicherzugriffs- und Transportprotokoll für Flash- SSD-Laufwerke
* für parallele Zugriffe
* Vorteil bei Servern: Auf die SSDs kann von mehreren Prozessor-Kerne zugriffen werden

### TRIM

>Löscht man eine Datei, dann löscht das BS auf Magnetfesplatte nur einen Eintrag in der FAT bzw. MFT. Die Datencluster auf der Festplatte werden aber normalerweise nicht geändert (sondern einfach irgendwann wieder überschrieben)