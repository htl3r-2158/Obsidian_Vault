---
noteID: 6e0eb021-bc71-40f5-8503-dd2360f5f362
---
#Graphentheorie #NWT #Netzwerktechnik

## Anwendungen
- Netzwerkpläne
- Routenpläne
- Constructive Solid geometry
- Sichtbarkeit
- Grafikkarten
- ER-Modelle
- Petrinetze, neuronale Netze
- …

## Graphen
- lange vor Informatik bekannt
- durch Infromatik Problemfelderweiterung
	- Beispiel: travelling salesman
	- Ziel:
		- F1: existiert ein NP - vollständiger Algorithmus?
		- F2: wie sieht dieser Algorithmus aus?
		- F3: ist die Laufzeit akzeptabel?
### Definition
- Ein Graph besteht aus …
	- … (meist endlichen) Menge von Knoten $V$ (vertex)
	- … (meist endlichen) Menge von Kanten $E$ (Eges)
- ist $V$ endlich, heißt der Graph ==ENDLICH==
- Kantenmenge entspricht der Beziehung zwischen Knoten
	- daher meist nur eine Kante zugelassen
	- aber auch Mehrfachkanten möglich (-> Gewicht)
	- Problem: Eulerkreis
	- Kanten können auch gerichtet sein

#### Gerichteter Graph / Ungerichteter Graph
- gilt: $E \subseteq \ V * V$ ($E$ als Menge geordneter Paare) -> ==gerichteter Graph==
- gilt: $E$ ist Zweigermenge von Knoten -> ==ungerichteter Graph==

 - $G$ ist ein ungerichteter Graph
- Der $Grad$ ($degree$, $dev (v)$) eines Knotens $v$ ist die Zahl der Kanten in $g$, die $v$ enthalten
- Eine folge ($v_1,... v_k$) von paarweise verschiedenen Knoten heißt $Weg$ ($path$) in $G$ falls $v_1,...$
## Graphenrepräsentation im Computer
- Problem: Klassifizierung des Zeitbedarfs zu Lösung algorithmischer Probleme
	- Konstruktion von theoretische Maschinenmodelle, wie die Turing - MAschinen
	- $M$ eine solche Maschine
	- $w$ die Eingabe 
	- $time_M (w)$ die Zahl der Takte von $M$ auf $w$ bis zur Terminierung (bzw $\infty$, falls $M$ auf $w$ nicht terminiert). 
	- $t_M (n)$ die maximale Laufzeit der Maschine $M$ auf Eingaben der Länge $n$, 
		- $t_M (n):=max [time_M (w) : |w| = n]$
	- Ist $t_M (n)  \in O (n)$, so spricht man von ==Linearzeit==, ist $t_M (n) \in O (n^k)$, so spricht man von ==Polynomzeit==

### Binärbaum
#### Definition Binärbaum
- Elemente eines Binärbaums:
	- Knoten sind hierarchisch angeordnet
	- oberster Knoten: ==Wurzel==
	- jede innere Knoten hat genau zwei Nachfolger
	- Auf den untersten Ebenen stehen die Blätter

> Ein ==Baum== ist ein endlicher ungerichteter Graph, der zusammenhängend ist und keine Kreise enthält
