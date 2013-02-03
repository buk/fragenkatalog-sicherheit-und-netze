# Probeklausur Sicherheit und Netze Februar 2012

### Aufgabe 1: Grundlegende Konzepte

##### a) Welche Eigenschaft besitzt ein Kryptosystem, wenn es symmetrisch genannt wird?

- Ein Kryptosystem hat dann die Eigenschaft *symmetrisch*, wenn mit dem gleichen Schlüssel **Ver-** und **Entschlüsselt** wird.

##### b) Welches Verfahren ist besser zum Chiffrieren geeignet, Substitution oder Transposition? Wann hat ein Angreifer den größeren Aufwand?

- Die **Substitution** ist besser zum verschlüsseln geeignet, da bei diesem Verfahren die Symbole durch andere Symbole ersetzt werden. Bei der *Transposition* wird lediglich die Position der Symbole vertauscht. Der Aufwand bei der Transposition ist somit geringer, da alle Symbole bereits bekannt sind.

##### c) Erläutern Sie den Unterschied zwischen einer monoalphabetischen und einer polyalphabetischen Chiffre! Welche Art von Angriffen wird mit einer polyalphabetischen Chiffren wesentlich erschwert?

- Bei einer monoalphabetischen Chiffre wird ein Symbol immer durch dasselbe Symbol ersetzt. Wenn z. B. nur das *a* durch ein *z* (und umgekehrt) ersetzt werden würde, dann wird aus *abba* -> *zbbz*. Ein Angreifer kann mittels statistischer Analyse das Chiffrat entschlüsseln. Bei einer polyalphabetischen Chiffre wird jedes Symbol abhängig von seiner Position durch ein anderes Zeichen ersetzt. Das bedeutet, *a* würde nicht immer durch ein *z* ersetzt werden.

##### d) Weshalb ist es wichtig, zu verschlüsselnde Daten mit Redundanz zu versehen? Wie lässt sich zusätzliche Redundanz erzeugen?

- Damit ein Angreifer keine Manipulationen (auch ohne Kentnisse der Nachricht) in der Chiffre vornehmen kann, die dann als gültig interpretiert werden. Bei Redundanzen werden zusätzliche (geheime) Informationen ergänzt.

##### e) In der Kryptografie ist die Aktualität von Nachrichten von besonderer Bedeutung. Erläutern Sie, warum Aktualität wichtig ist und auf welche Weise die Aktualität einer Nachricht gewährleistet werden kann!

- Die Aktualität ist wichtig, um sogenannte *replay Attacken* zu vermeiden. Die Aktualität wird durch einen Zeitstempel erreicht. Damit während dieser Zeitspanne keine unzulässige Wiederholung stattfindet, wird zusätzlich noch eine Kennung mitgegeben, die im Gültigkeitszeitraum nicht erneut auftreten darf.

### Aufgabe 2: Vertrauliche Kommunikation im Verein

#### Ein Verein verfügt über n Mitglieder inkl. Vorstand. Die Vorstandsschaft möchte eine vertrauliche elektronische Kommunikation einrichten. Helfen Sie die folgenden Fragen zu klären.

##### a) Wie viele geheime Schlüssel werden benötigt, damit jedes Vereinsmitglied jedem anderen geheime Nachrichten zusenden kann?

- Die Anzahl der geheimen Schlüssel berechnet sich wie folgt: **n * (n - 1) / 2**

##### b) Alle Mitglieder sollen dem Vorsitzenden des Vereins vertrauen. Wenn ein Vereinsmitglied einem anderen eine Nachricht senden möchte, dann sendet es diese Nachricht zunächst an den Vorsitzenden; der Vorsitzende sendet danach die Nachricht weiter an das gewünschte Mitglied. Wie viele geheime Schlüssel werden in diesem Fall benötigt?

- Es werden nach wie vor **n-1** Schlüssel benötigt.

##### c) Wie viele geheime Schlüssel werden benötigt, wenn ein Mitglied, das mit einem anderen kommunizieren will, zunächst den Vorsitzenden kontaktieren muss, um einen temporären Sitzungsschlüssel zu erhalten? Der Vorsitzende erzeugt den temporären Schlüssel und sendet diesen den beiden Mitgliedern chiffriert zu. Welche Schlüssel werden zum Chiffrieren des temporären Schlüssels benutzt?

- Es werden nach wie vor **n-1** Schlüssel benötigt. Zum verschlüsseln des temporären Schlüssels werden die gemeinsamen Geheimnisse zwischen dem Vorstand und den Mitgliedern verwendet.

### Aufgabe 3: Symmetrische Kryptosysteme

##### a) Bei modernen symmetrischen Chiffren wird zum Dechiffrieren im Prinzip die Umkehrfunktion derjenigen Funktion verwendet, die zum Chiffrieren benutzt wurde. Welche Funktion wird benutzt, wenn zum Chiffrieren die Funktion XOR verwendet wurde?

- Die Umkehrfunktion von **XOR** ist **XOR**

##### b) Welche Schwachstelle besitzt der Electronic Code Book Mode Für welche Attacke ist er besonders anfällig?

- Die Reihenfolge chiffrierter Blöcke kann unbemerkt verändert und neue Blöcke eingefügt werden. Kapitel 5, Seite 5,6

##### c) Der CBC Mode überwindet die Nachteile des ECB Modes. Was ist der Grund dafür?

- Im *Cipher Block Changing (CBC) Mode* werden die einzelnen Blöcke miteinander verbunden. D. h. jeder Block ist abhängig vom vorhergehenden. Dadurch entsteht eine *polyalphabetische* Chiffre.

##### d) Wann setzt man den sogenannten Counter Mode Code ein?

- Den Counter Mode setzt man ein, wenn man einen wahlfreien Zugriff auf die Blöcke des Chiffrates benötigt.

##### e) Sind One-Time-Pads Blockchiffren oder Stromchiffren? Begründen Sie die Antwort

- Es handelt sich dabei um Stromchiffren, da **bitweise Ver- und Entschlüsselt** wird.

### Aufgabe 4: Asymmetrische Kryptosysteme

##### a) Vergleichen Sie symmetrische und asymmetrische Kryptosysteme. Welche Unterschiede gibt es im Aufwand für die Schlüsselverteilung?

- In symmetrischen Systemen wird ein Schlüssel zum ver- und entschlüsseln verwedet. Dieser muss über einen sicheren Kanal übertragen werden. Für die Kommunikation mit mehreren Partnern empfiehlt es sich ein *Trust Center* (eine zentrale Stelle der jeder vertraut) einzurichten, die dann Sessionkeys generiert. Ansonsten wäre der Aufwand für die Verteilung sehr groß.

- Bei asymmetrischen Systemem gibt es ein Schlüsselpaar (public und private key). Der öffentliche Schlüssel kann auch über unsichere Wege verteilt werden, da man nur mit einem Key nicht gleichzeitig ver- und entschlüsseln kann.

##### b) Wie unterscheiden sich die beiden Verfahren in Bezug auf die Verschlüsselungsgeschwindigkeit (d.H. Bit/s)?

- Symmetrische Verfahren sind wesentlich schneller, da hier nur logische Operationen eingesetzt werden.

##### c) Warum gibt es einen Unterschied in der Verschlüsselungsgeschwindigkeit?

- Bei asymmetrischen Systemen werden arithmetische Operationen eingesetzt, die im Vergleich zu den logischen Operatoren langsamer sind.

##### d) Maria entdeckt dass Ihr privater RSA-Schlüssel (d,n) der gleiche ist, wie der öffentliche RSA-Schlüssel (e,n) eines anderen Benutzers Franz. Soll nun Maria Ihr Schlüsselpaar wechseln?

- Maria sollte auf jeden Fall Ihr Schlüsselpaar wechseln. Denn dies bedeutet, dass Ihr öffentlicher Schlüssel mit dem privaten Schlüssel von Franz identisch ist. Somit ist keine Vertraulichkeit mehr gewährleistet, da Franz Nachrichten von und für Maria ver- und entschlüsseln kann (und umgekehrt).

### Aufgabe 5: Integrität und Authentizität

##### a) Ein Fingerprint (elektronischer Fingerabdruck) wird benutzt um Integrität und Authentizität eines Dokuments bzw. einer Nachricht sicherzustellen. Welche Eigenschaft muss ein Verfahren für die Erstellung von Fingerrings besitzen, damit es tatsächlich die gewünschte Sicherheit liefert?

- Ein Fingerprint sichert zunächst einmal nur die Integrität eines Dokumentes bzw. einer Nachricht. Erst durch die Verschlüsselung (MAC oder digitale Signaur) des Fingerprints wird auch die Authentizität gewährleistet.
 
##### b) Wie wird die Integrität eines Dokuments überprüft wenn ein Fingerprint benutzt wird? Erläutern Sie die notwendigen Prozessschritte. Welches Problem entsteht, wenn Dokument und Fingerprint gemeinsam versandt werden?

- Der Empfänger erzeugt vom empfangenen Dokument ebenfalls einen Fingerprint (Hash/Digest) und vergleicht diesen mit dem übermittelnden Fingerprint. Sind beide identisch, ist das Dokument unverändert und vollständig. 

- Wird der Fingerprint (ohne entsprechende Verschlüsselung durch MAC oder einer digitalen Signatur) mit dem Dokument zusammen übertragen, könnte ein Angreifer Dokument und Fingerprint austauschen.

##### c) Wie unterscheiden sich Fingerprint und digitale Signatur? Welchen Fortschritt liefert eine digitale Signatur?

- Ein Fingerprint gewährleistet nur die Integrität eines Dokumentes bzw. einer Nachricht. Durch die digitale Signatur (verschlüsselt den Fingerprint) erreicht man das Schutzziel der Authentizität (der Fingerprint wird mit dem privaten Schlüssel des Sender verschlüsselt und kann mit dessen öffentlichen Schlüssel wieder entschlüsselt werden). Dadurch isr es auch möglich den Fingerprint zusammen mit dem Dokument zu übertragen.

##### d) Vergleichen Sie die *Message Authentication Code* und digitale Signatur in Bezug auf den Verwendungszweck. Wann wird man sich für das eine und wann für das andere Verfahren entscheiden?

- MAC (gemeinsames Geheimnis) wird verwendet wenn zwei Kommunikationspartner miteinander kommunizieren wollen. Wenn die Kommunikation mit mehreren Kommunikationspartnern stattfindet und die Authentizität gewährleistet werden soll, verwendet man die digitale Signatur, da dort die Verteilung der Schlüssel einfacher ist.

### Aufgabe 6: Instanzenauthentisierung

##### a) Zur Authentisierung eines Kommunikationspartners werden verschiedene Protokolle verwendet. Häufig wird ein Challenge-Response Verfahren benutzt. Welcher Vorteil besteht dabei gegenüber einer Authentisierung mittels Passwort?

- Beim *Challenge-Response* Verfahren wird die Authentizität geprüft ohne dass das Geheimnis preisgegeben wird.

