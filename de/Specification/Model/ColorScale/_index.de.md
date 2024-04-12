---
title: ColorScal
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/colorscale/
description: "Aspose.Cells Cloud-Modellspezifikation: ColorScale. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Farbskala**

 Beschreiben Sie die bedingte Formatierungsregel von ColorScale. Diese bedingte Formatierungsregel erstellt eine abgestufte Farbskala für die Zellen.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| MaxCfvo| Klasse:ConditionalFormattingValue| WAHR| FALSCH|| Rufen Sie das Maximalwertobjekt dieser ColorScale ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Min können nicht darauf festgelegt werden.|
| MaxColor| Klasse:Farbe| WAHR| FALSCH||Rufen Sie die Verlaufsfarbe für den Maximalwert im Bereich ab oder legen Sie sie fest.|
| MidCfvo| Klasse:ConditionalFormattingValue| WAHR| FALSCH|| Rufen Sie das Mittelwertobjekt dieser ColorScale ab oder legen Sie es fest. CFValueObject mit dem Typ FormatConditionValueType.Max oder FormatConditionValueType.Min kann nicht darauf festgelegt werden.|
| MidColor| Klasse:Farbe| WAHR| FALSCH|| Rufen Sie die Verlaufsfarbe für den mittleren Wert im Bereich ab oder legen Sie sie fest.|
| MinCfvo| Klasse:ConditionalFormattingValue| WAHR| FALSCH|| Rufen Sie das Minimalwertobjekt dieser ColorScale ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Max können nicht darauf festgelegt werden.|
| MinColor| Klasse:Farbe| WAHR| FALSCH|| Rufen Sie die Verlaufsfarbe für den Mindestwert im Bereich ab oder legen Sie sie fest.|

