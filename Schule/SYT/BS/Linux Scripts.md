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