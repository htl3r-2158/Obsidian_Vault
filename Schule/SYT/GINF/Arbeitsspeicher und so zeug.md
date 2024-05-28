## Bsp.:
> Geg: Größe des virtuellen Speichers = $v = 64 ki$
> ges: Wie viele Bit hat die virt. Adresse?

 Lösung $lb(v) = lb(64ki) = 16$

## Bsp.:
> Geg: phys. Adresse  = $15bit$
> ges: Wie groß ist der Arbeitsspeicher?

=>$2^{15} = 32kib$

## Paging

### Begriffsdefinitionen
#Swapping : ganze Prozesse auslagern
#Paging: einzelne Seiten werden ausgelagert

Jeder aktive Prozess hat eigenen Adressraum -> eigene Seitentabelle
$\Sigma$ Adressräume aller aktiven Prozesse kann größer sein als Arbeitsspeicher

#Working-Set: Menge an Seiten, die ein Prozess zu einem bestimmten Zeitpunkt benutzt

Nur aktuell benötigte Seiten im Arbeitsspeicher
Rest wird im #Seitenspeicher = #Hintergrungdspeicher ausgelagert
	Auslagerungsdatei = Pagefile.sys (Windows)
	"Swap"-Partition (Linux)

#Demand-Paging : Seiten werden nur bei Bedarf geladen
#Page-Fault : wenn ausgelagerte Seite adressiert wird (derzeit nicht im AS)
	Seite vom Seitenspeicher holen und in AS
	Falls kein freier Platz -> Andere Seite aus HS verdrängen = **auslagern**
		Wurde auszulagernde Seite verändert?
			Nein: Seite läschen
			J: Seite muss auf Seitenspeicher zurückgeschrieben werden
			
#Thrashing: Falls Arbeitsspeicher kleiner ist als die Working Sets aller Prozesse
	häufige Page Faults bremsen System ein
#TLB: #Translation-Lookaside-Buffer 
	Cache-Speicher für Adressumsetzung