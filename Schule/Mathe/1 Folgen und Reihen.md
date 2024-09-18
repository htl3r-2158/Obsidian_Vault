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


>[!info] Zur Arithmetischen Folge
>beschreiben einen diskreten **Wachstums** und **Abnahmeprozess**
>Es ist daher meist von Vorteil die Zählung mit **$0$** zu **beginnen**
>
>Termdarstellung:
>$a_n = a_0 + n*d$ (Arithmetisch)
>$b_n = b_0 * q$ (Geometrisch)
>
>Rekursive Darstellung
>$a_n = a_1 + (n-1) * d$ (Arithmetisch)
>$b_n = b_1 * p^{n-1}$ (Geometrisch)
### Bsp.: 1 Zunahme
Der Verbrauch eines Rohstoffs **steigt** pro Jahr  **um $4\%$**. Wie würde sich eine Reduktion der Steigerungsrate auf $2\%$, auf die Zeit auswirken, in der sich der Verbrauch verdoppelt.

Verbrauch zu beginn … $v_0$  ($v_1$ → $1$ Jahr)   $q = 1,04$
$v_1 = v_ * q^1$
$v_n = v_0*q^n = 2*v_0 \ |: v_0$
$q^n = 2 \ | ln$
$ln(q^n) = ln(2)$
$n*ln(q) = ln(2) \ | : ln(q)$
$n = \frac{ln(2)}{ln(1,04)} = 17,67a$

### Bsp.:2 Abnahme
![[Drawing 2024-09-13 14.07.43.excalidraw]]
$y_0 = 8cm$ Anfangsamplitude
Jede Folgeamplitude ist um $10\%$ kleiner
1) berechne $y_8$
2) Wann erhalte ich $5\%$ von $y_0$

$y_1 = y_0 * q^n$
$y_8 = y_0 * q^n = 8cm * 0,9^8 = 3,44cm$
$y_0 * q^n = y_0 * 0,05 \ \| : y_0$
$0,9^n = 0,005$
$n = 28$

## Wiederholung Exponentielles Wachstum
#exponentielles-Wachstum

### Bsp. 1:
Ein Kapital von $10$€wird $3$ Jahre lang jährlich mit $4\%$ verzinst. Berechne das Kapital nach $3a$
→ gemoetrische Folge
	$b_n = b_1 * q^{n-1}$
	$b_n = b_0 * q^n$

$k_n = k_0 * 1,04^n = 100 * 1,04^3 = 112,486$€

### Bsp. 2:
Bestimme das $101$  Folgeglied der geometrischen Folge
$< 2, - \sqrt{2}, 1, - \frac{1}{\sqrt{2}}, ... >$

$q = \frac{a_2}{a_1} = \frac{-\sqrt{2}}{2} = - \frac{1}{\sqrt{2}}$
$a_n = a_1 * q^{n}$
$a_{101} = 2 * (-\frac{1}{\sqrt{2}})^{101-1} = 2 * (- \frac{1}{\sqrt{2}})^{100} = 2*(-\frac{1}{2^{\frac{1}{2}}})^{100} = \frac{1}{2^{49}} = 1,78 * 10^{15}$
### Bsp.: 2b
Geg.: $a_2 = 9$   $a_5 = \frac{1}{3}$

$a_n = a_1 * q^{n-1}$
$a_5 = a_2 * q^3 = 9 * q^3 = \frac{1}{3}$
$q = \sqrt[3]{\frac{1}{27}} = \frac{1}{3}$

## Summe einer arithmetischen oder geometrischen Folge

### 2.1: Die Summe $\Sigma$ einer arithmetischen Folge

Mathematisch formulieren: 
$s_n = 50* (1+100)$

>[!info] Summenformel einer arithmetischen Folge
$s_n = \frac{n}{2} * (a_1 + a_n)$

#### Bsp. 1:
Man berechne $s_{11}$ einer arithmetischen Folge wenn:
$a_1 = 9$ und $d = 5$ ist

$a_n = a_1 + (n-1) * d$ → $s_n$ einsetzen!

$s_{11} = \frac{11}{2} * (9 + 59) = 374$

>[!info] Summe einer Arithmetischen Folge
>$s_n = \frac{n}{2} * (2* a_1 + (n-1) * d)$

>[!note] Arithmetische Summenformel
Ist $a_1 + a_2 + ... + a_n$ eine arithmetische Reihe von $n$ Gliedern mit der Differenz $d$, so gilt für die Summe: 
>$s_u =\sum\limits_{i=1}^{n} a_i$

Eine Reihe stellt somit eine Folge von $n$ Partialsummen dar.

### 2.2 $\Sigma$ einer geometrischen Folge
$s_n = \sum\limits_{i=1}^{n} * b * i = b_1 + b_2 + ... + b_n = b_1 + q^2 + ... b_1 * q^{n-1}$

Ist $b_1+b_2 + ...$ eine geometrische Reihe von $n$ Gliedern mit dem Quotienten $q ≠1$, so gilt für die Summe $s_n$ ihrer Glieder.

$s_n = b_1 * (1+q+q^2+...+q^{n-1}) =$ 
>[!info] Geometrische Summenformel
>$s_n = b_1 \frac{q^{n-1}}{q-1}$
>Die Hochzahl $n$ von $q^n$ ist gleich der Anzahl der Folgeglieder

### Bsp. 1:
Eine geometrische Folge mit $b_1 = 3$ unddem Quotienten $q = 2$. Berechne die Summe der ersten $5$ Glieder
$s_n = 3 \frac{2^5 - 1}{2-1} = 3 * \frac{2^5-1}{1} = 93$

### Bsp. 2:
Geg.: Sind die ersten Glieder einer geometrischen Folge
$<8;\ 1.6;\ 0.32>$
Berechne: $s_7$

$q= \frac{b_2}{b_1} = \frac{1.6}{8} = \frac{1}{5} = 0.2$
$s_n = b_1 * \frac{q^{n-1}}{q-1} => s_7 = 9.999872$


### Bsp. 1.20:
#### a)
$s_n = \frac{15}{2} * (2* 4 + (15-1) * 3) = 375$
$a_n = 46$
#### b)
$a_n = a_1 + (n-1) * d$ Umformen
$a_1 =a_n -  (n-1)*d = 2$
$s_n = \frac{19}{2} * (2* 2 + (19-1) * 5) = 893$
#### c)
$a_n = a_1 + (n-1) * d$ Umformen
$d = \frac{a_n - a_1}{n-1} = 7$
$s_n = \frac{16}{2} * (2* 2 + (16-1) * 7) = 872$
