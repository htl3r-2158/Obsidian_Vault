## Lauflängencodierung + Codebaum

Erkennung von häufigen Folgen und dadurch eine Erstellung eines Codebaums nach einem Mobile Prinzip

![[Drawing 2024-02-15 15.39.10.excalidraw]]
![[Drawing 2024-02-15 15.56.06.excalidraw]]
## Verlustbehaftete Kompression (lossy compression)

Teil der Information geht verloren
	decodierte Daten unterscheiden sich vom Original
kann toleriert werden, wenn nicht relevante Information entfernt wird
nutzt die nicht perfekte menschliche Wahrnehmung:
	Ohren hören unterschiedliche Frequenzen verschieden gut
	leise Geräusche werden von lauten überlagert
	Auge ist für manche Farbtöne mehr empfindlich
	Grautöne detaillierter als Farbtöne
### JPEG
#JPEG
>[!note] Was ist JPEG
>Joint Photographic Expert Group: Expertengruppe die maßgeblich in der digitalen Fotoverarbeitungen beteiligt war

Fügt benachbarte Pixel in Blöcke zusammen und findet die am häufigsten vorkommende Farbe. Stärkere Komprimierung -> Stärkere Verpixelung

## MP3
#MP3
>[!note] Was ist MP3
>Abk.: MPEG-1 Audio Layer 3
>gehört der Famileie der Motion Picture Expert Group (MPEG)

Audiokodierung -> Musik-Datei wird komprimiert
Sehr starke Kompression bei nur geringfügigem Verlust

ca. 10% der Original Datei

Psychoakustische Effekte:
	2 Töne kann man erst sehr spät unterschieden
	Vor und nach sehr lauten Geräuschen kann man für kurze Zeit leisere Geräusche schlechter oder gar nicht wahrnehmen
	
**NUR** Signalanteile speichern, die ein Mensch wirklich hören kann
#Kompressionsrate wird in KBit/s angegeben. Höher -> bessere Qualität. An 196 KBit/s hört man fast keinen Unterschied

## 1 aus n Code = One-Hot-Code
stellt Zahlen binär dar

dezimale Ziffer -> #1-aus-n-Codierung:
	durch n Bits darstellen_ jeweils nur ein Bit auf 1 gesetzt ist, restliche n-1 Bits sind 0.
	
Beispiel für #1-aus-n-Codierung 

| Dezimal | #1-aus-n-Codierung |
|-|-|
| 0 | 0000000001 |
| 0 | 0000000010 |
| 0 | 0000000100 |
| 0 | 0000001000 |
| 0 | 0000010000 |
| 0 | 0000100000 |
| 0 | 0001000000 |
| 0 | 0010000000 |
| 0 | 0100000000 |
| 0 | 1000000000 |



## K-aus-n-Code
verwendet Teilmenge eines Binärcodes mit n Stellen = n Bit
Jedes Codewort hat an genau k Stellen den Wert 1

| Dezimal | #2-aus-5-Codierung |
| ---- | ---- |
| 0 | 00011 |
| 1 | 00101 |
| 2 | 01001 |
| 3 | 10001 |
| 4 | 00110 |
| 5 | 01010 |
| 6 | 10010 |
| 7 | 01100 |
| 8 | 10100 |
| 9 | 11000 |
2 aus 5 --> $\frac{5*(5-1)}{2}$
$\binom{2}{5}$
## Hammingdistanz
#Hammingdistanz zweier #Codewörter:
	Maß für die Unterschiedlichkeit von Codewörtern
	Anzahl der unterschiedlicher Stellen zwischen 2 #Codewörter 
Hammingdistanz eines Codes:
	Minimum der paarweisen Hammingdistanzen aller Codewörter
## Übertragungsfehler erkennen / korrigieren
**erkennbar** wenn ein ungültiges Codewort entsteht
**korrigierbar** wenn nur ein Bit sich verschoben hat

>[!error] Fehlererkennung
>Um Störungen an x Bits zu **erkennen** benötigt man Codes mit Hammingdistanz $≥ x + 1$

>[!success] Fehlerkorrektur
>Um Störungen an k Bits zu **korrigieren** benötigt man Codes mit Hammingdistanz $≥ 2k + 1$

>[!help] Wie erzeugt man fehlererkennenden / -korrigierenden Code
> #Redundanz hinzufügen
>	Gibt an, wie viel Information im  mittel pro Zeichen in einer Nachricht mehrfach vorhanden ist.
>	Redundanz kann für Fehlertoleranz sorgen
> #Deduplikation = Identifizieren und und Entfernen von Redundanz

### Anwendung Redundanz
#### DVD
87% sind Nutzdaten
13% Redundanz
Redundanz für Kratzer oder Staubkorn
Bei zu starker Abweichung funktioniert die Fehlerkorrektur nicht mehr

### Eindimensionale Parität (Parity)
#Parity-Bit hinzufügen = #Querparität = #Vertical-Redundancy
	aus einem nicht-fehlertoleranten Code --> 1-bit 
	fehl==erkennend==en Code
* Die "Parität" bezeichnet die Anzahl mit 1 belegten Bits im gesamten Informationswort (incl. #Parity-Bit)
* **gerade Parität** ( #even-parity): Gesamtanzahl der belegten Bits ist gerade 
* **ungerade Parität** ( #odd-parity): Gesamtanzahl der Bits ist ungerade
![[Drawing 2024-02-22 15.37.20.excalidraw | 1000]]
### Fehlerkorrigierenden Codes
#### Blockkodierung = 2-dimensionale Parität
![[IMG_4080 2.jpg | 00]]

| Anzahl Fehler | erkennen | korrigierbar |
| ---- | ---- | ---- |
| 1 | ✓ | ✓ |
| 2 | ✓ | ✕ |
| 3 | ✓ | ✕ |
| 4 | ✕ | ✕ |
| ... | ... | ... |
