---
title: "Autojustera rader i en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Rader"
type: docs
url: /sv/autofit-rows-on-an-excel-file/
aliases: [  /sv/auto-fit-rows-in-excel-workbooks/ , /sv/workbook/autofit/rows/ ]
keywords: "autojustera rader, Excel-arbetsbok, Aspose.Cells Cloud, REST API, alternativ för automatisk justering"
description: "Lär dig hur du automatiskt justerar radhöjder i en Excel-arbetsbok med Aspose.Cells Cloud REST API. Innehåller endpoint, parametrar, cURL-exempel och SDK-fragment för C#, Java, Python och mer."
weight: 90
ArticleTitle: "Autojustera rader i en Excel-arbetsbok – Aspose.Cells Cloud API"
---

**Förutsättningar**  
Innan du anropar API:t måste du hämta en giltig Bearer JWT-token från Asposes autentiseringstjänst och se till att målarbetsboken finns lagrad på en stödd lagringsplats (standardlagring eller en anpassad lagring du har konfigurerat).

Detta REST API gör det möjligt för dig att **autojustera rader** i en Excel-arbetsbok, det vill säga automatiskt justera radhöjden efter att data har infogats eller ändrats.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

Begärandeparametrarna inkluderar:

| Parameternamn     | Typ               | Plats   | Beskrivning                                                                     |
| ----------------- | ----------------- | ------- | ------------------------------------------------------------------------------- |
| name              | string            | path    | Namn på arbetsboksfilen.                                                        |
| autoFitterOptions | AutoFitterOptions | body    | Alternativ som styr beteendet vid autojustering.                               |
| startRow          | integer           | query   | Index för den första rad som ska justeras.                                      |
| endRow            | integer           | query   | Index för den sista rad som ska justeras.                                       |
| firstColumn       | integer           | query   | Index för den första kolumn som ska inkluderas i autojusteringen.              |
| lastColumn        | integer           | query   | Index för den sista kolumn som ska inkluderas i autojusteringen.               |
| onlyAuto          | boolean           | query   | Om **true** bearbetas endast rader med AutoFit-flaggan (standard är **false**). |
| folder            | string            | query   | Mappväg där arbetsboken är lagrad.                                              |
| storageName       | string            | query   | Namn på lagringstjänsten.                                                       |

**AutoFitterOptions** är ett objekt som anger hur autojusteringsåtgärden ska bete sig (t.ex. `AutoFitMergedCells`, `IgnoreHidden`).

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                  |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel.                               |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att anropa Aspose.Cells-webbtjänster. Ersätt `<jwt token>` med en giltig Bearer JWT-token från Asposes autentiseringstjänst.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Exempel på felaktigt svar (t.ex. om arbetsboken saknas):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "Den angivna arbetsboken 'myWorkbook.xlsx' finns inte."
}
```

{{< /tab >}}

{{< /tabs >}}

**Anteckningar**  
- När `AutoFitMergedCells` är inställt på **true** behandlas sammanfogade celler som en enda entitet vid autojustering.  
- Om `IgnoreHidden` är inställt på **true** hoppas dolda rader och kolumner över, och deras nuvarande dimensioner bevaras.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på ditt projekt. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---