---
title: "Verschieben einer Pivot-Tabelle in einer Excel-Datei"
second_title: "Dokument"
linktitle: Verschieben
type: docs
url: /de/pivot-tables/move/
aliases: [  /de/move-pivot-table/ ]
keywords: "Aspose.Cells Cloud, Pivot-Tabelle verschieben, Excel, REST-API, SDK, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST-API verwenden, um eine Pivot-Tabelle innerhalb einer Excel-Arbeitsmappe zu verschieben. SDKs sind für Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift verfügbar."
weight: 120
---

Diese REST-API verschiebt eine Pivot-Tabelle innerhalb einer Excel-Arbeitsmappe.

**Voraussetzungen:** Vor dem Aufruf dieser Operation benötigen Sie ein gültiges JWT-Access-Token, und die Arbeitsmappe muss im Aspose-Cloud-Speicher gespeichert sein. Geben Sie die Parameter `folder` und `storageName` gegebenenfalls an.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **Anforderungsparameter**

| Parametername   | Typ     | Speicherort | Beschreibung                                            |
| --------------- | ------- | ----------- | ------------------------------------------------------- |
| name            | string  | path        | Name der Excel-Datei.                                   |
| sheetName       | string  | path        | Name des Arbeitsblatts, das die Pivot-Tabelle enthält. |
| pivotTableIndex | integer | path        | Nullbasierter Index der zu verschiebenden Pivot-Tabelle. |
| fieldIndex      | integer | query       | Index des zu verschiebenden Pivot-Felds.               |
| from            | string  | query       | Quellbereich des Felds (z. B. `Row` oder `Column`).    |
| to              | string  | query       | Zielbereich des Felds (z. B. `Row` oder `Column`).     |
| folder          | string  | query       | Ordner im Speicher, in dem sich die Datei befindet.     |
| storageName     | string  | query       | Name des Speicherdienstes.                              |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Verwenden Sie HTTPS-Endpunkte in der Produktion.
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}