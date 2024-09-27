
## Kenngrößen
#Kenngrößen
![[Drawing 2024-05-06 08.12.13.excalidraw | 1000]]
_Liniendiagramm_

$T$ … #Periodendauer = Zeit bis sich die Kurvenform wiederholt

$f$ … #Frequenz in $Hertz$ = Anzahl der Perioden in einer Sekunde $f = \frac{1}{T}$

$Û$ … #Amplitude = #Scheitelwert = höchster vorkommender Wert

$U_{SS}$ … #Spitze-Spitze-Wert = Abstand zwischen höchstem und tiefstem Wert

$U$ … #Effektivwert = Gleichspannung die an einem ohmschen Widerstand die gleichen Wärme Verluste bewirkt, wie die Wechselspannung

> Für Sinusgrößen gilt : $U = \frac{Û}{\sqrt{2}}$

## Zeigerdiagramm
![[Drawing 2024-05-06 08.38.01.excalidraw]]
_Zeigerdiagramm_

$U$ zum Zeitpunkt $t$ 
$\alpha$ … #Phasenwinkel
$\omega$ … #Winkelgeschwindigkeit
$\alpha = \omega * t$
$\omega = 2 * \pi * f$

>Jeder Zeiger stellt eine sinusförmige Spannung oder einen sinusförmigen Strom dar

>Die Länge des Zeigers entspricht der Amplitude einer Spannung oder Stromstärke. Der Winkel entspricht ihrer #Phasenlage

## Eigenschaften von Widerstand, Spule und Kondensator bei sinusförmiger Wechselspannung

### Widerstand
![[Drawing 2024-05-06 08.45.24.excalidraw]]
$I = \frac{U}{R}$

Spannung und Strom haben die selbe #Phasenlage (Zeigerrichtung) Ein Widerstand leitet alle Frequenzen gleich gut.

## Impedanz

> $Z = R+jX$
> Widerstand den man dann wie ein Widerstand bei Gleichspannung berechnen kann


Normaler Widerstand: $Z_R = R$
Spule : $Z_L = j \omega L$
Kondensator: $Z_C = -\frac{j}{\omega C} = \frac{1}{j \omega C}$

### Bsp.:
$U_q = 10V$
$f = 11288Hz$
$R = 10 \ohm$
$C = 470 nF$
$ges: \ I, U_r; U_C$

![[Drawing 2024-06-10 08.15.56.excalidraw]]
### Bsp.:
![[Drawing 2024-06-10 08.32.02.excalidraw]]

**:: Ab hier im 3. Jahrgang ::**

Widerstand (R), Spule (L) Kondensator (C) bei sinusförmiger Wechselspannung

| Bauteil         | Zeichen                                     | Formel                                                         | Leitereigenschaft                       | Phasenlage                                      |
| --------------- | ------------------------------------------- | -------------------------------------------------------------- | --------------------------------------- | ----------------------------------------------- |
| Widerstand $R$  | ![[Drawing 2024-09-05 12.04.57.excalidraw]] | $I = \frac{U}{R}$                                              | leitet alle Frequenzen gleich gut       | Spannung und Strom haben die gleiche Phasenlage |
| Spule $L$       | ![[Drawing 2024-09-05 12.10.22.excalidraw]] | $I = \frac{U}{X_L}$ $X_L = \omega * L$<br>$\omega = 2 \pi * f$ | leitet tiefe Frequenzen besser als hohe | Der Strom eilt gegenüber der Spannung 90° nach  |
| Kondensator $C$ | ![[Drawing 2024-09-05 12.10.45.excalidraw]] | $I = -\frac{U}{X_C}$ $X_C = - \frac{1}{\omega C}$              | leitet hohe Frequenzen besser           | Der Strom geht der Spannung um 90° vor          |

## Bsp.:
![[Drawing 2024-09-05 12.12.42.excalidraw]]

## Bsp.:
![[Drawing 2024-09-05 12.21.09.excalidraw]]
## Bsp.:
![[Drawing 2024-09-12 11.43.53.excalidraw | 1000]]
## Bsp.:
![[Drawing 2024-09-12 12.14.40.excalidraw |1000]]

## Wie es schneller geht:
$Z_R = R$
$Z_C =  \frac{1}{j*\omega*C}$
$Z_{ges} = R + \frac{1}{j*\omega*C}$
$I = U_q * \frac{1}{R+\frac{1}{j*\omega*C}} * \frac{j*\omega*C}{j*\omega*C} = U_q * \frac{j*\omega*C}{j*\omega*R*C+1}$
$U_C = I * Z_C = U_q * \frac{j*\omega*C}{1+j*\omega*R*C} * \frac{1}{j*\omega*C} = U_q * \frac{1}{1+j*\omega*R*C}$
$|U_c| = U_q * \frac{1}{\sqrt{1+(\omega * R*C)^2}}$

$|Z_C| = \frac{1}{\omega*C}= R \ | \omega \ :R$
$2 * \pi * f = \omega = \frac{RC} \ | : 2* \pi$
$f_g = \frac{1}{2* \pi * R * C}$   -> Grenzfrequenz

