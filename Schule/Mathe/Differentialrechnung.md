_Infinitesimalrechnung_

>[!info]
>Von Gottfried Wilhelm Leibnitz und Newton unabhängig von einander entdeckt

## Änderungsmaße einer Funktion

$y = f(x)$ im Intervall $[a,b]$

1. Absolute Änderung: $f(b) - f(a)$
2. Relative Änderung: $\frac{f(b) - f(a)}{f(a)}$
3. Differenzenquotient oder mittlere Änderungsrate: $\frac{\Delta y}{\Delta x}$

## Tangentenproblem

![[Drawing 2024-11-13 08.33.16.excalidraw | 1000]]

> Differenzieren bedeutet den Grenzwert einer Funktion des #Differenzquotient en zu bilden

>[!important] Differentialquotient
$f'(x_0) = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}$ oder $f'(x_0) = \lim_{\Delta \to 0} \frac{\Delta y}{\Delta x}$
>
oder
>
$f'(x) = lim \frac{f(x) - f(x_0)}{x-x_0}$



### Beispiel
Berechne die Ableitung der Funktion $f$ mit $y = f(x) = -x^2 + 4x$ an der Stelle $x_0 = 1$

**a)** ![[Drawing 2024-11-13 08.50.48.excalidraw | 1000]] **b)** Ermittle die Gleichung der Tangente an der Stelle $x_0 = 1$ und berechne den **Steigungswinkel**
![[Drawing 2024-11-13 09.05.38.excalidraw  | 1000]]
```functionplot
---
title: f(x) = -x^2 + 4x
xLabel: x
yLabel: y
bounds: [0,4,0,4]
disableZoom: true
grid: true
---
f(x) = -x^2 + 4x
```
## Merkregel
1. Addiere $\Delta x (\Delta x \neq 0 )$  zu $x_0$
3. Berechne nun die Differenz $f(x_0 + \Delta x) - f(x_0)$

## Beispiele
3.10
![[Drawing 2024-11-13 09.30.07.excalidraw | 1000]]
## HÜ:
3.10 b-f

>[!note] Merksatz
>Eine Funktion die an einer Stelle stetig ist muss nicht differenzierbar sein

## 3.13
$t = 0 \ H = 2m \ v_0 = 20ms^{-1}$
$k(t) = H + v_0 * t + \frac{g*t^2}{2}$
$\Delta t = 0,5s; 0,1s; 0,01s$
![[Drawing 2024-11-20 08.39.50.excalidraw]]

## 3.14
$t = 0$ $s(t) = 260 * ln [cosh(0,2t)])$
$cosh = \frac{e^x + e^{-x}}{2}$
![[Drawing 2024-11-20 09.05.12.excalidraw]]

# Ableitung elementarer Funktionen
### Ableitung einer konstanten Funktion
![[Drawing 2024-11-20 09.25.23.excalidraw]]
### Ableitung der Potenzfunktion
![[]]