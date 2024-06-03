---
title: Stil
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/style/
description: "Aspose.Cells Cloud-Modellspezifikation: Stil. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Stil
weight: 50
---
## **Stil**

 Stellt den Anzeigestil des Excel-Dokuments dar, beispielsweise Schriftart, Farbe, Ausrichtung, Rahmen usw. Das Style-Objekt enthält alle Stilattribute (Schriftart, Zahlenformat, Ausrichtung usw.) als Eigenschaften.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Schriftart| Klasse:Schriftart| WAHR| FALSCH|| Ruft ein Objekt ab.|
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen des Stils ab oder legt ihn fest.|
| KulturBrauch| Zeichenfolge| WAHR| FALSCH|| Ruft die kulturabhängige Musterzeichenfolge für das Zahlenformat ab und legt sie fest. Wenn für dieses Objekt kein Zahlenformat festgelegt wurde, wird null zurückgegeben. Wenn das Zahlenformat integriert ist, wird die Musterzeichenfolge zurückgegeben, die der integrierten Zahl entspricht.|
| Brauch| Zeichenfolge| WAHR| FALSCH|| Stellt die benutzerdefinierte Zahlenformatzeichenfolge dieses Stilobjekts dar. Wenn das benutzerdefinierte Zahlenformat nicht festgelegt ist (z. B. wenn das Zahlenformat integriert ist), wird „“ zurückgegeben.|
| Hintergrundfarbe| Klasse:Farbe| WAHR| FALSCH|| Ruft die Hintergrundfarbe eines Stils ab oder legt sie fest.|
| Vordergrundfarbe| Klasse:Farbe| WAHR| FALSCH|| Ruft die Vordergrundfarbe eines Stils ab oder legt sie fest.|
| IstFormelVersteckt| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Formel ausgeblendet wird, wenn das Arbeitsblatt geschützt ist.|
| IstDatum/Uhrzeit| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das Zahlenformat ein Datumsformat ist.|
| IstTextWrapped| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Text innerhalb einer Zelle umbrochen wird.|
| IstGradient| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob es sich bei der Zellenschattierung um ein Verlaufsmuster handelt.|
| Ist gesperrt| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob eine Zelle geändert werden kann oder nicht.|
| IsPercent| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das Zahlenformat ein Prozentformat ist.|
| Schrumpfen bis es passt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der Text automatisch verkleinert wird, um in die verfügbare Spaltenbreite zu passen.|
| Einzugsebene| Ganze Zahl| WAHR| FALSCH|| Stellt die Einzugsebene für die Zelle oder den Bereich dar. Kann nur eine Ganzzahl zwischen 0 und 250 sein.|
| Nummer| Ganze Zahl| WAHR| FALSCH|| Ruft das Anzeigeformat für Zahlen und Datumsangaben ab oder legt es fest. Die Formatierungsmuster sind je nach Region unterschiedlich.|
| Drehwinkel| Ganze Zahl| WAHR| FALSCH|| Stellt den Textdrehwinkel dar.|
| Muster| Zeichenfolge| WAHR| FALSCH|| Ruft den Mustertyp des Zellenhintergrunds ab oder legt ihn fest.|
| Textrichtung| Zeichenfolge| WAHR| FALSCH|| Stellt die Textlesereihenfolge dar.|
| Vertikale Ausrichtung| Zeichenfolge| WAHR| FALSCH||Ruft den vertikalen Ausrichtungstyp des Texts in einer Zelle ab oder legt ihn fest.|
| HorizontaleAusrichtung| Zeichenfolge| WAHR| FALSCH|| Ruft den horizontalen Ausrichtungstyp des Texts in einer Zelle ab oder legt ihn fest.|
| Rahmenkollektion| Container| WAHR| FALSCH|||
| HintergrundThemaFarbe| Klasse:ThemeColor| WAHR| FALSCH|| Ruft die Hintergrunddesignfarbe ab und legt sie fest.|
| VordergrundThemaFarbe| Klasse:ThemeColor| WAHR| FALSCH|| Ruft die Vordergrunddesignfarbe ab und legt sie fest.|

