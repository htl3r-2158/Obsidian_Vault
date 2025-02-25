---
noteID: 142b306e-54d5-4e3d-a757-ba7e528f5a91
---
## 3.55 
B)
![[Drawing 2025-02-12 08.10.18.excalidraw]]
C)
![[Drawing 2025-02-12 08.40.08.excalidraw]]

## Unbestimmte Audsrücke
>  Ausdrücke der Form "$\frac{0}{0}$" oder "$\frac{\infty}{\infty}$" heißen unbestimmte Ausdrücke oder unbestimmte Form

### Buch S 156
#### Bsp 1)
![[Drawing 2025-02-12 08.48.25.excalidraw]]

>  Bei der Ermittlung des Grenzwertes dürfen Zähler und Namen getrennt ausgewertet werden.
>  Um den Grenzwert zu bestimmen verwendet man die Regel de l'Hospital


$\lim_{x \to 0}{\frac{f(x)}{g(x)}} = \lim_{x \to 0}{\frac{f'(x)}{g'(x)}}$

- Vorraussetzung, dass die Funktion f und g an $x_0$ differenzierbar sind. Es dar auch $\pm \infty$ eingesetzt werden
- Zähler und Namen sind getrennt zu differenzieren und danach der Grenzwert zu bilden
- Mehrmalige Anwendug öfters notwendig

#### Beispiele

a) $\lim_{x \to 1}{\frac{x^2 -1}{x-1}} = "\frac{0}{0}" -> \lim_{x \to 1}{\frac{(x+1) * (x-1)}{x - 1}} = \lim_{x \to 1}{x + 1} = 2$    oder $\lim_{x \to 1}{\frac{f'(x)}{g'(x)}} = \lim_{x \to 1}{\frac{2x}{1}} = 2$

b) $\lim_{x \to 0}{\frac{sin(x)}{x}} = "\frac{0}{0}" -> \lim_{x \to 0}{\frac{sin(x)'}{x'}} = \lim_{x \to 0}{\frac{cos(x)}{1}} = 1$

c) $\lim_{x \to \infty}{\frac{x^3}{e^x}} = \frac{\infty}{\infty} = \lim_{x \to \infty}{\frac{1}{e^x}} = 0$

d) $\lim_{x \to \infty}{\frac{x^3}{e^x} = \frac{\infty}{\infty}} \lim_{x \to \infty}{3x^2}{e^x} = \frac{\infty}{\infty} = \lim_{x \to \infty}{\frac{6x}{e^x}} = \frac{\infty}{\infty} = \lim_{x \to \infty}{\frac{6}{e^x}} = 0$

e) $\lim_{x \to \infty}{\frac{ln(x)}{x}} = \lim_{x \to \infty}{\frac{1}{x}} = \lim_{x \to \infty}{\frac{1}{\infty}} = 0$


4.107
![[Drawing 2025-02-12 09.26.49.excalidraw]]

### Monoton steigende Funktionen im Vergleich

> Die **Exponentialfunktion** $y = e^x$ geht schneller gegen $\infty$,
> als die **Potenzfunktion** $y = x^4 \ (n>0)$
> und diese schneller als die **logharithmische Funktion** mit $y = ln (x)$
