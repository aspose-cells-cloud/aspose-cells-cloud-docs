---
title: "Kopiera innehåll och format från ett annat kalkylblad."
second_title: "Document"
linktitle: "Kopiera"
type: docs
url: /worksheets/copy/
aliases: [/copy-excel-worksheet/]
keywords: "Aspose Cells kopierings-API för kalkylblad, kopiera kalkylblad via REST API, Aspose Cloud SDK kopiera, kopiera kalkylark"
description: "Lär dig hur du kopierar ett kalkylblad och dess format till ett nytt kalkylblad med Aspose.Cells Cloud REST API. Innehåller endpoint, parametrar, cURL-exempel och SDK-exempel för C#, Java, Python och mer."
weight: 20
---

Denna REST API kopierar ett kalkylblad och dess format till ett nytt kalkylblad inom samma arbetsbok.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

Följande parametrar används i begäran:

| Parameter Name   | Typ    | Plats  | Beskrivning                                                              |
| ---------------- | ------ | ------ | ------------------------------------------------------------------------ |
| `name`           | string | path   | Namnet på arbetsboksfilen.                                               |
| `sheetName`      | string | path   | Namnet på målkalkylbladet (det nya kalkylbladet).                        |
| `sourceSheet`    | string | query  | Namnet på kalkylbladet som ska kopieras.                                 |
| `options`        | object | body   | JSON-objekt som innehåller kopieringsalternativ (t.ex. kolumnbredd, formler). |
| `sourceWorkbook` | string | query  | Namnet på källarbetsboken om den skiljer sig från den aktuella arbetsboken. |
| `sourceFolder`   | string | query  | Mappbanan där källarbetsboken är lagrad.                                  |
| `folder`         | string | query  | Mappbanan där målarbetsboken ska sparas.                                  |
| `storageName`    | string | query  | Namnet på lagringstjänsten som ska användas.                             |

### Exempel på begäran och svar

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### Felhantering

API:et returnerar standard HTTP-statuskoder tillsammans med ett JSON-felmeddelande i brödtexten. Typiska svar inkluderar:

| HTTP-kod | Beskrivning                                                | Exempel på JSON-felbrödtext                                  |
| -------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| 400      | Felaktig begäran – saknade eller ogiltiga parametrar.      | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401      | Obehörig – saknad eller ogiltig token.                     | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404      | Inte hittad – arbetsbok, kalkylblad eller mapp finns inte. | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500      | Internt serverfel – oväntat tillstånd.                     | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}