#ER-Modell 

## Was ist eine rekursive Beziehung?

> Eine Beziehung zwischen #Entitiy ies die demselben #Entity-Typ angehören.

#### Bsp.:
- In einem Betrieb gibt es mehrere Personen
- Jede Person hat eine oder keine andere Person als Chef
![[Drawing 2024-09-12 08.33.41.excalidraw | 1000]]
#Fremdschlüssel 

## Einfache Aggregation
> Entities können

## Komposition
> spezielle Form der Aggregation:
> #Entity des Komponenten- #Entity-Typ 

## Was ist eine is-a-Beziehung
### Bsp.:
- Gegenstände in der Bibliothek
	- Buch
	- DVD
- Es gibt gemeinsame Eigenschaften
	- Titel
	- Erscheinungsjahr
- Eigenschaften die nicht gemeinsam sind
	- Regisseur
	- Spieldauer
	- Autor
	- Seitenzahl
→ Gemeinsame Eigenschaften in eine Tabelle abspeichern und nicht gemeinsame Eigenschaften auftrennen und nach Art (Film, Buch) in eigene Tabellen legen.