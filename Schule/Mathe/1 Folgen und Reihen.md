#Folgen #Zahlenfolge

## Was ist eine Zahlenfolge (kurz Folge)?

> Eine fortlaufende endliche oder unendliche Anordnung von Zahlen

$<a_1, a_2,a_3, ..., a_n> bzw. <a_1, a_2, a_3, ... a_n, ...>$

Die einzelnen Zahlen werden #Glieder genannt mit dem Index $n$

Einfachste Zahlenfolge ist die **Zahlenfolge der Natürlichen Zahlen

$N^* = 1,2,3,4,5 ... n$
Die Folge beginnt mit 1.

Das #Bildungsgesetz ist ganz einfach: von Glied zu Glied kommt eins dazu.

Die Zahlenfolge lautet: $a_1 = 1, a_2 = 2, a_3= 3, ...$
Das allgemeine Glied heißt: $a_n = n$

### Weitere Bsp.:
* gerade Zahlen
	$2,4,6,8,...$ → $a_n = 2*n$
	$a_1, a_2, a_3,a_4,...$ 
- ungerade Zahlen
	$1,3,5,7,...$ → $a_n = 2*n -1$

## Eine Folge als Funktionalität
Die #Definitionsmenge $D$ ist im Falle einer **endlichen** Folge mit $m$ Gliedern die Menge ${1,2,3,...,m}$ 

## Arten des Bildungsgesetzes

### Explizite oder #Term-Darstellung
Term = allgemeines Glied einer Folge

> Angabe eines Terms (Formel), wie das Glied $a_n$ allgemein berechnet werden kann
### #Rekursive-Darstellung
>Angabe, wie das Glied $a_n$ aus dem vorhergehenden Folgeglied oder aus mehreren vorhergehenden Folgegliedern berechnet werden kann.

### Beispiele
1)  $c_n - \frac{n}{n+1}$
	Termdarstellung
2) $a_n = 2_n -1$
	Termdarstellung
3) $x_1 = 1, x_{n+1} = \frac{1}{2} * (x_n + \frac{3}{x_n})$
	-> rekursive Darstellung

### Arithmetische und Geometrische Folge
#Arithmetische-Folge kann als eine #lineare-Funktion, eine #geometrische-Folge kann als eine #Exponentialfunktion aufgefasst werden

|                       | Arithmetische Folge                                                                                                         | Geometrische Folge                                                                                 |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Termdarstellung       | $a_n = a_1 + (n-1) * d$                                                                                                     | $b_n = b_1 * q^{n-1}$                                                                              |
| Rekursive Darstellung | $a_{n+1} = a_n +d$                                                                                                          | $b_{n+1} = b_n * q^n$                                                                              |
|                       | Eine folge heißt arithmetisch, wenn die #Differenz zweier aufeinander folgener Glieder $a_{n+1}$ und $a_n$ **konstant** ist | Eine Folge heißt geometrisch, wenn der #Quotient zweier aufeinander folgender Glieder **konstant** |
|                       | <br>                                                                                                                        |                                                                                                    |
| Beispiele:            | $<2,5,8,11,14>$ -> #Differenz ist konstant $3$                                                                              | $<2,6,18,54,162>$     -> #Quotient ist konstant $3$                                                |
|                       | $<19, 17,15,13>$ -> #Differenz ist konstant $-2$                                                                            | $<128, 32, 8, 2>$ -> #Quotient ist konstant $\frac{1}{4}$                                          |

#### Beispiele: Stelle die Folgen al Term und rekursiv dar.

##### Bsp.: 1
$<5,7,9,11,13,15,17>;n ≤ 7$
#Term-Darstellung : $a_n = 5 + (n-1) * 2 = 3 + 2n$   $n = 1,2,...,7;$
#Rekursive-Darstellung : $a_{n+1} = a_n + 2 → a_1 = 5$    $n=1,2,...,7;$
##### Bsp.: 2
$<24,21,18,15,12,9>$
#Term-Darstellung : $a_n = 24 + (n-1) * 3 = 3*n + 21$ $n=1,2,...,6;$
#Rekursive-Darstellung : $a_{n+1} = a_n - 3 → a_1 = 24$   $n=1,2,...,6;$

##### Bsp.: 3 Arithmetische Folge
Geg.: $a_1 = 1$ #Differenz ist 0,8
Ges.: berechne die ersten $6$ Folgeglieder

$a_n = 1 + (n-1) * 0,8 → 0,2 + 0,8n$  

| Wertetabelle |       |
| ------------ | ----- |
| $1$          | $a_1$ |
| $1,8$        | $a_2$ |
| $2,6$        | $a_3$ |
| $3,4$        | $a_4$ |
| $4,2$        | $a_5$ |
| $5$          | $a_6$ |

##### Bsp.: 4 Geometrische Folge
Geg.: $b_1 = 2; q = 1,2$
Ges.: Berechne das $b_5$

$b_n = 2 * 1,2^{n-1}$

$b_5 = 4,1472$

##### Bsp.: 5
_Berechne die Glieder der geometrischen Folge_
Bestimme das $7.$ Glied einer geometrischen Folge mit $b_1 = 1000$ und $q = 0,2$

$b_n = 1000 * 0,2^{n-1}$
$b_7 = 1000 * 0,2^6 = 0,064$

##### Bsp.:6
1) $<6,18,54,62>$ 
	-> $b_n = 6 * 3^{n-1}$
	$b_{n+1} = b_n * 3$
1) $<4, 2, 1, \frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \frac{1}{16}>$
	-> $b_n = 4*(\frac{1}{2})^{n-1} = 2^{n-1}$
	$b_{n+1} = b_n * \frac{1}{2}$
	