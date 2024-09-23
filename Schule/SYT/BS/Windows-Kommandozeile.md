#Windows
## Warum CMD
- man ist häufig schneller
>[!info]- Beispiel
>`mkdir a b c d` legt gleich diese 4 Ordner -> effizienter als in der graphischen
## Befehlssyntax und Hilfe

Die Option `/?` zeigt Syntax und Hilfe eines Befehles an:
```shell
dir /?
dir [Laufwerk:][Pfad][Dateiname][...] [/p][/q][/a] ...
    ------------Parameter------------ --Optionen--
```
`/p, /q, /a` ändern die Verhaltensweise des Befehls (hier welche Dateien angezeigt werden und in welcher Reihenfolge)

Windows:
	`/` … leitet Optionen ein (Verändert Verhalten eines Befehls)
	`\` … Trennzeichen zw. Ordner / Dateien

## Sonderzeichen
### `*` und `?`

`*` Platzhalter (=Wildcard, Joker) für beliebig viele Zeichen (auch 0 Zeichen)
`?` Platzhalter für genau ein belibiges Zeichen (außer `.`)

>[!info] Beispiel
>`dir *.txt` jede Datei, die mit `.txt` endet
>`dir a?1.*` alle Dateien, deren Namen: 
>- mit a beginnen
>- danach kommt ein einziges beliebiges
>- anschließend die Zeichen `1` und `.`
>- und zuletzt beliebig viele weitere Zeichen

#Dateinamen
```
lusmgr   . msc
Dateiname  Extension
(max 82 Z) (max 3 Zeichen)
```
DOS … Disk Operating System (Vorgänger von Windows)

Extension: entscheidet, welches Programm eine Datei öffnet … Windows
Linux … Magic Sequenz … erste Zeichen im Datei Inhalt entscheiden welches Programm die Datei öffnet
![[Drawing 2024-01-09 12.16.37.excalidraw | 600]]
>[!note] __Zeige alle Dateien an, die …__
>- mit einem a beginnen
>- als Dateierweiterung `.txt` haben
>- mit `foto` beginnen und mit `.jpg` enden
>- genau 5 Zeichen lang sind
>- als drittes Zeichen `t` haben
>- als letztes Zeichen ein `i` haben
>- als drittes Zeichen ein `g` und als vorletztes Zeichen ein `o` haben
>--> `dir a* *.txt foto*.jpeg ????? ??t* *i ??g*o?`

### Punkt `.`

`.` geht zum Nächst höheren Verzeichnis

>[!note] Beispiel
>`dir ..`
>`cd ..`
>`.\programm.exe`
>`copy a*.txt ..\temp`
>`move ..\*.jpg .`

### Pipe `|`

Mit der Pipe `|` kann man Befehle verketten und nacheinander ausführen
# Operationen um Verzeichnisse und Dateien zu bearbeiten
#Verzeichnis-Operationen

#Kopieren
`ren` … Datei / Verzeichnis umbenennen
`copy` … Datei /Verzeichnis
`mov` … Datei / Verzeichnis verschieben
`del` … Datei / Verzeichnis löschen

#tree
`tree` … Zeigt die Verzeichnisstruktur
`tree /f` … Dateien auch anzeigen

#Laufwerke
`[Laufwerksbuchstaben]:` … wechselt in das Laufwerk

#Schreiben
`[Dateiname] > [Neuer Text]` … Überschreibt den Text in der Datei
`[Dateiname] >> [Neuer Text]` … Fügt den Text der Datei hinten dazu
`[Befehl] < [Dateiname]` … Eingabeumleitung, Befehlsausgabe wird in die Datei eingefügt
>[!note] Beispiel
>`dir /a /b c:\windows\system32 > listing.txt`
>`echo "Erstellt am" >> listing.txt`
>`date /t >> listing.txt`
>`type x.txt >> listing.txt`

#Tastenkürzel
`[Pfeil Nach Oben]` … letzter Befehl
`[F7]` … zeigt alle verwendeten Befehle an
`[F8]` … letzten Befehl vervollständigen
`[TAB]` … vervollständigt den letzten Befehl
`[STRG + C]` … Beendet die Ausführung von einem Befehl

# Prozess
… Programm in Ausführung
Jeder Prozess hat eine `pid` eine Nummer die dem Prozess eindeutig zugewiesen werden kann