---
noteID: 66ab49b0-04b9-4365-be97-c7d02f9fd870
---
## Bsp. 1
>  Veranschauliche das bestimmte Integral $\int^{2}_{-1}(-2x^2 -1)dx$
> 
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 8.13am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
## Bsp.: 2
> Berechne das bestimmte Integral $\int^{2\pi}_{0} sin(x) dx$ und integriere das Ergebnis

![[Drawing 2025-05-07 08.28.11.excalidraw]]

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 8.30am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```

## Stückweise Integration
### Bsp. 3:
> Die obere Begrenzungslinie der dargestellten Fläche setzt sich aus den Parabelbögen zusammen. 
> Berechne das bestimmte Integral.
> Funktionsgleichung: 
> $f_1(x) = (x+2)^2$  für $-2 \leq x \leq 0$
> $f_2(x) = (x+2)^2$  für $0 \leq x \leq 2$

```functionplot
---
title: 
xLabel: x
yLabel: y
bounds: [-2,2,0,4]
disableZoom: true
grid: true
---
f1(x) = (x+2)^2
f2(x) = (x-2)^2
```

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 8.49am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
## Unbestimmtes Integral (Integrationsmethoden)
### Substition (Ersetzung)
#### Bsp. 1:
>  Berechne $\int(3x+2)^4dx$

Ersetzen von dem **linearen Term** durch $z = 3x +2$
$z' = \frac{dz}{dx} = 3 \ ->\ dx = \frac{dz}{3} = \frac{1}{3}dz$

-> $\int z^4 * \frac{1}{3} dz = \frac{1}{3} \int z^4 dz = \frac{1}{3} * \frac{z^5}{5} + C = \frac{z^5}{15} + C = \frac{(3x + 2)^5}{15} + C$

#### Bsp. 2:
$\int cos (5t + 1) dt$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 9.17am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```

#### Bsp. 3:
$\int\frac{3}{x-2}dx = 3 \frac{1}{x-2} dx$


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 9.24am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
#### Bsp. 4:
>  Nicht lineare Substitution: Berechne $\int \frac{x}{x^2+1} dx$


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 9.26am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
#### Bsp. 5:
Berechne $\int^{2}_{0} (x^2 + 1)^2 dx$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.5.7 - 9.36am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
