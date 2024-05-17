## Einschub nächste Labor Aufgabe
![[Drawing 2024-01-16 11.43.36.excalidraw | 500]]
## Warum ein Backup?
Hardware-Ausfall:
- Harddisks
	- Mechanischer Verschleiß (z. B. Lesekopf)
- SSDs
	- Häufiger Schreibzugriff auf eine Speicherzelle
- Power-Supply
	- Glättungskondensatoren (Elko)
![[Drawing 2024-01-16 12.03.22.excalidraw | 500]]

## Fünf Goldenen Regeln für Backups
1. regelmäßig
2. automatisch (z.B. per `cron-job` gesteuert)
3. geographisch getrennt lagern (Cloud (Nachteil Cyberattacken?, Datenschutz?))
4. unterschiedliche Datenträger/Medien
5. Testen
## 3-2-1 Regel
- 3 Datenkopien auf …
- … 2 unterschiedlichen Medien …
- … und 1 auf eine externen Backup (Cloud (verschlüsseln!))

## Backuparten
![[Drawing 2024-01-16 12.23.05.excalidraw | 1000]]
## Definitionen:
#Ransomware … Erpresst ein Lösegeld durch Datenverschlüsselung
#Recovery … Backup wieder einspielen
#Elko … Elektrolytkondensator (Plattenkondensator $C = {\epsilon}_0 * {\epsilon}_{R} * \frac{A}{d}$)
#Vollbackup … [[siehe #Vollbackup]]
#Offline-Backup … Rechnerbetrieb vor dem Backup herunterfahren
#Online-Backup … Dienste laufen währen des Betriebs weiter --> kompliziert => Snapshot-Mechanismen sorgen für konsistente Daten! Vorteil: Keine Downtime
