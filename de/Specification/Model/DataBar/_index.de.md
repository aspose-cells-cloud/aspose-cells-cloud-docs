---
title: DataBa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/databar/
description: "Aspose.Cells Cloud-Modellspezifikation: DataBar. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **dataBar**

 Beschreiben Sie die bedingte Formatierungsregel von DataBar. Diese bedingte Formatierungsregel zeigt einen abgestuften Datenbalken im Zellbereich an.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| AxisColor| Klasse:Farbe| WAHR| FALSCH|| Ruft die Farbe der Achse für Zellen mit bedingter Formatierung als Datenbalken ab.|
| Achsenposition| Zeichenfolge| WAHR| FALSCH|| Ruft die Position der Achse der durch eine bedingte Formatierungsregel angegebenen Datenbalken ab oder legt diese fest.|
| BarBorder| Klasse:DataBarBorder| WAHR| FALSCH||Ruft ein Objekt ab, das den Rahmen einer Datenleiste angibt.|
| BarFillType| Zeichenfolge| WAHR| FALSCH|| Ruft ab oder legt fest, wie eine Datenleiste mit Farbe gefüllt wird.|
| Farbe| Klasse:Farbe| WAHR| FALSCH|| Rufen Sie die Farbe dieser DataBar ab oder legen Sie sie fest.|
| Richtung| Zeichenfolge| WAHR| FALSCH|| Ruft die Richtung ab, in der die Datenleiste angezeigt wird, oder legt diese fest.|
| MaxCfvo| Klasse:ConditionalFormattingValue| WAHR| FALSCH|| Rufen Sie das Maximalwertobjekt dieser DataBar ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Min können nicht darauf festgelegt werden.|
| Maximale Länge| Ganze Zahl| WAHR| FALSCH|| Stellt die maximale Länge der Datenleiste dar.|
| MinCfvo| Klasse:ConditionalFormattingValue| WAHR| FALSCH|| Rufen Sie das Mindestwertobjekt dieser DataBar ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Max können nicht darauf festgelegt werden.|
| Minimale Länge| Ganze Zahl| WAHR| FALSCH|| Stellt die Mindestlänge der Datenleiste dar.|
| NegativeBarFormat| Klasse:NegativeBarFormat| WAHR| FALSCH|| Ruft das NegativeBarFormat-Objekt ab, das einer bedingten Formatierungsregel für Datenleisten zugeordnet ist.|
| Wert anzeigen| Boolescher Wert| WAHR| FALSCH|| Rufen Sie das Flag ab, das angibt, ob die Werte der Zellen angezeigt werden sollen, auf die diese Datenleiste angewendet wird, oder legen Sie es fest. Der Standardwert ist wahr.|

