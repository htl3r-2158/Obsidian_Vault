## Allgemeines

> Physische Konzepte der Architektur von #Datenbanksystem en ergen sich aus dem logischen Konzept in Verbindung mit der Rechnerumgebung

### Betrachtungsweisen
- zentralisiert oder verteiltes #Datenbanksystem 
- #Client-Server-Konzept oder parallele #Datenbanksystem e

## Zentralisiertes #Datenbanksystem 
- #Datenbankmanagementsystem und die Anwendungen befinden sich auf einem Computer
- #Datenbank-Anwendung en laufen auf dem Server
- #Terminal s nur für Eingabe und Ausgabe
- Moderne Rechennetze verwenden vollwertige Arbeitsplatzrechner statt #Terminal s
![[Pasted image 20241106135233.png]]
## Verteiltes #Datenbanksystem 
- Mehrere Datenbanken die in einen Netz von Computern gespeichert wird
- Computer können geografisch getrennt sein
- Mechanismen zur Zusammenführung und Abfrage
	- Verteilung ist für Benutzer unsichtbar

# Verteilung eines #Datenbanksystem s
### homogen
#Datenbank en mit gleichem #Datenbankmanagementsystem 
### heterogen
#Datenbank en sind unterschiedlich gemanged.

# Vorteile von verteilten #Datenbanksystem en



| Lokale Autonomie                      | Abfragen effektiver ausgeführt, Daten dort wo sie gebraucht werden        |
| ------------------------------------- | ------------------------------------------------------------------------- |
| **Zuverlässigkeit und Verfügbarkeit** | Fällt ein Teil aus nicht das ganze System betroffen                       |
| **Leistung**                          | Verteilt sich auf mehr Rechner                                            |
| **Erweiterbarkeit**                   | Skalierbarkeit durch Hinzufügen und Entfernen                             |
| **Komplexität**                       | Synchronisation und Anfragen sehr aufwendig                               |
| **Dezentrale Verwaltung**             | Aufwand für die Verwaltung und Synchronisation                            |
| **Sicherheit**                        | Für mehrere Standorte muss sichergestellt werden und Kommunikationsknoten |
| **Kosten**                            | Höher durch Komplexität, Maßgeschneiderte Software (Wartung teurer)       |
## #Client-Server-DBS
- Zwei Prozesse kommunizieren über eine Schnittstelle miteinander
- Client-Server können sich auf einem Rechner befinden oder auf verschiedenen im Netzwerk
- #relationales-Datenbankmodell Abfragen mittels SQL. Server -> SQL-Server
- Client bsp. #Datenbank-Anwendung welche die Anzeige und Bearbeitung der Daten ermöglicht

- Kommunikation über Anforderung-Antwort Dialog
	- Client stellt Anforderungen. Server bearbeitet diese und schickt Antwort an Client
- Häufig Server von mehreren Clients gleichzeitig
- Server macht nichts so lange keine Client Anforderung

## #Paralleles-Datenbanksystem 
Laufen auf parallen Systemen die über ein schnelles Netz verbunden sind
- Mehrere PRozessoren, Platten, Hauptspeicher, ...
	- Verkürzung der Bearbeitungszeit

Bei großen #Datenbank en mit vielen Benutzern verursacht sequenzielle Verarbeitung lange Antwortzeiten

### Arbeitsweise
Daten auf alle verfügbaren Platten verteilt
Abfragen und Transaktionen werden aufgeteilt

### Architektur
#### #Shared-Memory-Architektur
_Shared-Everything-Architektur_

Alle #Prozessor en des Systems können auf den gemeinsamen Speicher zugreifen und darüber kommunizieren

#Daten für #Datenbankoperation werden von den #Prozessor en über das #Netzwerk angefordert und im #Speicher bereitgestellt
![[Pasted image 20241107082719.png]]
#### #Shared-Nothing-Architektur

Alle #Prozessor en haben einen eigenen #Speicher 

Jeder #Prozessor hat eine eigene Kopie des #Datenbankmanagementsystem s

Weitergeben von Funktionen an nicht ausgelasteten Prozessor ist die wichtige Arbeitsweise
![[Pasted image 20241107082731.png]]
#### #Shared-Disk-Architektur

#RAM ist den #Prozessor en lokal zugeordnet

Plattenspeicher werden gemeinsam genutzt

Arbeitsweise ähnlich wie bei #Shared-Nothing-Architektur 

#Daten werden angefordert wie bei #Shared-Memory-Architektur 
![[Pasted image 20241107082914.png]]
