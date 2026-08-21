---
title: "Kopiera kolumner i ett Excel-arbetsark"
second_title: "Dokument"
linktitle: "Kopiera"
type: docs
url: /columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, kopiera kolumner, Excel API, REST, molntjänst, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Lär dig hur du kopierar en eller flera kolumner i ett Excel-arbetsark med Aspose.Cells Cloud REST API (v3.0). Inkluderar begärsyntax, nödvändiga parametrar, autentiseringsuppgifter, felhantering och SDK-exempel i C#, Java, Python, Ruby, Node.js, Go, Perl och mer."
articleTitle: "Kopiera kolumner i ett Excel-arbetsark med Aspose.Cells Cloud API"
weight: 30
---

Denna REST API kopierar **kolumner** i ett Excel-arbetsark. **Kopiera kolumner**-åtgärden låter dig duplicera en enskild kolumn eller ett intervall av kolumner och infoga kopian på en angiven plats inom samma arbetsark. Använd denna slutpunkt för att effektivt kopiera kolumner vid arbetet med stora kalkylark, och se relaterade åtgärder som [Lägg till kolumn](/columns/add/) och [Dölj kolumn](/columns/hide/) för ytterligare kolumnhanteringsuppgifter.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Begärparametrar

| Parameternamn              | Typ     | Plats  | Beskrivning                                                                           |
| -------------------------- | ------- | ------ | ------------------------------------------------------------------------------------- |
| **name**                   | string  | path   | Namnet på arbetsboken.                                                                |
| **sheetName**              | string  | path   | Namnet på arbetsarket.                                                                |
| **sourceColumnIndex**      | integer | query  | 0-baserat index för kolumnen som ska kopieras.                                       |
| **destinationColumnIndex** | integer | query  | 0-baserat index där den kopierade kolumnen/kolumnerna ska infogas.                   |
| **columnNumber**           | integer | query  | Antalet på varandra följande kolumner som ska kopieras.                              |
| **worksheet**              | string  | query  | _(Valfritt)_ Arbetsarkidentifikator som används när arbetsarkets namn skiljer sig från sökvägen. |
| **folder**                 | string  | query  | Sökvägen till mappen som innehåller arbetsboken i Aspose Cloud-lagringen.            |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) definierar hela kontraktet för denna åtgärd.

### cURL-exempel

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Svar

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Felhantering

API:et returnerar standard HTTP-statuskoder med ett JSON-svar som beskriver felet.

| Statuskod | Betydelse                                          | Exempel på JSON-svar                                                |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Ogiltig begäran – ogiltiga parametrar              | `{ "Code": 400, "Message": "Invalid column index." }`               |
| **401**   | Auktorisering misslyckades – token saknas eller är ogiltig | `{ "Code": 401, "Message": "Access token is invalid or expired." }` |
| **404**   | Hittades inte – arbetsboken eller arbetsarket finns inte | `{ "Code": 404, "Message": "Workbook not found." }`                 |
| **500**   | Internt serverfel – oväntat tillstånd              | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

> **Så här felsöker du:** Kontrollera att åtkomsttoken är giltig, att namnen på arbetsboken och arbetsarket är korrekta och att `sourceColumnIndex`, `destinationColumnIndex` och `columnNumber` ligger inom arbetsarkets kolumnintervall.

## Molntjänstfamilj för SDK
Att använda en SDK är det bästa sättet att snabba på utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Hur autentiserar jag vid anrop till Copy Columns API?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Skaffa en OAuth2-åtkomsttoken från Aspose Cloud med ditt klient-ID och hemlighet, och inkludera den i begärandehuvudet som `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "Vad är skillnaden mellan `sourceColumnIndex` och `destinationColumnIndex`?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` är det 0-baserade indexet för kolumnen du vill kopiera. `destinationColumnIndex` är det 0-baserade indexet där den kopierade kolumnen/kolumnerna ska infogas."
      }
    },
    {
      "@type": "Question",
      "name": "Vad får jag för svar om kopieringsåtgärden misslyckas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "API:et returnerar en statuskod som inte är 200 (t.ex. 400 för ogiltig begäran, 401 för auktoriseringsfel). Svarsbody innehåller ett JSON-objekt med fälten `Code` och `Message` som beskriver felet."
      }
    }
  ]
}
</script>
---