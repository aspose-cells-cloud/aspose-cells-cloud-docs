---
title: "Flytta ett Excel-ark – Aspose.Cells Cloud API (v3.0)"
second_title: "Dokument"
linktitle: "Flytta"
type: docs
url: /worksheets/move/
aliases: [/move-excel-worksheets/]
keywords: "Aspose.Cells Cloud, Flytta ark, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Lär dig hur du flyttar ett Excel-ark till en ny position med Aspose.Cells Cloud API (v3.0). Inkluderar slutpunkt, nödvändiga parametrar, cURL-exempel och SDK-kod i C#, Java, Python m.m."
weight: 20
ArticleTitle: "Hur man flyttar ett Excel-ark med Aspose.Cells Cloud API v3.0"
---

Denna REST API flyttar ett ark inom en Excel-arbetsbok.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### Begärparametrar

| Parameternamn | Typ    | Plats  | Beskrivning                                                                                                           |
| ------------- | ------ | ------ | --------------------------------------------------------------------------------------------------------------------- |
| name          | string | path   | Namn på Excel-filen.                                                                                                  |
| sheetName     | string | path   | Namn på arket som ska flyttas.                                                                                        |
| moving        | object | body   | JSON-objekt som anger målarket (`DestinationWorksheet`) och den relativa positionen (`Position`).                    |
| folder        | string | query  | Mappväg där arbetsboken lagras.                                                                                       |
| storageName   | string | query  | Namn på lagringstjänsten.                                                                                             |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att anropa Aspose.Cells-webbtjänster. Exemplet nedan visar hur du flyttar ett ark med en enskild begäran.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                           |
|-----|-----------------------------|-----------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).     |
| 401 | Oautentiserad               | Ogiltigt eller saknat JWT-token.                                      |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.                     |
| 500 | Internt serverfel           | Oväntat serverfel.                                                    |

**Exempel på felaktig svarsnyttolast**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Missing required parameter 'moving'."
}
```

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}
---