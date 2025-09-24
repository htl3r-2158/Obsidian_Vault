---
noteID: 73fcc494-142d-4eb6-a6c6-d92721d513f1
---
## VPN Technology
![[Pasted image 20250531142720.png]]
_Beispiel von VPNs_

VPNs werden genutzt um End-zu-End private Netzwerk verbindungen zu gewährleisten. Es simuliert ein privates Netzwerk obwohl der eigentliche Traffic über ein öffentliches Netzwerk geht. 

### Benfefits
Heutige VPNs verschlüsseln Nachrichten und verwenden IPsec und SSL um Sichere Verbindungen sicherzustellen.

### Site-to-Site und Remote-Access VPNs
#### Site-To-Site VPN
![[Pasted image 20250531143101.png]]
#### Remote-Access VPN
![[Pasted image 20250531143125.png]]

### Enterprise and Service Provider VPNs
VPNs können auf diese verschiedenen Arten aufgesetzt und gemanaged werden:
- Enterprise VPNs
	- Vom Unternehmen
	- Site-to-site
	- Remote Access 
	- IPsec
	- VPNs
- Service Provider VPNs
	- Von ISP
	- MPLS (für sichere Kanäle)
	- Trennung von standard Traffic und Kunden-Traffic
## Types of VPNs
### Remote-Access
![[Pasted image 20250531143901.png]]
Gehen meist von einzelnen Nutzern aus die einen sicheren Tunnel brauchen und auch aufbauen.
### SSL
Verwendet die Public-key-Infrastruktur um Nutzer zu authentifizieren. Wenn aber Sicherheit einen höheren Stellenwert hat sollte man IPsec lieber verwenden.
### Site-to-Site
![[Pasted image 20250531144233.png]]
Zwei nur über das Internet verbundene  (oder generell öffentlichem Netzwerk) bauen zwischen den Gateways (Router und/oder Firewall) einen sicheren Tunnel auf ohne das die Hosts irgendetwas davon mitbekommen würden. Für sie wirkt es so als ein kohärentes Netzwerk.
### GRE over IPsec
![[Pasted image 20250531144810.png]]
Ein nichtsicheres Site-to-Site VPN tunneling protocol, welches allerlei verschiedene network layer protocols encapsulaten kann.
Es löst das Problem das eine standard IPsec VPN nicht Routing-Information austauschen kann, mit GRE over IPsec wird das Routing Protocol in das GRE verpackt und dann zusätzlich noch in ein IPSec packkte um es sicher zum VPN-Gateway zu senden.
### Dynamic Multipoint
![[Pasted image 20250531145022.png]]

Gedacht für mehrere VPNs die in einer einfachen, dynamischen und skalierbaren Art und Weise aufgebaut werden sollen. 
Der Hub ist der zentrale Knotenpunkt der alle Spokes (Endständiger Router der Branchsites) mit VPN-Tunneln verbindet.
Spoke-Sites können auch über den Hub Informationen über andere Spoke-Sites bekommen und so Spoke-to-Spoke Tunnels aufbauen.
### IPsec Virtual Tunnel interface
Ähnliches Konzept wie Dynamic Multipoint jedoch werden die Tunnel auf ein virtuelles statt einem physischen Interface konfiguriert.
Es werden Site-to-Site oder hub-and-spoke Topologien unterstützt.
### Service Provider MPLS
![[Pasted image 20250531145909.png]]
ISPs verwenden MPLS um Datenverkehr von den einzelnen Kunden aufzutrennen und auf verschiedene Wege (Geräte) die einzelnen Standorte miteinander zu verbinden. Damit sind die Verbindungen sicher weil niemand den Datenverkehr eines anderen Kunden sehen kann und damit liegt die Verantwortung auch beim ISP.
## IPsec

IPsec (Internet Protocol Security) ist ein IETF-Standard (RFC 2401-2412), der definiert, wie Daten über IP-Netzwerke sicher übertragen werden können. Es wird oft in VPNs verwendet, um die Sicherheit auf Layer 3 (Netzwerkschicht) zu gewährleisten.

### Funktionen von IPsec

IPsec bietet folgende Sicherheitsfunktionen:

- **Vertraulichkeit**: Durch symmetrische Verschlüsselung (DES, 3DES, AES, SEAL) wird der Inhalt der Pakete geschützt.
    
- **Integrität**: Hash-Algorithmen (MD5, SHA) prüfen, ob Daten unverändert ankommen.
    
- **Authentifizierung des Ursprungs**: Quelle und Ziel authentifizieren sich gegenseitig mittels PSK oder RSA.
    
- **Schlüsselaustausch**: Über Diffie-Hellman-Gruppen wird ein sicherer, symmetrischer Schlüssel vereinbart.
    

IPsec ist modular aufgebaut. Jede Funktion (Protokoll, Verschlüsselung, Integrität, Authentifizierung, DH) kann individuell mit passenden Algorithmen bestückt werden.

### IPsec-Protokolle

- **AH (Authentication Header)**: Bietet Integrität & Authentizität, aber keine Verschlüsselung.
    
- **ESP (Encapsulating Security Payload)**: Bietet sowohl Verschlüsselung als auch Authentizität.
    
- **ESP + AH**: Kombination beider Verfahren für maximale Sicherheit.
    

### Beispiel für Security Associations (SAs)

- **SA 1**: AH, keine Verschlüsselung, MD5, PSK, DH16
    
- **SA 2**: ESP, AES, SHA, RSA, DH24
    

> Hinweis: SAs sind Kombinationen aus Parametern, die zwischen VPN-Peers ausgetauscht werden und die sichere Kommunikation definieren.

### Vertraulichkeit – Verschlüsselungsalgorithmen

|Algorithmus|Schlüssellänge|Sicherheit|
|---|---|---|
|DES|56 Bit|Niedrig|
|3DES|3×56 Bit|Mittel|
|AES|128–256 Bit|Hoch|
|SEAL|160 Bit|Sehr hoch|

Verwendet werden nur symmetrische Algorithmen (gleicher Schlüssel für Ver- und Entschlüsselung).

### Integrität – Hashing

|Algorithmus|Schlüssellänge|Sicherheit|
|---|---|---|
|MD5|128 Bit|Niedrig|
|SHA|160 Bit|Höher|

> Hinweis: SHA-1 gilt als veraltet. Empfehlung: mindestens SHA-256.

### Authentifizierung

- **PSK (Pre-Shared Key)**: Manuell eingetragene Schlüssel, einfach aber schlecht skalierbar.
    
- **RSA (digitale Zertifikate)**: Sicherer, verwendet asymmetrische Kryptografie zur Peer-Authentifizierung.
    

Beide Verfahren laufen in beide Richtungen (jeder Peer authentifiziert den anderen).

### Diffie-Hellman – Sicherer Schlüsselaustausch

DH ermöglicht es, über ein unsicheres Netzwerk einen geheimen Schlüssel auszutauschen.

|DH-Gruppe|Schlüsselgröße|Sicherheit|Anmerkung|
|---|---|---|---|
|DH1|768 Bit|Niedrig|Veraltet|
|DH2|1024 Bit|Niedrig|Veraltet|
|DH5|1536 Bit|Mittel|Veraltet|
|DH14–16|2048–4096 Bit|Hoch|Klassisch|
|DH19–24|256–2048 Bit|Sehr hoch|ECC-basiert, bevorzugt für neue Systeme|

> DH24 gilt als besonders sicher und für moderne VPNs empfohlen.