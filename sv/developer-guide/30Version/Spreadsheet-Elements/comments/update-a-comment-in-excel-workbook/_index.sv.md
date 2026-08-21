---
title: "Uppdatera en kommentar i ett kalkylblads cell"
type: docs
url: /sv/comments/update/
aliases: [  /sv/update-a-comment-in-excel-workbook/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, kalkylblad, cellkommentar, uppdatera cellkommentar, kommentarobjekt"
description: "Använd Aspose.Cells Cloud REST API för att uppdatera en cellkommentar i ett kalkylblad i en Excel-arbetsbok, inklusive begärandedetaljer, svarsstatuskoder och SDK-exempel."
weight: 30
ArticleTitle: "Uppdatera cellkommentar i kalkylblad – Aspose.Cells Cloud API"
---

Detta REST API uppdaterar en kommentar i en kalkylblads cell. Använd denna slutpunkt för att **uppdatera en cellkommentar** i en Excel-fil.

**Förutsättningar:**
- Ett giltigt OAuth/JWT-åtkomsttoken måste inkluderas i `Authorization`-headern.
- Arbetsboken måste lagras på en stödd molnlagringsplats (ange `folder` och valfritt `storageName`).

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameter namn | Typ    | Plats  | Beskrivning                                                           |
| -------------- | ------ | ------ | --------------------------------------------------------------------- |
| name           | string | path   | Namnet på Excel-dokumentet.                                           |
| sheetName      | string | path   | Namnet på kalkylbladet som innehåller cellen.                        |
| cellName       | string | path   | Adressen till cellen (t.ex. **A1**).                                 |
| comment        | object | body   | Ett **Comment**-objekt som definierar kommentaren som ska läggas till eller uppdateras. |
| folder         | string | query  | Mappen där dokumentet lagras.                                         |
| storageName    | string | query  | Namnet på lagringstjänsten.                                           |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "detta är en kommentar",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

Möjliga svarsstatuskoder:

| Kod | Beskrivning                                    |
|-----|------------------------------------------------|
| 200 | Kommentaren uppdaterades framgångsrikt.       |
| 400 | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401 | Ej auktoriserad – autentisering misslyckades.  |
| 404 | Ej hittad – arbetsboken, kalkylbladet eller kommentaren finns inte. |
| 500 | Internt serverfel.                             |

**Anteckningar / Tips:**
- Maximal kommentarlängd är 1024 tecken.
- Stödda tecken är UTF‑8; undvik kontrolltecken.

## Moln SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla med Aspose.Cells Cloud. En SDK hanterar detaljer på lågnivå så att du kan fokusera på ditt projekt. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förvaret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

Relaterade operationer:
- [Hämta kalkylbladskommentar](/comments/get/)
- [Lägg till kalkylbladskommentar](/comments/add/)
- [Ta bort kalkylbladskommentar](/comments/delete/)