---
title: "Automatisk anpassning av kolumner i en Excel-fil"
second_title: "Dokument"
linktitle: "Kolumner"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "Automatisk anpassning av kolumner, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att automatiskt anpassa kolumner i en Excel-arbetsbok. Inkluderar begärandedetaljer, ett cURL-exempel och SDK-kodexempel för flera språk."
weight: 90
---

Denna REST API stöder automatisk anpassning av kolumner i en Excel-arbetsbok.

## PostAutofitWorkbookColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

Begärandeparametrarna är:

| Parameternamn         | Typ     | Plats  | Beskrivning                                         |
| --------------------- | ------- | ------ | --------------------------------------------------- |
| **name**              | string  | path   | Namnet på arbetsboksfilen.                          |
| **autoFitterOptions** | objekt  | body   | Alternativ som styr beteendet för automatisk anpassning. |
| **startColumn**       | heltal  | query  | Nollbaserat index för den första kolumnen som ska automatiskt anpassas. |
| **endColumn**         | heltal  | query  | Nollbaserat index för den sista kolumnen som ska automatiskt anpassas. |
| **folder**            | string  | query  | Mappen som innehåller arbetsboken.                  |
| **storageName**       | string  | query  | Namnet på lagringstjänsten.                         |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Obs:** Använd alltid HTTPS-slutpunkten i produktion och håll din JWT-token hemlig.

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

### Förutsättningar
Innan du anropar denna åtgärd, se till att du har en giltig Aspose Cloud API-nyckel, en genererad JWT-token och att målarbetsboken redan finns på den angivna lagringsplatsen.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

API:et kan returnera följande HTTP-statuskoder:

| Kod | Beskrivning                                      |
|-----|--------------------------------------------------|
| 200 | Framgång – kolumner har automatiskt anpassats   |
| 400 | Felaktig begäran – saknade eller ogiltiga parametrar |
| 401 | Otillåten – ogiltig eller utgången JWT-token    |
| 500 | Serverfel – internt bearbetningsfel              |

## Moln-SDK-familj

Att använda en SDK är det mest effektiva sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på din projekts logik. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}