---
title: "Diagramm aus einem Arbeitsblatt abrufen"
type: docs
url: /de/charts/get/
aliases: [  /de/get-chart-from-a-worksheet/ ]
weight: 10
keywords: "Aspose.Cells Cloud, Diagramm abrufen, Arbeitsblatt, REST API, Excel, Diagramm-API, Diagrammabruf, Excel-Diagramm"
description: "Abrufen von Diagramminformationen, einschließlich Metadaten und Exportformat, aus einem Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API."
ArticleTitle: "Diagramm aus einem Arbeitsblatt abrufen – Aspose.Cells Cloud API"
---

Diese REST API ruft Diagramminformationen ab.

**Voraussetzungen** – Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges Aspose.Cells Cloud-Konto, einen aktiven Speicherort sowie ein JWT-Access-Token. Holen Sie sich das Token gemäß den Anweisungen im Authentifizierungsleitfaden, bevor Sie API-Anfragen stellen.

## GetWorksheetChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Parametername   | Typ    | Ort   | Beschreibung                                |
| --------------- | ------ | ----- | ------------------------------------------- |
| name            | string | path  | Name der Excel-Datei.                       |
| sheetName       | string | path  | Name des Arbeitsblatts, das das Diagramm enthält. |
| chartNumber     | integer| path  | Nullbasierter Index des abzurufenden Diagramms. |
| format          | string | query | Gewünschtes Exportformat (z. B. png, jpeg). |
| folder          | string | query | Pfad des Ordners, in dem das Dokument gespeichert ist. |
| storageName     | string | query | Name des Speicherdiensts.                   |


### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Diagramm 1",
    "Type": "Balken",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |
## Wie Sie die GetWorksheetChart API mit SDKs verwenden

### GetWorksheetChart API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Diagramm 1",
    "Type": "Balken",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektziele konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}
---