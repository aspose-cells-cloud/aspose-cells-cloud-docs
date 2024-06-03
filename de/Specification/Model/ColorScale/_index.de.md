---
title: Farbskalierung
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/colorscale/
description: "Aspose.Cells Cloud-Modellspezifikation: ColorScale. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Farbskala
weight: 50
---
## **Farbskala**

 Beschreiben Sie die Regel für die bedingte Formatierung „ColorScale“. Diese Regel für die bedingte Formatierung erstellt eine abgestufte Farbskala für die Zellen.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| MaxCfvo| Klasse:BedingterFormatierungswert| WAHR| FALSCH|| Rufen Sie das Maximalwertobjekt dieser Farbskala ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Min kann nicht darauf festgelegt werden.|
| MaxColor| Klasse:Farbe| WAHR| FALSCH|| Rufen Sie die Verlaufsfarbe für den Maximalwert im Bereich ab oder legen Sie sie fest.|
| MittelCfvo| Klasse:BedingterFormatierungswert| WAHR| FALSCH|| Rufen Sie das mittlere Wertobjekt dieser Farbskala ab oder legen Sie es fest. CFValueObject mit dem Typ FormatConditionValueType.Max oder FormatConditionValueType.Min kann nicht darauf festgelegt werden.|
| Mittelfarbe| Klasse:Farbe| WAHR| FALSCH|| Rufen Sie die Verlaufsfarbe für den mittleren Wert im Bereich ab oder legen Sie sie fest.|
| MinCfvo| Klasse:BedingterFormatierungswert| WAHR| FALSCH|| Rufen Sie das Minimalwertobjekt dieser Farbskala ab oder legen Sie es fest. Null oder CFValueObject mit dem Typ FormatConditionValueType.Max kann nicht darauf festgelegt werden.|
| MinFarbe| Klasse:Farbe| WAHR| FALSCH||Rufen Sie die Verlaufsfarbe für den Mindestwert im Bereich ab oder legen Sie sie fest.|

