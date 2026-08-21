---
title: "Legende eines Diagramms in einem Arbeitsblatt anzeigen"
type: docs
url: /de/charts/legend/show/
aliases: [  /de/show-chart-legend-in-a-worksheet/ ]
weight: 100
keywords: "Aspose.Cells Cloud, Chart-Legende-API, Excel-Diagramm-Legende, REST PUT Chart-Legende, Aspose API v3.0"
description: "Erfahren Sie, wie Sie die Legende eines Diagramms in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) anzeigen. Enthält Endpunkt-Details, Parameter, ein cURL-Beispiel und SDK-Snippets."
---

Diese REST API ermöglicht es Ihnen, die **Legende** – das erklärende Feld, das die Datenreihen identifiziert – in einem Diagramm anzuzeigen, das sich in einem Arbeitsblatt einer Excel-Arbeitsmappe befindet.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Anforderungsparameter

| Parametername   | Typ    | Speicherort | Beschreibung                                      |
| --------------- | ------ | ----------- | ------------------------------------------------- |
| name            | string | path        | Der Name der Arbeitsmappendatei.                 |
| sheetName       | string | path        | Der Name des Arbeitsblatts, das das Diagramm enthält. |
| chartIndex      | integer | path       | Der nullbasierte Index des Diagramms.            |
| folder          | string | query       | Der Ordner, der die Arbeitsmappe enthält.        |
| storageName     | string | query       | Der Name des Speicherdiensts.                    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Die Authentifizierung erfolgt mithilfe eines Bearer-JWT-Tokens, das im **Authorization**-Header übergeben wird.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie der Aufruf mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
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

Die API kann folgende HTTP-Statuscodes zurückgeben:

- **200 OK** – Die Legende wurde erfolgreich angezeigt.
- **400 Bad Request** – Ungültige Parameter.
- **401 Unauthorized** – Authentifizierung fehlgeschlagen.
- **404 Not Found** – Die angegebene Arbeitsmappe, das Arbeitsblatt oder das Diagramm ist nicht vorhanden.
- **500 Internal Server Error** – Ein unerwarteter Serverfehler ist aufgetreten.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und lässt Sie sich auf Ihre Projekt Aufgaben konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}