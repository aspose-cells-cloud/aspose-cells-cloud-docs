---
title: "Autojustera flera kolumner i ett Excel-arbetsark"
second_title: "Document"
linktitle: "Kolumner"
type: docs
url: /sv/worksheets/autofit/columns/
aliases: [  /sv/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, autojustera kolumner, Excel API, molnspreadsheat, REST"
description: "Lär dig hur du autojusterar flera kolumner i ett Excel-arbetsark med Aspose.Cells Cloud REST API (v3.0). Innehåller endpoint, parametrar, cURL-exempel, felhantering och SDK-kodsnuttar för C#, Java, Python och mer."
weight: 20
---

Denna REST API autojusterar **flera kolumner** i ett Excel-arbetsark.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **Begäranparametrar**

| Parameter Name      | Typ     | Plats  | Beskrivning                                                                                                                                 |
| ------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string  | path   | Filnamnet.                                                                                                                                  |
| sheetName           | string  | path   | Arbetsarkets namn.                                                                                                                          |
| firstColumn         | integer | query  | Startkolumnindexet.                                                                                                                         |
| lastColumn          | integer | query  | Slutkolumnindexet.                                                                                                                          |
| autoFitterOptions\* | object  | body   | Autojusteringsalternativ (se [Autojusteringsalternativ](/cells/auto-fitter-options/)). Innehåller `AutoFitMergedCells`, `IgnoreHidden` och `OnlyAuto`. |
| firstRow            | integer | query  | Startradindex för autojustering (**valfritt**).                                                                                             |
| lastRow             | integer | query  | Slutradindex för autojustering (**valfritt**).                                                                                              |
| folder              | string  | query  | Mappväg i lagring (**valfritt**).                                                                                                           |
| storageName         | string  | query  | Lagringsnamn (**valfritt**).                                                                                                                |

\*Parameternamnet visas som en länk till den relaterade dokumentationen.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}