# Zusammenfassung der Themen

##### Blockchiffre

Text der Länge *X* wird in Blöcke der Größe *n* (64, 128, 256 oder 512 Bits) aufgeteilt. Ggfs. wird aufgefüllt um den kompletten Block zu füllen. Jeder Block wird **symmetrisch** (d.h. es gibt einen Schlüssel, der zum ver- und entschlüsseln verwendet wird) verschlüsselt. Daraus entsteht ein Chiffrat der Länge *n*

Eine Blockchiffre verwendet einen *n-bit* Block der Klartextes als Eingabe und liefert als Ausgabe einen ebenso großen Block mit verschlüsseltem Text; es handelt sich daher um einen **monoalphabetischen** Code.

*Quelle: Kapitel 3, Seite 3,4*

**Blockchiffren** können sowohl als Substitutions- als auch als Transpositionschiffre realisiert werden. Transposition (das vertauschen der Symbolreihenfolge) wird aber wegen dem geringen Schutz in modernen Blockchiffren nicht mehr verwendet. Stattdessen verwendet man eine Kombination von Transpositions- und Substitutionschiffren sowie anderen Einheiten

*Quelle: Kapitel 3, Seite 5,7*

Nachteile von Blockchiffren (symmetrische Verschlüsselung):

- Anzahl der benötigten Schlüssel *n * (n-1) / 2*
- Verteilung der Schlüssel
- Beweislast, Missbrauch des Schlüssels (Authentizität ist nicht gegeben)

##### Transposition

Transposition ist ein Verschlüsselungsverfahren, bei dem die Zeichen einer Botschaft (des Klartextes) umsortiert werden. Jedes Zeichen bleibt unverändert erhalten, allein die Stelle wird geändert, an der es steht. Ein Wort mit drei Buchstaben wie  *"nur"* kann auf sechs verschiedene Weisen umgestellt (*"transponiert"*) werden: nur, nru, rnu, run, urn, unr.

*Quelle: Kapitel 2, Seite 11*

##### Substitution

Substitution bezeichnet Verschlüsselungsverfahren, bei denen die Symbole des Klartextes durch andere Symbole ersetzt werden. Die Zuordnung wird durch ein sogenanntes Alphabet beschrieben. Die Anzahl der Verschlüsselungsmöglichkeiten entspricht der Anzahl der möglichen Alphabete.

*Quelle: Kapitel 2, Seite 11*

##### Monoalphabetisch

Bedeutet dass ein Symbol immer durch das gleiche Symbol (oder Gruppe) ersetzt wird. Beispiel hierfür ist die *"Ceasar-Verschlüsselung"*. Hier wird ein Buchstabe durch einen anderen ersetzt. Wenn z. B. ein "a" durch "b" und ein "b" durch ein "c" ersetzt wird sieht die Verschlüsselung des Textes "abba" wie folgt aus: "bccb". Anfällig gegen **statistische Attacken**

*Quelle: Kapitel 2, Seite 16*

##### Polyalphabetische Chiffren

Ein Symbol im Klartext wird nicht mehr durch ein unveränderlich festgelegtes anderes Symbol ersetzt. Jedes Zeichen im chiffrierten Text wird nun abhängig gemacht von dem entsprechenden Zeichen des Klartextes und zusätzlich von dessen Position im Text. Obiges Beispiel mit "abba" würde Beispielsweise "bcde" ergeben (unwichtig wie dieses Chiffrat zu Stande gekommen ist, es ist nur wichtig zu sehen, dass ein "a" nicht automatisch in ein "b" verwandelt wird).

*Quelle: Kapitel 2, Seite 19*

##### Produktchiffren

Bestehen aus Funktionsblöcken wie Substitution, Permutation und anderen Komponenten. Dadurch sollen zwei wichtige Ziele erreicht werden:

- Diffusion (Verwischen der Beziehung zwischen Klartext und chiffriertem Text)
- Confusion (Verwischen der Beziehung zwischen chiffriertem Text und Schlüssel)

Diffusion und Confusion werden durch mehrfache Verwendung von Produktchiffren verbessert.

##### Diffusion und Confusion

**Diffusion** soll die Beziehung zwischen Klartext und chiffriertem Text verbergen. Ein Symbol wird dadurch abhängig von vielen oder allen Symbolen des Klartextes. Falls ein Symbol im Klartext geändert wird, werden sehr viele oder alle Symbole im chiffriertem Text verändert.

**Confusion** soll die Beziehung zwischen dem chiffriertem Text und dem benutzten Schlüssel verbergen. Wenn ein einzelnes Bit im Schlüssel verändert wird, sollen sich möglichst viele Bits im chiffriertem Text verändern.

*Quelle: Kapitel 3, Seite 9*

##### Statistische Analyse / Häufigkeitsanalyse

Bei monoalphabetischer Verschlüsselung wird jeder Buchstabe eines Alphabetes einem bestimmten anderen zugeordnet. Dadurch bleibt die Häufigkeit des Auftretens der einzelnen Buchstaben erhalten. Somit lassen sich durch eine einfache Häufigkeitsanalyse Rückschlüsse auf den ursprünglichen Text ziehen, sofern man dessen Sprache kennt oder erraten kann.

In deutschen Texten tritt etwa der Buchstabe "e" mit einer mittleren Wahrscheinlichkeit von 17,4 Prozent auf und übertrifft damit alle anderen Buchstaben weit. Findet man also in einem verschlüsselten Text einen Buchstaben, dessen Häufigkeit der der anderen deutlich übersteigt, handelt es sich sehr wahrscheinlich im Klartextalphabet um das "e". Auch Buchstabenpaare (Bigramme) treten mit unterschiedlichen Häufigkeiten auf: "en" ist beispielsweise mit 3,9 Prozent das häufigste Bigramm. Mit solchen Kenntnissen ausgestattet, kann ein Angreifer durch statistische Analyse monoalphabetische Codes sehr schnell entschlüsseln.

*Quellen: Kapitel 2, Seite 17*

**Symmetrische Chiffren** werden in zwei Kategorien eingeteilt:

- **Stromchiffren**: Ein Symbol (z. B. ein Buchstabe oder ein Bit) wird nach dem anderen ver- oder entschlüsselt
- **Blockchiffren**: Es werden Blöcke gebildet und diese werden dann gemeinsam chiffriert. Wenn bei jedem Block derselbe Schlüssel verwendet wird, handelt es sich um eine monoalphabetische Chiffrierung mit einem sehr großen Alphabet

*Quelle: Kapitel 3, Seite 15*

Bei **synchronen** Stromchiffren ist der Schlüsselstrom unabhängig vom Klartext (Beispiel: *Output Feedback Mode*)

Bei **nicht synchronen** Stromchiffren hängen die Schlüssel ab vom Klartext oder dem chiffriertem Text (Beispiel: *Cipher Feedback Mode*)

*Quellen: Kapitel 3, Seite 17*

##### One-Time-Pads
- Klartext wird in eine Bitfolge verwandelt
- Ein zufälliger (einmalig verwendeter) Schlüssel wird erzeugt und über einen sicheren Kanal dem Empfänger übermittelt
- Schlüssel ist per XOR mit dem Text verknüpft
- Keine statistische Analyse möglich
- Datenmenge auf Schlüsselgröße beschränkt

*Quelle: Kapitel 3, Seite 20*

Symmetrisches Verschlüsselungsverfahren, welches polyalphabetisch ist. Bei *One-Time-Pads* handel es sich um Stromchiffren

##### RC4
- Wird zur Sicherung von Wlans verwendet
- ist ein kryptografischer Zufallsgenerator
- Mit einem Schlüssel (Anfangswert, seed) wird bei beiden Kommunikationspartnern unabhängig voneinander ein reproduzierbarer Schlüsselstrom erzeugt

*Quelle: Kapitel 3, Seite 23*

##### WEP
- Blockchiffre für symmetrische Schlüssel
- Ein kleine Änderung des Klartextes (oder des Schlüssels) bewirken eine große Veränderung des chiffrierten Texts (Avalanche Effekt)
- Jedes Bit im chiffrierten Text soll von möglichst vielen Bits des Klartextes abhängig sein. Die Konzepte der Diffusion und Confusion sind in hogem Maß realisiert
- 2^56 verschiedene Schlüssel sind möglich, d.h. "schnell" zu brechen

*Quelle: Kapitel 4, Seite 2,9*

##### Triple DES
- Mehrfaches ausführen von DES
- Kann mit zwei (2^112 verschiedene Schlüssel) oder mit drei (2^168 verschiedene Schlüssel) Schlüssel verwendet werden
- Wird von PGP verwenet

*Quelle: Kapitel 4, Seite 14*

##### AES
- Nachfolger von DES und Triple DES
- Symmetrische Blockverschlüsselung
- Sicher aufgrund der großen Schlüssel
- Für hohe Geschwindigkeit entworfen
- Einfache Algorithmen

*Quelle: Kapitel 4, Seite 15,17*

Als Blockchiffren (DES, AES, usw) stellen monoalphabetische Verschlüsselungen mit sehr großen Alphabeten (2^128 Zeichen bei AES und 2^64 Zeichen bei DES) da.

Wird der gleiche Klartext wiederholt chiffriert, so entsteht jeweils wieder derselbe verschlüsselte Text. Ein Angreifer kann dies ausnutzen, um die Verschlüsselung zu brechen.

*Quelle: Kapitel 5, Seite 2*

##### Electronic Code Book Mode

Es werden immer 8 Bytes (64 Bit) verschlüsselt (falls notwendig, wird aufgefüllt). Alles mit demselben Passwort. Es existiert kein Abhängigkeit zum vorangegangenen Block.

Die Reihenfolge chiffrierter Blöcke kann unbemerkt verändert und  neue Blöcke eingefügt werden.

*Quelle: Kapitel 5, Seite 5,6*

##### Cipher Block Chaining Mode

Um Attacken auf den "Electronic Code Book Mode" zu verhindern, muss die monoalphabetische Chiffrierung aufgehoben werden -> polyalphabetisch

Blöcke werden verkettet: Jeder Klartext-Block wird mit dem vorhergehenden verschlüsselten Block mit XOR verknüpft, bevor er selbst verschlüsselt wird.

Der erste Block wird mit einem IV verknüpft, der im Klartext gemeinsam mit dem verschlüsselte Text übertragen wird.

*Quelle: Kapitel 5, Seite 7*

##### Cipher Feedback Mode
- Byteweise Verschlüsselung (Stromchiffre), damit kein komplette Block gefüllt werden muss (anders wie beim Cipher Block Chaining Mode)
- Der IV wird in einem Schieberegister abgelegt. Dieses wird verschlüsselt (z.B. mit DES) und das linke Byte mit dem aktuellen Byte des Klartextes XOR verknüpft. Danach wird das linke Byte des Schieberegisters ans Ende des Registers geschoben.

*Quelle: Kapitel 5, Seite 9*

Störungen (Bit wird während der Übertragung invertiert) betreffen 8 Byte (also solange bis das fehlerhafte Bit das Schieberegister verlassen hat).

*Quelle: Kapitel 5, Seite 12*

Nachteil: Zeitverzögerung. Schlecht bei Streams, VoIP, Wlan. Dort ist es besser, wenn der Schlüssel vorab vorhanden ist.

##### Output Feedback Mode
- Einfluss von Übertragungsfehlern minimieren
- IV wird nur zum Start benötigt
- Der Keystream ist unabhängig von den Daten und kann daher im Voraus berechnet werden
- Übertragungsfehler wirken sich nur auf das entsprechende Bit aus, nicht auf andere
- Das gleiche Paar (Schüssel, IV) darf nicht zweimal mit dem gleichen verschlüsselten Text benutzt werden, weil sonst jeweils der gleiche Keystream erzeugt würde
- XOR von zwei Klartexten kann immer mit statistischen Methoden attackiert werden (siehe WEP)

*Quelle: Kapitel 5, Seite 13, 15*

##### Counter Mode

Alle Betriebsarten bis auf den "Electronic Code Book Mode" erlauben keinen wahlfreien Zugriff auf die verschlüsselten Daten  (da jeder Block vom Vorgänger abhängt).

Die Besonderheit des Counter Mode im Vergleich zu anderen Betriebsarten, stellt die Tatsache dar, dass der Initialisierungsvektor hier aus einer für jedes Chiffrat neu zu wählenden Zufallszahl (**Nonce**) verknüpft mit einem Zähler besteht, der mit jedem weiteren Block hochgezählt wird. Die Verknüpfung kann z.B. durch Kokatenation (Anhängen), Addition oder XOR erfolgen.

Counter Mode ist wie Output Feedback Mode ein Betriebsmodus, der es erlaubt, eine Blockchiffre als Stromchiffre zu betreiben. Die Vorteile des OFB-Modus gegenüber Cipher Block Chaining Mode, Cipher Feedback Mode und anderen Modi, welche klartextabhängige Daten für den nächsten Block weiterverwendeten, kommen auch hier zu tragen:

- Bitfehler bei der Übertragung ergeben Fehler bei nur den entsprechenden Bits des Klartextes (anstatt einen ganzen Block bzw. eventuell sogar einen weiteren Block unbrauchbar zu machen)
- Verschlüsselung und Entschlüsselung sind identisch, daher können hier auch Einwegfunktionen verwendet werden
- Der Schlüsselstrom kann auch vorausberechnet werden

Im Gegensatz zum OFB-Modus aber hängt der Schlüssel für einen Block nicht vom Schlüssel für den vorherigen Block ab, daher:

- hat man hier wahlfreien Zugriff auf jeden verschlüsselten Block und
- sämtliche Ver- und Entschlüsselungsoperationen können parallel durchgeführt werden.

*Quellen: Kapitel 5, Seite 16*

##### Integrität

Bezeichnet die Sicherstellung der Korrektheit (Unversehrtheit). Auf "Daten" angewandt bedeutet dies, dass die Daten vollständig und unverändert sind.

Eine Verschlüsselung von Daten sichert nicht deren Integrität. Verschiedene Angriffsarten können zu plausiblen Verfälschungen führen, die dem Empfänger nicht auffallen.

##### Authentizität

Mit dem Begriff Authentizität wird die Eigenschaft bezeichnet, die gewährleistet, dass ein Kommunikationspartner tatsächlich derjenige ist, der er vorgibt zu sein.

*Quelle: Kapitel 7, Seite 2*

##### Schutzziele
- Vertraulichkeit (erreicht durch eine Verschlüsselung)
- Authentizität (erreicht durch eine Signatur / MAC)
- Integrität (erreicht durch einen Fingerprint (z.B. SHA oder MD5))

*Quelle: Kapitel 7, Seite 3*

##### Kryptografische Hashfunktionen

Werden benötigt, um einen Fingerprint/Message Digest/Hash zu erzeugen

- Haben eine feste Länge (unabhängig von der Dokumentenlänge)
- Einwegeigenschaften (aus *h(m)*) kann nicht wieder *m* gemacht werden)
- Kollisionsfrei: Es muss praktisch unmöglich sein zwei Dokumente zu finden, die den gleichen Hash liefern
- SHA-1 erzeugt einen längeren Hashwert (160 Bit) wie MD5 (128 Bit)

*Quelle: Kapitel 7, Seite 8*

##### Iterative Hashfunktion

Die Eingabe (Message) wird in feste Blöcke aufgeteilt, die dann gehasht werden.

*Quelle: Kapitel 7, Seite 9*

Der von eine kryptografischen Hash-Funktion erzeugte Digest wird  oft als **Modifikation Detection Code (MDC)** bezeichnet. Während die Nachricht über einen unsicheren Kanal versendet werden kann, muss der MDC über einen sicheren Kanal transportiert werden.

*Quellen: Kapitel 7, Seite 23*

Ein Message Digest (= Fingerprint / Hash) garantiert nur die Integrität nicht die Authentizität eines Dokumentes. Es kann aber eine Geheimnis im Message Digest integriert werden. Dies nennt man dann **Message Authentication Code (MAC)** 

*Quelle: Kapitel 7, Seite 25*

##### Digitale Signatur

Zwei Ziele: Integrität und Authentizität sicherstellen!

Zwei Verfahren:

- Signatur durch zentrale Autorität (quasi ein Notar; erstellt eine digitale Signatur, die nur er selbst überprüfen kann) Siehe  *Kapitel 8, Seite 9,10*
- Signatur durch den Urheber (Herausgeber)

*Quelle: Kapitel 8, Seite 8*

Nachteile zentraler Autorität

- Jeder muss der zentralen Instanz vertrauen
- Die Zentrale Instanz kann alle Nachrichten lesen

*Quelle: Kapitel 8, Seite 11*

##### Signieren durch Autor
- Private & Public Key werden benötigt (asymmetrische Verschlüsselung)
- Daten die mit dem privaten Schlüssel verschlüsselt werden, werden mit dem public Key entschlüsselt und umgekehrt
- Der Sender verschlüsselt sein Plaintext mit seinem privaten Schlüssel. Damit es nur der Empfänger lesen kann, wird das Ergebnis der Verschlüsselung mit dem public Key des Senders verschlüsselt

*Quelle: Kapitel 8, Seite 11*

**Probleme:**

- Falls der private Schlüssel bekannt wird
- Schlüsselpaare werden periodisch gewechselt. Ein neuer public key kann nicht mehr auf alte Chiffrate angewandt werden

*Quelle: Kapitel 8, Seite 13*

Allein eine Signatur, die vom Autor erstellt wird, benötigt ein asymmetrischer Kryptosystem. Aber die Verschlüsselung des vollständigen Dokumentes mit dem privaten Schlüssel des Autors ist sehr aufwändig.

*Quelle: Kapitel 8, Seite 14*

**Digitale Signaturen unterstützen drei Sicherheitsziele:**

- Authentisieren von Nachrichten
- Nachrichtenintegrität
- Unwiederrufbarkeit

*Quelle: Kapitel 8, Seite 20*

**Authentifizierung** ist der Vorgang der Überprüfung einer behaupteten Identität

**Authentisierung** hingegen ist der Vorgang des Nachweises der eigenen Identität

*Quelle: Kapitel 10, Seite 2*

Symmetrische Schlüsselverteilung: **n * ( n - 1 ) / 2**

Symmetrische Schlüsselverteilung mit einer zentralen Stelle: **n-1**

**RSA** (**R**ivest, **S**hamir und **A**dleman) ist ein asymmetrisches kryptographisches Verfahren, das sowohl zur Verschlüsselung als auch zur digitalen Signatur verwendet werden kann.

**PGP** nutzt zum zertifizieren des public keys das sogenannte "Web of Trust" - Modell. In einer Gruppe kann jeder für jeden anderen in der Gruppe ein Zertifikat signieren.

*Quelle: Kapitel 12, Seite 14*

##### S/MIME
- Alternative zu PGP
- MIME = ermöglicht die Übertragung von binären Daten (in Emails)

Bei **Cross-Zertifikaten** zertifiziert jeder Root-CA jeden anderen Root-CA. Man braucht also **n * ( n - 1 ) / 2** Zertifikate

*Quelle: Kapitel 13, Seite 19*

**Sniffing** = schnüffeln; Software die einen Datenverkehr eines Netzwerkes empfangen, aufzeichnen, darstellen und ggfs. auswerten kann

**Spoofing** = Manipulation, Verschleierung oder Vortäuschen

##### SSL / TLS

Hängt zwischen TCP/UDP und der Anwendungsschicht. Es handelt sich um ein Anwendungsprotokoll

##### Handshake Protocol

Bereitet die Sicherheitseinstellungen für eine verbindungsorientierte Kommunikation vor. Dabei wird der Server authentisiert und optional der Client

##### Change Cipher Spec Protocol

Bereitet das Aushandeln der Sicherheitsparameter. Daten der Anwendung werden danach vom Record Protocol entsprechend der vereinbarten Sicherheitsvorgaben übertragen

##### Alert Protocol

Informiert über einen Fehler und abnormale Zustände

##### Record Protocol

Ist zuständig für die Übertragung aller SSL-Nachrichten

*Quelle: Kapitel 15, Seite 10*

Für SSL werden sechs kryptografische Geheimnisse benötigt: Vier Schlüssel und zwei Initialisierungsvektoren.

##### Aufgaben es Handshake Protocol
- Vereinbarung der kryptografischen Algorithmen: Client schlägt mehrere Ihm bekannte Verfahren vor, der Server wählt eines davon aus.
- Kryotografische Geheimnisse festlegen: Server senden ein Serverzertifikat. Der Client macht nun einen Vorschlag für einen Teil der Geheimnisse (Pre-Master-Secret) und sendet den Vorschlag verschlüsselt (mit dem public key aus dem Zertifikat) an der Server
- Mastersecret berechnen: Server und Client produzieren unabhängig voneinander ein "Mastersecret". Aus diesem werden die benötigten Geheimnisse herausgeschnitten

Ein **Keyed-Hash Message Authentication Code (HMAC)** ist eine Art Message Authentication Code (MAC), dessen Konstruktion auf einer kryptografischen Hash-Funktion basiert.

Im Protokoll Transport Layer Security (TLS) legt die **Cipher Suite** fest, welch Algorithmen zum Aufbau einer Datenverbindung verwendet werden sollen. Dabei identifiziert jede Cipher Suite eine Kombination aus vier Algorithmen:

- Schlüsselaustausch (RSA, DH)
- Authentifizierung (RSA, DSA)
- Hashfunktion (MD5, SHA)
- Verschlüsselung (keine, RC4, DES, 3DES, IDEA, AES)

**F**: Erst verschlüsseln und dann komprimieren oder umgekehrt?

**A**: Erst komprimieren, dann verschlüsseln. Nach einer Verschlüsselung ist die Entropie maximal, und keine Kompression mehr möglich.

Nachteil von asymmetrischen Verschlüsselungen: langsam, daher liegt der Verwendungszweck beim erstellen von digitalen Signaturen und dem sicheren Übertragen von symmetrischen Schlüsseln.

Eine Variante der Einwegfunktionen sind **Trapdoor-Einwegfunktionen**, auch Falltürfunktionen genannt. Diese lassen sich nur dann effizient umkehren, wenn man eine gewisse Zusatzinformation besitzt. Falltürfunktionen werden in asymmetrischen Verschlüsselungsverfahren wie zum Beispiel RSA verwendet. Eine schöne Metapher für Falltürfunktionen ist die Funktion eines Briefkastens: Jeder kann einen Brief einwerfen. Das Herausholen ist dagegen schwierig - es sei denn, man ist im Besitz des Schlüssels.

##### DNSSEC

Die Domain Name Security Extensions (DNSSEC) ist eine Menge von Erweiterungen des DNS, die Authentizität und Datenintegrität von DNS-Transaktionen gewährleisten.

Sicherheitsziele:

- Authentisieren des Servers (abfragen des Geheimnisses)
- Sicherung der Datenintegrität

Probleme:

- Zertifikate sind teuer und müssen regelmäßig erneuert werden
- Schutz der privaten Schlüssel
- Signieren großer Datenbestände ist aufwendig

**F**: Wann setze man MAC ein, und wann eine digitale Signatur?

**A**: MAC wird eingesetzt, wenn zwischen zwei Partnern ein Austausch stattfinden soll. Eine digitale Signatur wird verwendet, wenn mit mehreren Empfängern kommunizert werden soll und die Authentifizierung wichtig ist. Eine Authentifizierung lässt sich mit MAC nur über einen vertrauenswürdigen Dritten realisieren.

**Symmetrische Verfahren** verwenden logische Operationen.

**Asymmetrische Verfahren** verwenden **langsame** arithmetische Operationen.

**F**: Wie überprüft man ein Serverzertifikat?

**A**: Man verschlüsselt das Pre-Master-Secret (PM) mit dem public key aus dem Serverzertifikat: EB(PM).

Nur wenn der Server der Eigentümer des Zertifikates ist, besitzt er den privaten Schlüssel um das Pre-Master-Secret zu entschlüsseln. DB(EB(PM)). Kennt er den private Schlüssel nicht, errechnet er ein falsches Mastersecret und die weitere Kommunikation schlägt fehl.

**F**: Wie unterscheiden sich die Zertifikatskonzepte von PGP und SMIME?

**A**: SMIME verwendet eine hierarchische Struktur (Zertifikatskette). PGP eine flache Ebene ("Web of Trust").
 

