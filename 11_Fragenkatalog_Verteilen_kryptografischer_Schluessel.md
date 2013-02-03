# 10 Verteilen kryptografischer Schlüssel

##### In manchen Organisationseinheiten werden Key Distribution Center (KDC) eingesetzt

- a) Welche Aufgabe hat ein KDC

- b) Erläutern Sie die Vorteile, die sich aus der Einführung eines KDC ergeben

- c) Beschreiben Sie die Kommunikation zwischen einen Benutzer und einem KDC

##### Das auf Folie 7 dargestellte Protokoll überträgt in Nachricht 1 die Identität Alice im Klartext. Warum wird Alice nicht ebenso wie der Session Key verschlüsselt?,

##### Das KDC-Protokoll soll gegen die auf Folie 9 dargestellte Replay-Attacken geschützt werden. Schlagen Sie geeignete Maßnahmen vor

##### Protokolle zur Authentikation vereinbaren oder verhandeln auch Session Keys zwischen den Kommunikationspartnern. Warum werden jeweils neue Session Keys generiert und nicht die für die Autentisierung eingesetzen Schlüssel auch für die nachfolgende Kommunikation zwischen den Partnern benutzt?

##### Bei Kerberos werden sogenannte Tickets verwendet. Erläutern Sie den Begriff!

##### In Nachricht 2 des Needham-Schroeder-Authentifizierungsprotokolls (authentication protocol) wird das (bereits verschlüsselte) Ticket unter Verwendung des geheimen Schlüssels verschlüsselt, der von Alice und dem KDC gemeinsam genutzt wird. Ist diese zusätzliche Verschlüsselung erforderlich?"

##### Im Needham-Schroeder-Protokoll (Folie 12) erzeugt Alice zwei Zahlen, Ra und Ra2 um Ihren Partner zu authentisieren. Würde es nicht reichen, nur eine Zahl Ra zu verwenden?

##### Welche Vorteile und Nachteile sind mit der Verwendung von Nonces verbunden?

##### Nehmen Sie an, eine Organisation verwendet Kerberos (Folien 15,16) zur Autentisierung. Wie sicher und zuverlässig ist das System in Bezug auf einen Ausfall von AS oder TGS?

##### Überlegen Sie ein Verfahren um die in Folie 25 beschriebene Man-In-The-Middle-Attack zu verhindern?

##### Folie 28 zeigt den (von Trudy sabotierten) Versuch von Alice, Bobs öffentlichen Schlüssel zu erhalten. Angenommen, Alice und Bob verfügen über einen gemeinsamen, geheimen Schlüssel und Alice braucht immer noch Bobs öffentlichen Schlüssel. Gibt es dann eine Möglichkeit, diesen auf sichere Weise zu bekommen?  

##### Was wird mit der Vorlage eines Zertifikats bewiesen?