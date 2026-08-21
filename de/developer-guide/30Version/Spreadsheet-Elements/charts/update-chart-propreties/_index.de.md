---
title: "Diagrammeigenschaften aktualisieren"
type: docs
url: /de/charts/properties/update/
aliases: [  /de/update-chart-properties/ ]
weight: 160
keywords: "Aspose.Cells, Diagramm, aktualisieren, Excel, REST API, SDK"
description: "Erfahren Sie, wie Sie Diagrammeigenschaften (Typ, Titel, Legende usw.) in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API (v3.0) aktualisieren können. Enthält Endpunkt, Parameter, cURL-Beispiel und SDK-Snippets für C#, Java, PHP, Ruby, Node.js, Perl und Go."
ArticleTitle: "Diagrammeigenschaften aktualisieren – Aspose.Cells Cloud REST API"
---

Diese REST API aktualisiert Diagrammeigenschaften.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Anforderungsparameter

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                      |
| --------------- | ------ | ---------------------------------- | ----------------------------------------------------------------- |
| name            | string | path                               | Der Name der Excel-Datei.                                         |
| sheetName       | string | path                               | Der Name des Arbeitsblatts, das das Diagramm enthält.            |
| chartIndex      | integer| path                               | Der nullbasierte Index des zu aktualisierenden Diagramms.        |
| chart           | object | body                               | JSON-Objekt, das die zu ändernden Diagrammeigenschaften definiert.|
| folder          | string | query                              | Der Ordner im Speicher, in dem sich die Datei befindet.          |
| storageName     | string | query                              | Der Name des Speicherdiensts.                                     |

### Anforderungstext-Schema

Das **`chart`**-Objekt enthält die Eigenschaften, die Sie ändern können. Nachfolgend finden Sie ein repräsentatives JSON-Beispiel mit mehreren häufig verwendeten Feldern:

```json
{
  "Title": {
    "Text": " Quartalsumsätze"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Hinweis:** Es müssen nur die Felder übermittelt werden, die Sie tatsächlich ändern möchten. Weitere Eigenschaften behalten ihre aktuellen Werte bei.

Die <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Antwort

Die API gibt ein JSON-Objekt zurück, das das Ergebnis des Vorgangs angibt. Eine erfolgreiche Aktualisierung ergibt:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Erfolgs-HTTP-Statuscodes**

| HTTP-Status | Beschreibung                                           |
| ----------- | ------------------------------------------------------ |
| 200         | OK – Die Diagrammeigenschaften wurden erfolgreich aktualisiert. |

**Antwortheader**

| Header           | Beschreibung                                                      |
| ---------------- | ----------------------------------------------------------------- |
| `Content-Type`   | `application/json` – Gibt an, dass der Antworttext JSON-formatiert ist. |
| `X-RequestId`    | Eindeutige Kennung für die Anforderung (nützlich zur Fehlerbehebung). |

Mögliche Fehlerantworten:

| HTTP-Status | Beschreibung                                             |
| ----------- | -------------------------------------------------------- |
| 400         | Bad Request – ungültige Parameter oder Body             |
| 401         | Unauthorized – fehlendes oder ungültiges Token          |
| 404         | Not Found – Datei, Arbeitsblatt oder Diagramm nicht gefunden |
| 500         | Internal Server Error                                    |

Weitere diagrammbezogene Vorgänge finden Sie in den verwandten Themen wie [Diagrammtitel aktualisieren](/charts/title/update/) und [Diagrammlegende aktualisieren](/charts/legend/update/).

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webservices durchführen:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}