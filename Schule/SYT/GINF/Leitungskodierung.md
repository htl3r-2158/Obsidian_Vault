## Parallele vs. Serielle Datenübertragung

### Paralelle Übertragung
#Paralelle-Übertragung
* auf mehrern physischen Leitungen
* nebeneinander oder über mehrere Kanäle
* zur gleichen Zeit "im Gleichsschritt"
* eigen Leitung zur Snychronisation erforderlich (Taktsignal = Clock oder Strobe)
### Serielle Übertragung
#Serielle-Übertragung
- Datenübertragung auf 1 Leitung
- Bits nacheinander übertragen

# Leitungscodes
## Manchester Codierung
```10010110100 ... Datenstrom```
![[Pasted image 20240430130240.png]]
> Taktsignal  wird XOR-Verknüpft mit dem Datenstrom

> `0` = Steigende Flanke
> `1` = Fallende Flanke


### Nachteil
Signal ändert den Zustand innerhalb eines Bits
	$Signalrate = Datenrate * 2$ 

$Overhead = \frac{Signalrate}{Datenrate} -1$
#Overhead = Mehrarbeit

$Overhead \ Manchestercodierung = 100 \%$
### Anwendung
klassisches #Ethernet

## 4b/5b Codierung

| 4B-Wort | 5B-Wort | 4B-Wort | 5B-Wort |
| ------- | ------- | ------- | ------- |
| 0000    | 11110   | 1000    | 10010   |
| 0001    | 01001   | 1001    | 10011   |
| 0010    | 10100   | 1010    | 10110   |
| 0011    | 10101   | 1011    | 10111   |
| 0100    | 01010   | 1100    | 11010   |
| 0101    | 01011   | 1101    | 11011   |
| 0110    | 01110   | 1110    | 11100   |
| 0111    | 01111   | 1111    | 11101   |

### Bsp.:
> Eva schickt an Hugo den folgenden Datenstrom

`1011 1100 0000 0011`

> Wie sieht das 4B/5B-codierte Signal aus ?

`10111 11010 11110 10101`

$Overhead = \frac{20 Signalbits}{16 Datenbits} -1 = 25\%$

## Weiter Leitungscodes
### #8b/10b-Code
> übersetzt jeweils 8 bit Nutzdaten in 10 bit Signaldaten
>$Signalrate = 10 * 8 * Datenrate$
>$Overhead = 25\%$

#### Anwendung
* USB 3.0
* PCI-Express 1.x und 2.x
* HDMI bis 2.x
* Serial ATA

### #64b/66b-Code
* 64bit Nutzdaten -> 66bit Signaldaten
* $Signalrate = 66/64 * Datenrate$
* $Overhead = 3,125\%$
#### Anwendung
* 100-Gigabit-Ethernet

### #128b/130b-Code
* $Overhead = 1,6\%$
#### Anwendung
* PCIe 3.0 bis 5.0

# SATA-BUS
#SATA = Serial Advanced Technology Attachment

>[!info] SATA in Kürze
>  #8b/10b-Code ierung
>  Serielle Datenübertragung
>  Hot Pluggable
>  Punkt-zu-Punkt-Verbindung

| Offizielle Bezeichnung mit #Signalrate = Transferrate = Baudrate | Datenrate ("Durchsatz") MByte/s |
| ---------------------------------------------------------------- | ------------------------------- |
| Serial ATA 1,5 Gbit/s                                            | 150                             |
| Serial ATA 3,0 Gbit/s, SATA Revision 2.x                         | 300                             |
| Serial ATA 6,0 Gbit/s, SATA Revision 3.x                         | 600                             |
| SATA Express 8,0 Gbit/s (nutzt PCIe 3.x), SATA Revision 3.2      | Ca. 1000 (985)                  |
| SATA Express 16,0 Gbit/s (nutzt PCIe 4.0), SATA Rev. 3.2         | Ca. 2000 (1.969)                |

