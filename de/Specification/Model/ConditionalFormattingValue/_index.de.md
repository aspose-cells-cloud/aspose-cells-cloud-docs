---
title: BedingterFormatierungswert
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/conditionalformattingvalue/
description: "Aspose.Cells Cloud-Modellspezifikation: ConditionalFormattingValue. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, ConditionalFormattingValue
weight: 50
---
## **bedingterFormatierungswert**

 Beschreibt die Werte der Interpolationspunkte in einer Verlaufsskala, einer Datenleiste oder einem Symbolsatz.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| IsGTE| Boolescher Wert| WAHR| FALSCH||Rufen Sie das Flag „Größer als oder gleich“ ab oder legen Sie es fest. Wird nur für Symbolsätze verwendet. Legt fest, ob dieser Schwellenwert den Operator „Größer als“ oder „Gleich“ verwendet. „False“ bedeutet, dass „Größer als“ anstelle von „Größer als oder gleich“ verwendet wird. Der Standardwert ist „True“.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Rufen Sie den Typ dieses bedingten Formatierungswertobjekts ab oder legen Sie ihn fest. Wenn Sie den Typ auf FormatConditionValueType.Min oder FormatConditionValueType.Max festlegen, wird „Value“ automatisch auf null gesetzt.|
| Wert| Klasse:Objekt| WAHR| FALSCH|| Rufen Sie den Wert dieses Wertobjekts für bedingte Formatierung ab oder legen Sie ihn fest. Es sollte in Verbindung mit „Typ“ verwendet werden.|

