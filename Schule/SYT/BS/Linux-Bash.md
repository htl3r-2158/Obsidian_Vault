#Linux 
[[Windows-Kommandozeile]]
#bash : Born Again Shell + `bash.completion`
```shell
junioradmin@hostname:~$ /etc/#
```
#Tilde : (~) Home-Verzeichnis des aktuellen Benutzers
#Hashtag : (#) Achtung: root!
`sudo` … `superuser do` führt den folgenden Befehl als root aus
```shell
su - hugo #substitue /set user
//Simuliert einen login vorgang
```
Aufbau von Befehlen:
```shell
$Kommandoname -Option Arg1 Arg2
```
Optionen verändern das Verhalten

```shell
cp -p datei1 datei2 dir1 #copy
```
`-p` … preserve timestamp
`pwd` … print working directory
`man` … manual page `/` suche starten `N` vorherige Treffer `n` nächster Treffer
`ls` … list directory
```shell
//optionen für ls
-l ... long list
-a ... auch versteckte Dateien (beginnen ,it .)
-t ... time
-r ... reverse sort
```
| [[Windows-Kommandozeile]] | [[Linux-Bash]] |
|-|-|
|`dir`| `ls`|
|`help /?`| `man -h --help`|
|`cd hugo`| `pwd`|
|`copy`| `cp`|
|`more`| `mv`|
|`md`|`mkdir -p (create parent directory if not existing)`|
|`type more` | `cat (concatenate)`|
|`del`|`rm`|
|`rmdir /q /s`|`rm -rf (r recursive, f force`|
|`tree`|`tree`|
|`C:\users\hugo`|`/home/hugo`|
|`..\kurt\x.txt`|`../kurt/x.txt`|

`rm -rf /` !!!!!! Achtung löscht das ganze System !!!!!!

## Unterschiedliche Erkennung von Dateien
![[Drawing 2024-01-30 11.56.10.excalidraw | 1000]]
### Beispiel wie eine Python File unter Linux gestartet wird
![[Drawing 2024-01-30 12.03.13.excalidraw]]
`root` … Administrator, dessen Home-Verzeichnis liegt in `/root`
andere Benutzer, dessen Home Verzeichnis liegt unter `/home`
### Wichtige Verzeichnisse
Verzeichnis | Erklärung
|-|-|
`/`|Stamm Verzeichniss, Haupt-Vz, Wurzel-Vz
`/root`|
`/home`|
`/etc`| editable text configuration (Wichtige Systemkonfiguration Dateien)

## Befehle Verketten

```shell
cmd1; cmd2   hrt cmd1 aus und startet anschließend               # cmd2
cmd1 && cmd2 # startet cmd1, nur wenn cmd1 erfolgreich               # war => cmd2
cmd1 || cmd2 # startet cmd2, nur wenn cm1                            # fehlgeschlagen war => cmd2
```
erfolgreich $<=>$ Exit-Code war $0$ `exit(0)`
nicht erfolgreich $<=>$ Exit-Code war ungleich $0$
```shell
cp [Quelle] [Ziel] && eco "hurra" || echo "oje"
```

## Eingabe-/Ausgabeumleitung
### Ausgabeumleitung
```shell
echo Hallo 2BI > 2bi.txt           # Überschreibt
echo Heute ist Dienstag >> 2bi.txt # hängt hinten an
```
### Eingabeumleitung
```bash
befehl < x.txt # Die von befehl abgefragten Eingaben                   # werden nicht über die Tastatur sondern                # aus x.txt
```

```shell
p1 > file.txt # Statt "StdOut" zu file.txt geschrieben
```
### Umleitung von Befehlen und ihren Errors
![[Drawing 2024-01-30 13.02.01.excalidraw | 1000]]
```shell
P1 2> error.txt #Fehlermeldungen = StdError umleiten
P1 > file.txt 2>&1 #Fehlermeldungen auch in file1.txt                      #umleiten
find / -name"*.txt" 2> /dev/null #schwarzes loch im                                      #linux System
```
## Wildcards / Joker
`*` … Beliebig viele beliebige Zeichen
