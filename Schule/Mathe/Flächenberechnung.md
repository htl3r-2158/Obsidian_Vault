---
noteID: 4604e120-e153-46e8-93a2-127955f2bd55
---
## Bsp. 1
Berechne den Inhalt der Fläche die von der Kurve $y = x^3 - 4x$ und der $x$ -Achse eingeschlossen wird.
1) Zeichne den Graphen

```functionplot
---
title: 
xLabel: x
yLabel: 	y
bounds: [-2,2,-4,4]
disableZoom: false
grid: true
---
y(x) = x^3 - 4x
```
### Nullstellen:
> um die Integratiosngrenzen zu Bestimmen
> $x^3 - 4x = 0$
> $x (x^2 - 4) = 0$
> $x = 0$    $x\pm \sqrt{4}$ 

$A_1  = \int^{0}_{-2} (x^3 - 4x) dx = [\frac{x^4}{4} - 2x^2]^0_{-2} = 4$

## BSp 4.
Es soll der Inhalt der Fläche berechnet werden, die von den Graphen der Funktion $f (x) = 5$ und $g (x) = x^2 +1$ eingeschlossen wird.

## Bsp. 5
Berechne den Flächeninhalt, der durch 2 Funktionen begrenzt wird

$f (x) = x^3 - 12x$
$g(x)= 9x +20x$


```functionplot
---
title: 
xLabel: x
yLabel: y
bounds: [-4,5,-20,70]
disableZoom: false
grid: true
---
f(x) = x^3-12x
g(x) = 9x +20
```
