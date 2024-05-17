_(Weiterführung von OneNote)_ [Informationstheorie](onenote:https://d.docs.live.net/bea805b7c1a2dd7b/Dokumente/OneNote-Notizbücher/GINF_2324/Mitschrift-Ginf.one#Informationstheorie&section-id={45B5E75E-00DA-489F-86FB-D038859CA35B}&page-id={A9DA4DF9-17AF-4AA2-B36D-F7161651C95A}&end)  ([Webansicht](https://onedrive.live.com/view.aspx?resid=BEA805B7C1A2DD7B%21332&id=documents&wd=target%28Mitschrift-Ginf.one%7C45B5E75E-00DA-489F-86FB-D038859CA35B%2FInformationstheorie%7CA9DA4DF9-17AF-4AA2-B36D-F7161651C95A%2F%29))]

# Digitale Signalverarbeitung
- Signale können mittels __ADC__ digitalisiert werden
- __digitalisieren__
	- abtasten = sampling
	- quantisieren (in wertdiskretes Signal umwandeln = als Zahlenwert abspeichern)

>[!success] Vorteile der digitalen Signalverarbeitung
>- ohne Verluste beliebig speicherbar
>- ohne Verluste belibig kopierbar
>- keine Übertragungsverluste
>- Möglichkeit zur Fehlerkorrektur
>- Möglichkeit zu Datenkomprimierung
>- Möglichkeit zur nicht-linearen Datenverarbeitung

>[!fail] Nachteile der digitalen Signalverarbeitung
>- höherer Hardwareaufwand
>- möglicher Informationsverlust durch Abtastung und Quantisierung
>- begrenzter Signalraum (es gibt einen größten und kleinsten Wert, den das Signal annehmen kann = Sättigung)

> #Abtasten: (sampling) periodisches Messen eines zeitkontinuierlichen Signales.
--> wandelt ein zeitkontinuierliches Signal in ein zeitdiskretes Signal um

> #Clipping: wenn ein Signal über den maximalen Wert liegt wird dieses "abgeschnitten"

> #Interfolieren: Aus einem Signal die Abtast-Punkte das Original Signal wiederherzustellen

> #Abtasttheorem von Shannon / Nyquist:
Um ein analoges Signal mit der nächsten auftretenden Frequenz von $f \ Hz$ in ein zeitdiskretes Signal umzuwandeln, muss die Abtastung mit einer Frequenz $f_s$ von mehr als $2*f \ \ Hz$ erfolgen!
Sonst kann man das analoge Signal nicht mehr aus den Abtastwerten rekonstruieren!

> #Aliasing-Fehler: tritt bei #undersampling auf_ wenn im abzutastenden Signal Frequenz-Anteile vorkommen, die näher (oder gleich) sind als die halbe Abtastfrequenz ist

> #Fourier-Synthese: jedes periodische Signal kann man als ==Summe== von unendlich vielen Sinus-Signalen darstellen, deren Frequenz ein ganzzahliges Vielfaches der "Grundfrequenz" (= 1. Harmonische) ist