# 01 Einführung zum Thema Sicherheit und Netze

##### Nennen Sie jeweils ein Beispiel für eine passive und ein aktive Attacke auf ein Netzwerk!

- Bei einer **passiven Attacke** wird der Datenverkehr abgehört
- Bei einer **aktiven Attacke** wird der Datenverkehr verändert

##### Wie unterscheiden sich Kryptografie und Stenografie?

- Bei der **Kryptografie** wird die Nachricht durch Verschlüsselung verschleiert.

- Bei der **Steganografie** wird die Nachricht durch eine andere Nachricht verborgen, z. B. ein durch ein Bild.

##### Welche Typen von Sicherheitsdiensten greifen in den folgenden Fällen?

- a) Ein Unternehmen verlangt eine Identifikation und ein 	Passwort, um sich an dem Unternehmensserver anzumelden
	
- b) Der Unternehmensserver verwehrt jedem den Zugriff, der länger als zwei Stunden angemeldet ist

- c) Bestellungen werden nur dann akzeptiert, wenn der Besteller eine Identifikation vorweist, die vorher vom Unternehmen zugewiesen wurde.

- d) Eine Bank verlangt die Unterschrift des Kunden, wenn er von seinem Konto einen Geldbetrag abheben möchte
 
##### Welche Taktik (Kryptografie, Stenografie) wird in den folgenden Fällen verwendet, um Informationen zu verbergen

- a) Ein Student schreibt die Antworten zu einer Klausur auf ein kleines Stück Papier, rollt dieses zusammen, steckt es in einen Kugelschreiber und gibt diesen weiter an seinen Nachbarn
			
	-- **Steganografie**

- b) Um eine Nachricht weiterzugeben, ersetzt ein Spion jedes Zeichen der Nachricht durch ein vorher als Zeichenersatz vereinbartes Symbol.

	-- **Kryptografie**

- c) Ein Unternehmen verwendet spezielle Tinte für Ihre Schecks, um Fälschungen zu verhindern.

	-- **Kryptografie**

- d) Ein grafisches Unternehmen verwendet Wasserzeichen, um die Grafiken ihrer Website zu schützen

	-- **Steganografie**

##### Welcher Typ von Sicherheitsmechanismus wird verwendet, wenn eine Person das Formblatt unterschreibt, mit dem eine Kreditkarte beantragt wird?

- Es wird der Sicherheitsmechanismus der **Signatur** verwendet.

##### Erläutern Sie anhand eines Beispiels die Bedeutung des Sicherheitsziels Unwiederrufbarkeit!

- Durch die Unwiederrufbarkeit, werden Banküberweisungen gesichert, die nur einmal ausgeführt werden dürfen.

##### Ist die Authentisierung von Dokumenten oder eines Kommunikationspartners unbedingt notwendig oder würde auch allein Geheimhaltung (Verschlüsselung) für ausreichende Sicherheit sorgen?

- Alleine durch die Verschlüsselung wird die Authentizität  			der Teilnehmer nicht sicher gestellt

##### Warum lassen sich Papierdokumente leichter auf Echtheit überprüfen als elektronische Dokumente?

- Weil das Medium Papier mit einer Handschriftlichen Unterschrift sehr schwer zu kopieren ist.

##### Wo liegen die Sicherheitslücken, wenn Daten auf der Schicht 2 verschlüsselt werden?

- Auf Schicht 2 können die Daten aufgrund der Adressierung des ARP Protokolls leicht verändert werden, das ARP Protokoll nimmt Response Pakete an obwohl kein Request gestellt wurde

##### Wie kann man das ARP-Spoofing verhindern? Welchen Einfluss hat das eingesetzte Netzwerkprotokoll?

- Das ARP Protokoll darf nur Response Pakete annehmen, wenn es einen Request gestellt hat.

  
