# 02 Konzepte und Begriffe traditioneller Chiffrierung

##### Welche Eigenschaften besitzt ein Kryptosystem, wenn es symmetrisch genannt wird?

- Wenn ein Kryptosystem die Eigenschaft besitzt *symmetrisch* zu sein, wird zum Ver- und Entschlüsseln der gleiche Schlüssel benutzt.

##### Bei modernen symmetrischen Chiffren wird zum Dechiffrieren im Prinzip die Umkehrfunktion derjenigen Funktion verwendet, die zum Chiffrieren benutzt wurde. Welche Umkehrfunktion wird benutzt, wenn zum Chiffrieren XOR verwendet wurde?

- Die Umkehrfunktion der Funktion *XOR* ist **XOR**

##### Welches Verfahren ist besser zum Chiffrieren geeignet, Substitution oder Transposition?

- Die **Substitution** ist zum Chiffrieren besser geeignet, da hier ein Zeichen durch ein anderes **ersetzt** wird. Bei der Transposition werden die Zeichen nur vertauscht. 

##### Erläutern Sie den Unterschied zwischen einer monoalphabetischen und einer polyalphabetischen Chiffre! Welche Art von Angriffen wird mit einer polyalphabetischen wesentlich erschwert?

- Bei *Monoalphabetischen Chiffren* wird ein Zeichen immer mit genau einem anderen ersetzt, bei *Polyalphabetischen Chiffren* wird ein Zeichen immer durch ein anderes Zeichen ersetzt, da der Schlüsselstrom das *i-te* Zeichen verschlüsselt und daraus ein weiteres Zeichen erzeugt.

##### Archäologen fanden eine Steintafel mit einer Inschrift in unbekannter Sprache. Später fanden die Archäologen an der selben Stelle eine Wand mit einem Satz in der unbekannten Sprache und der griechischen Übersetzung. Mithilfe der Wandgravur konnte die Steintafel entziffert werden. Welchen Typ von Entschlüsselungsverfahren benutzten die Archäologen?

- Die Archäologen benutzen hier das *Monoalphabetische Entschlüsselungsverfahren*.

##### Alice kann auf Ihrem Rechner nur eine additive Chiffre benutzen. Sie denkt, dass Ihre Nachrichten sicherer übertragen werden, wenn Sie zweimal verschlüsselt, jedes mal mit einem anderen Schlüssel. Wie ist diese Idee zu beurteilen?

- Eine *additive Chiffre* ist eine *Monoalphabetische Chiffre* oder auch *Cäsar-Chiffre* genannt. Hier werden die Zeichen **nur ausgetauscht**. Da **immer** die gleichen Zeichen ausgetauscht werden, macht eine zweite Verschlüsselung **keinen Sinn** 


##### Alice möchte eine seht umfangreiche Nachricht versenden. Sie benutzt eine monoalphabetische Substitutionschiffre. Sie denkt, wenn Sie die Nachricht komprimiert, könne Sie den Text vor einer Häufgkeitsanalyse schützen. Hilfe ein Kompression? Soll die Nachricht vor oder nach der Verschlüsselung komprimiert werden? 

- Ja. Ein Kompression macht Sinn, dadurch wird eine **maximale Entropie** erreicht.

##### Folie 21 zeigt die Realisierung einer polyalphabetischen Chiffre. Macht es einen Unterschied, wenn zum Verschlüsseln von Pn statt Pn-1 der Wert von Cn-1 verwendet wird?

##### Warum werden kryptographische Methoden mit Schlüsseln parametrisiert?


##### Weshalb ist es wichtig, zu verschlüsselnde Daten mit Redundanz zu versehen? Wie lässt sich zusätzliche Redundanz erzeugen?

- Durch Redundanzen werden die Nachrichten mit weiteren Informationen versehen um eine Modifikation eines Angreifers zu erkennen. Ein Zeitstempel eignet sich sehr gut für eine Redundanz.

##### In der Kryptografie ist die Aktualität von Nachrichten von Bedeutung. Erläutern Sie, warum Aktualität eine wichtige Rolle spielt und auf welche Weise Aktualität einer Nachricht gewährleistet wird!

- Durch die Aktualität kann durch einen Zeitstempel bestimmt werden, ob die Nachricht noch gültig ist. 

