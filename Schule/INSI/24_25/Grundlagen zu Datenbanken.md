#Datenbanksystem (DBS) besteht aus einer oder mehreren #Datenbanken und dem #Datenbankmanagementsystem (DBMS)
Die DB ist eine Sammlung von logisch zusammengehörigen Daten zu einem Sachgebiet.

Das DMS stellt die Schnittstelle zwischen der Datenbank und deren Benutzern her.

#Daten der #Datenbank bilden einen Teil der realen Welt ab.

Beziehungen sind abgespeichert

Mehrbenutzer Betrieb ist möglich
Benutzer haben keinen direkten Zugriff auf das #Datenbankmanagementsystem 

## #Datenbankmanagementsystem
- Software die Daten und Zugriffe verwaltet
- Sorgt dafür das keine mehrfachen Bearbeitungen auf einen Datenpunkt gleichzeitig stattfinden
- Daten sichern und bei Abstürzen wiederherstellen.
- Ermöglicht
	- Erstellen von #Datenbanken
	- Abfragen von Daten
	- Erzeugen ändern und löschen von daten
	- Verwaltung von Benutzern und Zugriffsrechten

## Schnittstelle -SQL
- Sprachkonzept
- SQL ist Standard

## Datenbankmodell
- #Datenbankmodell  beschreibt die logische Struktur einer #Datenbank 
- Bestimmt in welcher Form #Daten gespeichert, organisiert und verarbeitet werden

## Historische Entwicklung
- 1950er: Magnetbänder
- 1960er: Magnetplatten
- 1960er: Erste #Datenbanksystem verwendeten #hierarchiesche-Datenbankmodell
- 1970er: #Netzwerkdatenbankmodell
- späte 70er: #relationales-Datenbankmodell (Edgar F. Codd) erste kommerzielle Anwendung: Oracle 
- 1980: #objektorientiertes-Datenbankmodell
- 1990: #objektrelationales-Datenbankmodell
- 2000er: #dokumentenorientiertes-Datenbankmodell alternative Ansatz

## Hierarchisches Datenbankmodell
#hierarchiesche-Datenbankmodell 
![[Drawing 2024-09-25 13.57.04.excalidraw | 1000]]

- Für die Verarbeitung unterschiedlich langer Datensätze
- Baumartige Struktur
	- untergeordneter Knoten ist von seinem Vorgänger abhängig
	- #Knoten kann mehrere #Kindknoten haben
	- #Kindknoten kann nur einen #Elternknoten
## Netwerkdatenbankmodell
#Netzwerkdatenbankmodell 
- Gleichartige Daten werden in #Recordset s gespeichert, die miteinander in Beziehung stehen
- Einem #Record eines #Recordset s können mehere #Record s eines anderen #Recordset s zugeordnet werden
- Beziehung darf nur in eine Richtung gehen
## Relationales Datenbankmodell
#relationales-Datenbankmodell 
- Daten werden in #Relationen (Tabellen) gespeichert
- am weitesten verbreitet
- Zwischen #Relationen können #Beziehung en definiert werden, die sich abhängig von der Anzahl der in Beziehung stehenden #Datensätze (Tabellenzeilen) unterscheiden
- SQL
## Dokumentorientiertes Datenbankmodell
- #Datensätze die unterschiedliche Eigenschaften und auch eine unterschiedlice Anzahl von Eigenschaften haben können
- ...
## Objektorientiertes Datenbankmodell
- ...