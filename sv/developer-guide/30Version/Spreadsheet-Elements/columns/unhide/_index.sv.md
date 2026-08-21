---
title: "Visa dolda kolumner i ett Excel-ark"
ArticleTitle: "Visa dolda kolumner i ett Excel-ark - Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Visa"
type: docs
url: /columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, molntjänst, visa kolumner, Excel, REST, SDK"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att visa dolda kolumner i ett Excel-ark. Innehåller begärandeinformation, ett cURL-exempel och SDK-kodexempel för flera programmeringsspråk."
weight: 50
---

Denna REST API visar dolda kolumner i ett kalkylark.

**Förutsättningar** – Alla Aspose.Cells Cloud-slutpunkter kräver HTTPS och en giltig OAuth 2.0-åtkomsttoken. Se till att du har fått en åtkomsttoken och inkluderat den i `Authorization`-huvudet i dina begäranden.

## PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parametername   | Typ     | Plats  | Beskrivning                                   |
| --------------- | ------- | ------ | --------------------------------------------- |
| name            | string  | path   | Arbetsbokens namn.                            |
| sheetName       | string  | path   | Arkets namn.                                  |
| startColumn     | integer | query  | Index för den första kolumnen som ska bearbetas. |
| totalColumns    | integer | query  | Antal kolumner som ska bearbetas.             |
| width           | number  | query  | Önskad kolumnbredd (standard = 50,0).         |
| folder          | string  | query  | Mappen som innehåller dokumentet.             |
| storageName     | string  | query  | Namnet på lagringstjänsten.                   |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till molntjänsten med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Typiska HTTP-statuskoder**

| Kod | Beskrivning                                  |
|-----|----------------------------------------------|
| 200 | OK – Kolumnerna visades framgångsrikt.      |
| 400 | Felaktig begäran – Ogiltiga parametrar.      |
| 401 | Auktorisering misslyckades – Saknad eller ogiltig token. |
| 404 | Hittades inte – Arbetsboken eller arket kunde inte hittas. |
| 500 | Internt serverfel – Oväntat fel.             |

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Besök <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-lagret</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}