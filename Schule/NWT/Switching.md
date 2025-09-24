---
noteID: 8236aaba-abd7-4c4e-a255-ffdfab7584f6
---
## Spanning Tree Protocol
Versionen
- Plain
	- älteste
- rapid
	- wie plain aber schneller durch Optimierung
- PVST (Per Vlan STP)
	- STP pro Vlan nicht nur pro Switch
- PVST+ (Rapid-Per-Vlan-STP)
	- wie PVST, nur schneller durch Optimierung
- Multiple STP
	- eher unbekannt
### Funktionsweise

- Spannbaum erzeugen indem eine Wurzel bestimmt wird
- Kürzester Pfad zur Rootbridge finden

### Auswahl der Rootbridge
> Switch mit der niedrigsten Priorität wird Rootbridge

> Gleiche Priorität -> niedrigste MAC-Adresse
### Port
- Root
- designated
- blocked

### Kürzester Weg zur Bridge
> bestimmt durch Path-kosten

| Speed      | Cost |
| ---------- | ---- |
| 10 Gbit/s  | 2    |
| 1 Gbit/s   | 4    |
| 100 Mbit/s | 19   |
| 10 Mbit/s  | 100  |

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.9.23 - 8.21am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
### Root-Bridge Election
> Root-Bridge wird durch Bridge-ID (BID) bestimmt

#### Bridge-ID
- Priorität = 32768
- Extended System-ID = Vlan ID
- MAC-Adresse

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.9.23 - 8.25am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
### Portfast

| State     | Beschreibung                                                                     |
| --------- | -------------------------------------------------------------------------------- |
| Disabled  | Administrativ down                                                               |
| Blocking  | empfängt BPDUs, sendet keine, keine MAC-Lernphase                                |
| Listening | empfängt und sendet BPDUs, keine MAC-Lernphase                                   |
| Learning  | empfängt und sendet BPDUs, lernt MAC-Adressen, keine Weiterleitung von Nutzdaten |
| Forward   | empfängt und sendet BPDUs, lernt MAC-Adressen, leitet Nutzdaten weiter           |

### Gezielte Protzuordnung
#### Rootport g0/25
```bash
#Kosten hoch halten
interface G0/24
spanning-tree vlan 77 cost 2000
int g0/26
spanning-tree vlan 77 cost 3000

#Kosten niedrig g0/25 halten
int g0/25
spanning-tree vlan 77 cost 1000
```

### Beispiel Root-Switch-Wahl und Portrollen bestimmen
![|700](Schule/Images/IMG_1424.jpg)
1. Rootbridge
	- niedrigste Priority gewinnt
		- S1
2. Root-Port Bestimmung
	- Weg mit den niedrigsten Pfadkosten zur Root-B gewinnt
		- S1: kein port
		- S2:
3. Designated Port-Bestimmung
4. Blocked Port-Bestimmung

![](Schule/Images/IMG_1425.jpg)
