---
title: DataBa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/databar/
description: "Aspose.Cells Cloud-Modellspezifikation: DataBar. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, DataBar
weight: 50
---
## **Datenleiste**

 Beschreiben Sie die Regel für die bedingte Formatierung von DataBar. Diese Regel für die bedingte Formatierung zeigt einen abgestuften Datenbalken im Zellbereich an.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Achsenfarbe| Klasse:Farbe| WAHR| FALSCH|| Ruft die Farbe der Achse für Zellen mit bedingter Formatierung als Datenbalken ab.|
| Achsenposition| Zeichenfolge| WAHR| FALSCH|| Ruft die Position der Achse der Datenbalken ab oder legt sie fest, die durch eine Regel zur bedingten Formatierung angegeben wird.|
| BalkenRahmen| Klasse:DataBarBorder| WAHR| FALSCH|| Ruft ein Objekt ab, das den Rahmen eines Datenbalkens angibt.|
| BalkenFülltyp| Zeichenfolge| WAHR| FALSCH|| Ruft ab oder legt fest, wie ein Datenbalken mit Farbe gefüllt wird.|
| Farbe| Klasse:Farbe| WAHR| FALSCH|| Rufen Sie die Farbe dieser Datenleiste ab oder legen Sie sie fest.|
| Richtung| Zeichenfolge| WAHR| FALSCH||Ruft die Richtung ab oder legt sie fest, in der die Datenleiste angezeigt wird.|
| MaxCfvo| Klasse:BedingterFormatierungswert| WAHR| FALSCH|| Rufen Sie das Maximalwertobjekt dieses DataBar ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Min kann nicht darauf festgelegt werden.|
| Maximale Länge| Ganze Zahl| WAHR| FALSCH|| Stellt die maximale Länge des Datenbalken dar.|
| MinCfvo| Klasse:BedingterFormatierungswert| WAHR| FALSCH|| Rufen Sie das Minimalwertobjekt dieses DataBar ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Max kann nicht darauf festgelegt werden.|
| Minimale Länge| Ganze Zahl| WAHR| FALSCH|| Stellt die Mindestlänge des Datenbalken dar.|
| NegativesBalkenformat| Klasse:NegativeBarFormat| WAHR| FALSCH|| Ruft das NegativeBarFormat-Objekt ab, das einer bedingten Formatierungsregel für Datenbalken zugeordnet ist.|
| Wert anzeigen| Boolescher Wert| WAHR| FALSCH|| Rufen Sie das Flag ab oder legen Sie es fest, das angibt, ob die Werte der Zellen angezeigt werden sollen, auf die dieser Datenbalken angewendet wird. Der Standardwert ist „true“.|

