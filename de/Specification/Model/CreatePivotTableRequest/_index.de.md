---
title: PivotTableRequests erstellen
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/createpivottablerequest/
description: "Aspose.Cells Cloud-Modellspezifikation: CreatePivotTableRequest. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, CreatePivotTableRequest
weight: 50
---
## **PivotTable-Anforderung erstellen**

 Gibt die Anforderung zum Erstellen einer Pivot-Tabelle an.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Name| Zeichenfolge| WAHR| FALSCH|| Name der Pivot-Tabelle|
| Quelldaten| Zeichenfolge| WAHR| FALSCH|| Die Daten für den neuen PivotTable-Cache.|
| Zielzellenname| Zeichenfolge| WAHR| FALSCH||Die Zelle in der oberen linken Ecke des Zielbereichs des PivotTable-Berichts.|
| UseSameSource| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die gleiche Datenquelle verwendet wird, wenn eine andere vorhandene Pivot-Tabelle diese Datenquelle verwendet hat. Wenn die Eigenschaft „true“ ist, wird Speicher gespart.|
| PivotFieldRows|Anordnung<Integer> | WAHR| FALSCH|| Stellt Zeilenfelder in einem PivotTable-Bericht dar.|
| PivotFieldColumns|Anordnung<Integer> | WAHR| FALSCH|| Stellt Spaltenfelder in einem PivotTable-Bericht dar.|
| PivotFieldData|Anordnung<Integer> | WAHR| FALSCH|| Stellt Datenfelder in einem PivotTable-Bericht dar.|

