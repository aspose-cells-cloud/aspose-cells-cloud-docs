---
title: Aspose.Cells Cloud Web API – Summe, Anzahl, Durchschnittswert usw. nach Farbe in Tabellenkalkulation/Exce
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /de/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Das Aspose.Cells Cloud Web API (Excel Cloud API) kann Datenberechnungen, Summierungen und Mittelwerte durchführen und kann auch die Maximal- und Minimalwerte in einer Excel-Tabelle basierend auf der Füllung oder Schriftfarbe der Zellen finden
weight: 100
kwords: Summe, Anzahl, Durchschnittswert, Maximalwert, Minimalwert, Excel REST API, Tabellenkalkulationsoperationen, Aspose.Cells, Excel Cloud API
---
Der API kann Datenberechnungen, Summierungen und Mittelwerte durchführen und anhand der Füllung oder Schriftfarbe der Zellen auch die Maximal- und Minimalwerte in einer Excel-Tabelle ermitteln.

| Berechnungsvorgang| Beschreibung|
|:- |:- |
| Zählen| Bestimmen Sie die Anzahl der Zellen mit der gleichen Farbe.|
| Summe| Berechnen Sie den Gesamtwert der Zellen mit derselben Farbe.|
| Maximalwert| Identifizieren Sie den höchsten Wert unter den Zellen mit derselben Farbe.|
| Min-Wert| Suchen Sie den niedrigsten Wert unter den Zellen mit der gleichen Farbe.|
|Durchschnittswert| Berechnen Sie den Mittelwert von Zellen mit derselben Farbe.|

## **Aggregieren von Cells nach Farbe API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Kalkulationstabelle| Datei| FormData| Tabellenkalkulationsdatei hochladen.|
| Arbeitsblatt| Zeichenfolge| Abfrage| Gibt das Arbeitsblatt an.|
| Reichweite| Zeichenfolge| Abfrage| Gibt den Bereich an.|
| Betrieb| Zeichenfolge| Abfrage| Geben Sie Berechnungsmethoden an, einschließlich Summe, Anzahl, Durchschnitt, Min und Max.|
| Farbposition| Zeichenfolge| Abfrage| Gibt den zu summierenden und zu zählenden Inhalt basierend auf der Hintergrundfarbe und/oder der Schriftfarbe an.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

### **Antwort**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Wo sollten wir das Aggregat nach Farbe API verwenden?

In einer Kalkulationstabelle werden Daten aus verschiedenen Kategorien in unterschiedlichen Farben angezeigt, sodass Operationen wie das Summieren, Zählen, Berechnen von Durchschnittswerten und das Ermitteln von Maximal- und Minimalwerten anhand der Farbe möglich sind.

## Warum sollten Sie das Aggregate by Color API verwenden?

- Stellen Sie Methoden zur Farbdatenanalyse bereit.
- Klassifizieren und berechnen Sie Daten anhand der Farbe, um grundlegende Daten für die Datenanalyse bereitzustellen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie das Aggregat nach Farbe API mit SDKs

### Aggregat nach Farbe API Spezifikation

 Der[Aggregat nach Farbe API Spezifikation](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, Berechnungen nach Zellenfarbe mit nur einem kurzen Codestück zu aggregieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
