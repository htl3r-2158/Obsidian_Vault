![[Drawing 2024-05-31 08.43.17.excalidraw | 1000]]
#Vektor
## HÜ
A(-2 | -2), B(3 | -1), C(-1 | 3) Berechne den Umfang des Dreiecks

![[Drawing 2024-06-06 13.04.12.excalidraw]]

## Multiplikation eines Vektors mir einer reellen Zahl:

Windstärke wird gemessen:
>Eine Multiplikation eines Vektors mit einer Zahl verändert den "Betrag" des Vektors


z.B. $3*\vec{a} = 3 * (\frac{4}{3} * (\frac{12}{9})$

>Multipliziert man $\vec{a} = w=\begin{pmatrix} a_x\cr a_y\cr\end{pmatrix}$ mit $-1$, so erhält man den  #Gegenvektor zu $\vec{a}$.

> #Einheitsvektor $\vec{a_{0}} = \frac{\vec{a}}{|\vec{a}|} = 1$

> #Nullvektor = $\begin{pmatrix} 0\cr0\cr \end{pmatrix}$ erhält man wenn man einen Vektor mit $0$ multipliziert

### Beispiel:
Multipliziere die Vektoren mit den gegebenen Faktoren. Wie ändern sich die Vektoren? Geben sie die speziellen Vektoren an.
$\vec{a} = \begin{pmatrix} -8 \cr 10 \cr \end{pmatrix}; s= 0,4$    $\vec{a_S} = \begin{pmatrix} -3,2 \cr 4 \cr \end{pmatrix}$    $|\vec{a}| > |\vec{a_S}|$

## Addition und Subtraktion von Vektoren

>Vektoren werden Koordinatenweise addiert bzw. subtrahiert
> $\vec{a} \pm \vec{b} = \begin{pmatrix} a_x \pm b_x \cr a_y \pm b_y \cr \end{pmatrix}$

### Grafisch
$\vec{a} = \begin{pmatrix} 4 \cr -3 \cr \end{pmatrix}$
$\vec{b} = \begin{pmatrix} 3 \cr 5 \cr \end{pmatrix}$
![[Drawing 2024-06-06 13.44.50.excalidraw]]

## Komponentendarstellung eines Vektors
$\vec{a}\begin{pmatrix}a_x \cr a_y \cr\end{pmatrix} = a_x * \vec{i} + a_y * \vec{j}$
##  #Skalarprodukt zweier Vektoren $\vec{a}$ und $\vec{b}$
$\vec{a} * \vec{b} = |\vec{a}| * \vec{b}| * cos\phi$
↑ Inneres Produkt von $\vec{a}$ und $\vec{b}$

### Beispiel: Die Arbeit als Skalarprodukt
$W = F_S * s = |\vec{F}| * |\vec{s}| * cos\phi$

## Besondere Skalarprodukte

> Normal aufeinander stehende Vektoren:
> Sind $\vec{a}$ und $\vec{b}$ keine Nullvektoren, so ist $\vec{a} * \vec{b} = |\vec{a}| * |\vec{b}| * cos \phi = 0$
> nur dann, wenn $cos \phi = 0$ oder $\phi = 90°$, die Vektoren also normal (orthogonal) aufeinander stehen

Speziell gilt: $\vec{i} * \vec{j} = 1 * 1 * cos90° = 0$
$\vec{a} * \vec{a} = \vec{a}^2 = |\vec{a}| * |\vec{a}| * cos 0° = |\vec{a}|^2 * 1 = |\vec{a}|^2$

## Koordinatenform des Skalarprodukts
$\vec{a} * \vec{b} = |\vec{a}| * \vec{b}| * cos\phi$

### Beispiel:
1) $\vec{a} = \begin{pmatrix} 3 \cr 2 \cr \end{pmatrix}, \vec{b} = \begin{pmatrix} -2 \cr 4 \cr \end{pmatrix}; \vec{a} * \vec{b} = ? = 2$
2)  $\vec{a} = \begin{pmatrix} 2 \cr 4 \cr \end{pmatrix}, \vec{b} = \begin{pmatrix} b_x \cr -1 \cr \end{pmatrix};$            $\vec{a} * \vec{b} = 2 * b_x + 4*(-1) → b_x = 2$

## Der Winkel zwischen den Vektoren

#Skalarprodukt wird auf $\phi$ umgeformt
$\vec{a} * \vec{b} = |\vec{a}| * |\vec{b}* cos \phi$    $| : (|\vec{a} * \vec{b})$
$cos \phi = \frac{\vec{a} * \vec{b}}{|\vec{a}*|\vec{b}|} → \phi = arccos (\frac{\vec{a} * \vec{b}}{|\vec{a}| * | {b}|})$

_Allgemeine Formel_
>$\phi = arrcos(\frac{a_x * b_x + a_y * b_y} {\sqrt{a_x^2 + a_y^2} * \sqrt{b_x^2 + b_y^2}})$
