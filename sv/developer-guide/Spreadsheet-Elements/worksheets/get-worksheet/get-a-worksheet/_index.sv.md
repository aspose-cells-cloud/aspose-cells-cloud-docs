---
title: Hämta arbetsblad från ett Excel-arbetsblad
second_title: Aspose.Cells Cloud Documen
linktitle: Arbetsblad
type: docs
url: /sv/worksheets/get-worksheet/
keywords: Get worksheet to different format from an Excel worksheet
description: Aspose.Cells Cloud REST API stöder att hämta kalkylblad till olika format från ett Excel-kalkylblad. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 10
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hämta kalkylblad från ett Excel-kalkylblad
---
Denna REST API indikerar `get worksheet description` eller `export worksheet to kinds of format file`.

 Du kan exportera format:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV-fil](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [Textmeddelande](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/),[GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/),[TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [TAL](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
 
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokumentnamnet.|
| arknamn| sträng| väg| Arbetsbladets namn.|
| formatera| sträng| fråga|Det exporterade filformatet.|
| vertikal upplösning| heltal| fråga| Ställer in den vertikala upplösningen för genererade bilder, i punkter per tum.|
| horisontell upplösning| heltal| fråga| Ställer in den horisontella upplösningen för genererade bilder, i punkter per tum.|
| område| sträng| fråga| Exporterat område.|
| sidaIndex| heltal| fråga| Exporterat sidindex.|
| mapp| sträng| fråga| Dokumentmappen.|
| lagringsnamn| sträng| fråga| lagringsnamn.|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

{
stream
} 

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
