---
title: "Aspose.Cells Cloud Web API – Summieren und Zählen nach Farbe in Excel"
second_title: "Dokument"
ArticleTitle: "Summe, Anzahl, Durchschnitt, Max, Min-Werte nach Farbe in Tabellenkalkulation/Excel"
LinkTitle: "Zellen nach Farbe aggregieren"
type: docs
url: /aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregieren, Farbe, Summe, Anzahl, Durchschnitt, Min, Max"
description: "Aggregieren Sie Excel-Zellen nach Hintergrund- oder Schriftfarbe (Summe, Anzahl, Durchschnitt, Min, Max) mit der Aspose.Cells Cloud API. Erfahren Sie mehr über den Endpunkt, die Parameter, die Authentifizierung und SDK-Beispiele."
weight: 100
---

## Übersicht

Die API kann Datenberechnungen basierend auf der **Farbe** der Zellen durchführen. Sie kann Summen bilden, Zählen, Durchschnittswerte ermitteln sowie den höchsten und niedrigsten Wert in einer Excel-Tabellenkalkulation basierend auf der Füll- oder Schriftfarbe der Zellen bestimmen.

| Berechnungsvorgang | Beschreibung                                                  |
| :----------------- | :------------------------------------------------------------ |
| Anzahl (Count)     | Ermitteln Sie die Anzahl der Zellen mit derselben Farbe.     |
| Summe (Sum)        | Berechnen Sie den Gesamtwert der Zellen mit derselben Farbe. |
| Maximalwert (Max)  | Ermitteln Sie den höchsten Wert unter den Zellen mit derselben Farbe. |
| Minimalwert (Min)  | Ermitteln Sie den niedrigsten Wert unter den Zellen mit derselben Farbe. |
| Durchschnitt (Average) | Berechnen Sie den Durchschnittswert der Zellen mit derselben Farbe. |

## Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Speicherort | Beschreibung                                                     |
| :-------------- | :----- | :---------- | :--------------------------------------------------------------- |
| Spreadsheet     | Datei  | FormData    | Die zu verarbeitende Excel-Arbeitsmappe.                        |
| Worksheet       | String | Query       | Name des Arbeitsblatts, das den Bereich enthält.                |
| Range           | String | Query       | A1-Stil-Bereich (z. B. `A1:B10`).                               |
| Operation       | String | Query       | Berechnungsmethode – `Sum`, `Count`, `Average`, `Min` oder `Max`. |
| ColorPosition   | String | Query       | Gibt an, welche Farbe ausgewertet werden soll – `Background`, `Font`. |
| Region          | String | Query       | Die Regionseinstellung der Tabellenkalkulation (z. B. `us-east-1`). |
| Password        | String | Query       | Passwort zum Öffnen einer geschützten Arbeitsmappe (optional).  |

#### Enumerationen

- **ColorPosition**

  | Wert       | Bedeutung                        |
  | :--------- | :------------------------------- |
  | Background | Verwenden Sie die Füllfarbe der Zelle. |
  | Font       | Verwenden Sie die Schriftfarbe der Zelle. |

**Beispiel für eine multipart/form-data-Anfrage**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Antwort

Das folgende Schema beschreibt das Antwortobjekt. Ein konkretes Beispiel folgt nach dem Schema.

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
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Beispielantwort (reale Werte)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wofür sollte die Aggregate-by-Color-API verwendet werden?

In einer Tabellenkalkulation stammen Daten aus verschiedenen Kategorien oft farblich gekennzeichnet. Diese API ermöglicht es Ihnen, Summen zu bilden, zu zählen, Durchschnitte zu berechnen oder Minimal- und Maximalwerte für jede Farbgruppe zu ermitteln, wodurch die farbbasierte Datenanalyse vereinfacht wird.

## Warum sollten Sie die Aggregate-by-Color-API verwenden?

Die API bietet eine schnelle und zuverlässige Möglichkeit, farbbasierte Berechnungen durchzuführen, ohne benutzerdefinierte Parsing-Logik schreiben zu müssen. Sie lässt sich nahtlos in Aspose.Cells Cloud SDKs integrieren, sodass Entwickler Farbaggregationen mit nur wenigen Codezeilen implementieren können.

## So verwenden Sie die Aggregate-by-Color-API mit SDKs

### Aggregate-by-Color-API-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">Aggregate-by-Color-API-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Low-Level-Details abstrahiert und es Ihnen ermöglicht, Berechnungen nach Zellfarbe mit nur einem kurzen Codeabschnitt zu aggregieren.  
Schauen Sie sich das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Hinweise:**

- Wenn Sie mit geschützten Arbeitsmappen arbeiten, fügen Sie den optionalen Abfrageparameter `Password` hinzu; andernfalls schlägt die Anfrage mit einem 401-Fehler fehl.
- Die maximale Anforderungsgröße für die Datei `Spreadsheet` beträgt 100 MB. Falls Sie größere Dateien verarbeiten müssen, erwägen Sie, die Arbeitsmappe zunächst in den Aspose-Cloud-Speicher hochzuladen und über den Parameter `Path` darauf zu verweisen (hier nicht dargestellt).