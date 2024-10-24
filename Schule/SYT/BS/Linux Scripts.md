#Linux #Shell #bash 

```bash
meinscript.sh           # Script Datei
sh meinscript.sh        # Ausführen
chmod +x meinscript.sh  # Ausführbar machen
./meinscript.sh         # Ausführbare Datei ausführen
```

```bash
#!/bin/bash            # Welches Programm zum ausführen

DATEI = /home/michael/fib1.txt # Variable
grep "..." $DATEI

$1 $2 $3              # Parameter

RABATT = 20

expr(4 + 5)*$RABATT   # Expression
UMSATZ = expr...

set -x                # Befehle nicht ausdrucken
set -e                # Bei Befehlfehler abbrechen

if [ ... ]            # If-Start -a AND -o OR
then
else
fi                    # If-Ende

read $X stdin=Tastatur # Liest von der Tastatur ein

echo "hallo welt \!"   # Standard Ausgabe
echo "" > datei1       # In Datei überscreiben
echo "" >> datei2      # An Datei anhängen

```

## grep
#grep: _get regular expression_

**Standard Syntax**
```bash
grep regulärer_Ausdruck  [Dateiname]
```

**Options**
```bash
-i     # Ignore Case
-v     # Text kommt nicht vor
-n     # Zeilennummer
-l     # Dateinamen mit Treffern auflisten
-r     # rekursive Suche

grep -i "^regulärer_Ausdruck" [Dateiname] # Text an                                              # Satzbeginn                                           # suchen

grep -i "regulärer_Ausdruck$" [Dateiname] # Text an                                              # Satzende                                             # suchen
```

## find
#find: _finde Dateien_

**Standard Syntax**
```bash
find [Verzeichnis] name *.txt
```

**Options**
```bash
-name   # Dateiname
-iname  # name case insensitive
-type   # Dateityp: f (file), d (directory) & l                # (Softlink)
-size   # Dateigröße: +10M (größer), -5k (kleiner) &           # 74c (genau 74 Characterlänge)
-user   # Datei-owner
-group  # Datei-owner-gruppe
-amin   # letzter Zugriff: -, + (min)
-mmin   # Le. Schreibzu.:  -, + (min)
-atime  # letzter Zugriff: -, + (days)
-mtime  # Le. Schreibzu.:  -, + (days)
```

## Steuerzeichen entfernen
```bash
-print0 | xargs -0 # Löscht etwaige Steuerzeichen
```



# Prozess
#Process: Gerade ausgeführtes Programm
```bash
sudo systemctl 
-              start
-              stop
-              restart, reload
-              disable         # Ob beim Boot gestartet
-              enable
-              status
```

### Thread

#Thread: Teil eines Prozesses

```bash
ps     # Process show
-e     # external
-f     # full-fomat


pstree
```