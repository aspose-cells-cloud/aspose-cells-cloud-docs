---
title: "Legende eines Diagramms in einem Arbeitsblatt aktualisieren"
type: docs
url: /charts/legend/update/
aliases: [/update-chart-legend-in-a-worksheet/]
weight: 160
keywords: "Aspose.Cells, Cloud, Excel, Diagramm, Legende, REST API, Aktualisieren, Arbeitsblatt, cURL, SDK"
description: "So aktualisieren Sie die Legende eines Diagramms in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API – mit cURL-Anforderungsbeispielen und SDK-Code-Snippets für mehrere Programmiersprachen."
ArticleTitle: "Legende eines Diagramms in einem Arbeitsblatt aktualisieren – Aspose.Cells Cloud API-Anleitung"
---

Diese REST API aktualisiert die Legende eines Diagramms.

**Voraussetzungen:** Um diesen Endpunkt nutzen zu können, benötigen Sie ein gültiges Aspose Cloud JWT-Token, und die Ziel-Arbeitsmappe muss an einem unterstützten Speicherort gespeichert sein (standardmäßig ist dies der Aspose Cloud-Speicher). Stellen Sie sicher, dass Arbeitsmappe, Arbeitsblattname und Diagrammindex korrekt sind.

Eine Diagramm-Legende zeigt die Namen und Symbole der Datenreihen in einem Diagramm an. Durch die Aktualisierung der Legende können Sie ihr Erscheinungsbild anpassen, z. B. Schriftart, Farbe und Schattierung.

## PostWorksheetChartLegend API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ     | Ort     | Beschreibung                                      |
| ------------- | ------- | ------- | ------------------------------------------------- |
| name          | string  | path    | Name der Arbeitsmappe.                            |
| sheetName     | string  | path    | Name des Arbeitsblatts.                           |
| chartIndex    | integer | path    | Index des zu ändernden Diagramms.                 |
| legend        | object  | body    | JSON-Objekt, das die Legenden-Einstellungen definiert. |
| folder        | string  | query   | Ordner, der die Arbeitsmappe enthält.             |
| storageName   | string  | query   | Name des Speichers.                               |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie die Cloud-API mittels cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK beschleunigt die Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}