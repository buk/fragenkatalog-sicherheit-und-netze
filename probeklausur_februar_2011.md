# Probeklausur Sicherheit und Netze Februar 2011

### Aufgabe 1: Kryptografische Grundlagen

##### a) Bei symmetrischen Chiffren wird zum Dechiffrieren im Prinzip die Umkehrfunktion derjenigen Funktion verwendet, die zum Chiffrieren benutzt wurde. Welche Umkehrfunktion wird benutzt, wenn zum Chiffrieren die Funktion XOR verwendet wurde?

##### b) Erläutern Sie den Unterschied zwischen einer monoalphabetischen und einer polyalphabetischen Chiffre! Welche Art von Angriffen hat zur Idee polyalphabetischer Chiffren geführt?

##### c) Ein Unternehmen verfügt über *n* Mitarbeiter (inkl. Chef). Jeder Mitarbeiter soll mit jedem anderen vertraulich mit Hilfe eines symmetrischen Verschlüsselungsverfahrens kommunizieren können. Wie viele geheime Schlüssel werden gebraucht?

##### d) Wie viele geheime Schlüssel werden gebraucht, wenn alle dem Chef vertrauen? Will ein Mitarbeiter in diesem Fall einem anderen eine Nachricht schicken, dann sendet er diese zunächst an den Chef, dieser sendet die Nachricht danach an den gewünschten Mitarbeiter.

##### e) In der Kryptografie ist die Aktualität von Nachrichten von Bedeutung. Erläutern Sie, warum Aktualität eine wichtige Rolle spielt und auf welche Weise die Aktualität einer Nachricht gewährleistet wird!

##### f) Warum fordert man bei der Verschlüsselung eine Redundanz der Daten?

### Aufgabe 2: Symmetrische Kryptosysteme

##### a) Warum sind moderne Blockchiffren im Kern Substitutionschiffren und keine Transpositionschiffren?

##### b) Was bedeutet der Begriff *Block* bei eiber Blockchiffre?

##### c) Welches Problem entsteht beim Einsatz von Blockchiffren? Für welche Art von Attacken sind diese besonders anfällig?

##### d) sind *One-Time-Pads* Blockchiffren oder Stromchiffren? Begründen Sie Ihre Antwort!

##### e) Erläutern Sie den Begriff *Electronic Code Book Mode*

##### f) Wie überwindet man die Nachteile des ECB Modes?

##### g) Wann setzt man den sogenannten Counter Mode ein?

### Aufgabe 3: Asymmetrische Kryptosysteme

##### a) Vergleichen Sie symmtrische und asymmetrische Kryptosysteme. Welche Unterschiede gibt es in Bezug auf Schlüsselaustausch und Schlüsselverwaltung?

##### b) Wie unterscheiden sich die beiden Verfahren in Bezug auf die Verschlüsselungsgeschwindigkeit (d.H. Bit/s)?

##### c) Warum gibt es einen Unterschied in der Verschlüsselungsleistung?

##### d) Maria entdeckt, dass Ihr privater RSA-Schlüssel (d,n) der gleiche ist wie der öffentliche RSA-Schlüssel (e,n) eines anderen Benuzers Franz. Soll nun Maria Ihr Schlüsselpaar wechseln? Begründen Sie Ihre Antwort.

### Aufgabe 4: Integrität und Authentizität

##### a) Erklären Sie die Begriffe Integrität und Authentizität in bezug auf elektronische Dokumente

##### b) Wieso kann man mit einem Fingerprint (elektronischer Fingerabdruck) Integrität und Autentizität eines Dokumentes bzw. einer Nachricht sicherstellen?

##### c) Welche besondere Anforderung wird an Algorithmen gestellt, mit denen Fingerprints bestimmt werden?

##### e) Aus welchem Grund besteht bei einer digitalen Signatur ein logischer Zusammenhang zwischen Dokument und Signatur? Wie entsteht dieser logische Zusammenhang?

##### f) Ein Dilletant kopiert eine existierende digitale Signatur von Alice und veröffentlicht diese zusammen mit einem gefälschtem Dokument, als dessen Herausgeber er Alice benennt. Erläutern Sie den Prozess, mit dem die Fälschung erkannt wird.

### Aufgabe 5: Instanzenautentisierung

##### a) Bei einer Autentisierung von Dokumenten werden zusätzliche Informationen erzeugt, die im Zusammenhang mit dem jeweilligen Dokument stehen. Bei der Autentisierung von Kommunikationspartnern werden dagegen Protokolle verwendet. Aus welchen Gründen sind diese beiden Konzepte zur Autentisierung unterschiedlich?

##### b) Welche grundlegende Idee steht hinter dem Challenge-Response Verfahren?

### Aufgabe 6: Verwaltung und Verteilung kryptografischer Schlüssel

##### a) Kryptografische Schlüssel werden für symmetrische und asymmetrische Chiffren benötigt. Erläutern Sie, worin die Unterschiede bei der Verwaltung und Verteilung von Schlüsseln abhängig vom jeweiligen Chiffretyp bestehen

##### b) Schlüssel werden verwendet zum Autentisieren von Dokumenten und Kommunikationspartnern, aber auch zum Verschlüsseln von Dokumenten bzw. Nachrichten. Warum werden dafür unterschiedliche Schlüsseltypen verwendet?