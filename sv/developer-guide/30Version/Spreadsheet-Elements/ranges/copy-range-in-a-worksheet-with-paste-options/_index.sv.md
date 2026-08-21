---
title: "Kopiera intervall i ett kalkylblad med kopiéralternativ"
second_title: "Dokument"
linktitle: "Kopiera"
type: docs
url: /sv/ranges/copy/
aliases: [  /sv/copy-range-in-a-worksheet-with-paste-options/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, kopiera intervall, kalkylblad, kopiéralternativ"
description: "Använd Aspose.Cells Cloud REST API för att kopiera ett intervall inom ett Excel-kalkylblad med fullständigt stöd för kopiéralternativ. Inkluderar SDK-exempel för flera programmeringsspråk."
weight: 20
ArticleTitle: "Kopiera intervall i ett kalkylblad med kopiéralternativ – Aspose.Cells Cloud API"
---

Detta REST API kopierar ett intervall i ett kalkylblad i en Excel-arbetsbok. För relaterade åtgärder, se dokumentationen för **Hämta intervall** och **Uppdatera intervall**.

**Förutsättningar:** För att använda denna slutpunkt måste du ha en giltig OAuth 2.0- eller JWT-token och säkerställa att din API-version matchar URL:en i begäran.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **Begärandeparametrar**

| Parameter Namn | Typ    | Plats  | Beskrivning                                                                   |
| -------------- | ------ | ------ | ----------------------------------------------------------------------------- |
| name           | string | path   | Namnet på arbetsboken.                                                        |
| sheetName      | string | path   | Namnet på kalkylbladet.                                                       |
| rangeOperate   | string | body   | Åtgärden som ska utföras: `copydata`, `copystyle`, `copyto` eller `copyvalue`. |
| folder         | string | query  | Mappen som innehåller arbetsboken.                                            |
| storageName    | string | query  | Namnet på lagringstjänsten.                                                   |

**Anteckningar:** Fältet `rangeOperate` bestämmer vad som kopieras. Använd `copydata` för att kopiera endast cellvärden, `copystyle` för formatering, `copyto` för både data och stil samt `copyvalue` för att kopiera värden utan formler. API:et stöder intervall upp till 1 miljon celler; större intervall kan leda till en timeout.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Ett lyckat svar returnerar statuskoden `200 OK`. Vid fel kan API:et returnera svar som:

```json
{
  "Code": 400,
  "Message": "Bad Request – ogiltiga parametrar."
}
```

eller

```json
{
  "Code": 401,
  "Message": "Unauthorized – autentiseringstoken saknas eller är ogiltig."
}
```

Dessa felobjekt innehåller en HTTP-statuskod och ett beskrivande meddelande för att hjälpa till med felsökning.

{{< /tab >}}

{{< /tabs >}}

Du kan ladda ner en exempelarbetsbok för att testa kopieringsåtgärden [här](https://example.com/sample.xlsx).

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}
---