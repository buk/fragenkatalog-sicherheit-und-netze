# Probeklausur Sicherheit und Netze Februar 2012

### Aufgabe 1: Grundlegende Konzepte

##### a) Welche Eigenschaft besitzt ein Kryptosystem, wenn es symmetrisch genannt wird?

##### b) Welches Verfahren ist besser zum Chiffrieren geeignet, Substitution oder Transposition? Wann hat ein Angreifer den größeren Aufwand?

##### c) Erläutern Sie den Unterschied zwischen einer monoalphabetischen und einer polyalphabetischen Chiffre! Welche Art von Angriffen wird mit einer polyalphabetischen Chiffren wesentlich erschwert?

##### d) Weshalb ist es wichtig, zu verschlüsselnde Daten mit Redundanz zu versehen? Wie lässt sich zusätzliche Redundanz erzeugen?

##### e) In der Kryptografie ist die Aktualität von Nachrichten von besonderer Bedeutung. Erläutern Sie, warum Aktualität wichtig ist und auf welche Weise die Aktualität einer Nachricht gewährleistet werden kann!

### Aufgabe 2: Vertrauliche Kommunikation im Verein

#### Ein Verein verfügt über n Mitglieder inkl. Vorstand. Die Vorstandsschaft möchte eine vertrauliche elektronische Kommunikation einrichten. Helfen Sie die folgenden Fragen zu klären.

##### a) Wie viele geheime Schlüssel werden benötigt, damit jedes Vereinsmitglied jedem anderen geheime Nachrichten zusenden kann?

##### b) Alle Mitglieder sollen dem Vorsitzenden des Vereins vertrauen. Wenn ein Vereinsmitglied einem anderen eine Nachricht senden möchte, dann sendet es diese Nachricht zunächst an den Vorsitzenden; der Vorsitzende sendet danach die Nachricht weiter an das gewünschte Mitglied. Wie viele geheime Schlüssel werden in diesem Fall benötigt?

##### c) Wie viele geheime Schlüssel werden benötigt, wenn ein Mitglied, das mit einem anderen kommunizieren will, zunächst den Vorsitzenden kontaktieren muss, um einen temporären Sitzungsschlüssel zu erhalten? Der Vorsitzende erzeugt den temporären Schlüssel und sendet diesen den beiden Mitgliedern chiffriert zu. Welche Schlüssel werden zum Chiffrieren des temporären Schlüssels benutzt?

### Aufgabe 3: Symmetrische Kryptosysteme

##### a) Bei modernen symmetrischen Chiffren wird zum Dechiffrieren im Prinzip die Umkehrfunktion derjenigen Funktion verwendet, die zum Chiffrieren benutzt wurde. Welche Funktion wird benutzt, wenn zum Chiffrieren die Funktion XOR verwendet wurde?

##### b) Welche Schwachstelle besitzt der Electronic Code Book Mode Für welche Attacke ist er besonders anfällig?

##### c) Der CBC Mode überwindet die Nachteile des ECB Modes. Was ist der Grund dafür?

##### d) Wann setzt man den sogenannten Counter Mode Code ein?

##### e) Sind One-Time-Pads Blockchiffren oder Stromchiffren? Begründen Sie die Antwort

### Aufgabe 4: Asymmetrische Kryptosysteme

##### a) Vergleichen Sie symmetrische und asymmetrische Kryptosysteme. Welche Unterschiede gibt es im Aufwand für die Schlüsselverteilung?

##### b) Wie unterscheiden sich die beiden Verfahren in Bezug auf die Verschlüsselungsgeschwindigkeit (d.H. Bit/s)?

##### c) Warum gibt es einen Unterschied in der Verschlüsselungsgeschwindigkeit?

##### d) Maria entdeckt dass Ihr privater RSA-Schlüssel (d,n) der gleiche ist, wie der öffentliche RSA-Schlüssel (e,n) eines anderen Benutzers Franz. Soll nun Maria Ihr Schlüsselpaar wechseln?

### Aufgabe 5: Integrität und Authentizität

##### a) Ein Fingerprint (elektronischer Fingerabdruck) wird benutzt um Integrität und Authentizität eines Dokuments bzw. einer Nachricht sicherzustellen. Welche Eigenschaft muss ein Verfahren für die Erstellung von Fingerrings besitzen, damit es tatsächlich die gewünschte Sicherheit liefert?
 
##### b) Wie wird die Integrität eines Dokuments überprüft wenn ein Fingerring benutzt wird? Erläutern Sie die notwendigen Prozessschritte. Welches Problem entsteht, wenn Dokument und Fingerprint gemeinsam versandt werden?

##### c) Wie unterscheiden sich Fingerprint und digitale Signatur? Welchen Fortschritt liefert eine digitale Signatur?

##### d) Vergleichen Sie die *Message Authentication Code* und digitale Signatur in Bezug auf den Verwendungszweck. Wann wird man sich für das eine und wann für das andere Verfahren entscheiden?

### Aufgabe 6: Instanzenauthentisierung

##### a) Zur Authentisierung eines Kommunikationspartners werden verschiedene Protokolle verwendet. Häufig wird ein Challenge-Response Verfahren benutzt. Welcher Vorteil besteht dabei gegenüber einer Authentisierung mittels Passwort?

