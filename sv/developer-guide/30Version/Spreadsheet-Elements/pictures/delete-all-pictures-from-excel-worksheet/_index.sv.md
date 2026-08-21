---
title: "Ta bort alla bilder i ett Excel-arbetsblad"
second_title: "Document"
linktype: "Clear"
type: docs
url: /sv/pictures/clear/
aliases: [  /sv/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, ta bort alla bilder, arbetsblad, REST API, rensa bilder"
description: "Lär dig hur du tar bort alla bilder från ett Excel-arbetsblad med Aspose.Cells Cloud REST API, inklusive exempel med cURL och SDK:er."
weight: 60
ArticleTitle: "Hur man tar bort alla bilder i ett Excel-arbetsblad med Aspose.Cells Cloud"
---

Denna REST API tar bort **alla** bilder från ett arbetsblad.

**Förutsättningar**  
- Ett aktivt Aspose.Cells Cloud-konto med en giltig OAuth 2.0-åtkomsttoken.  
- API-version 3.0 (eller senare) krävs; tidigare versioner är föråldrade.  
- Den målsatta Excel-filen måste lagras i en stödd lagringsplats (standard eller anpassad).

**Versionstillämplighet**  
Slutpunkten följer Cells Cloud 3.0 API-specifikationen. Se till att dina klientbibliotek och begärande-URL:er riktar sig till `api.aspose.cloud/v3.0`.

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäranparametrar**

| Parameternamn | Typ   | Plats  | Beskrivning                                      |
| ------------- | ----- | ------ | ------------------------------------------------ |
| name          | string | Sökväg | Namn på Excel-filen.                             |
| sheetName     | string | Sökväg | Namn på arbetsbladet som innehåller bilder.      |
| folder        | string | Fråga  | Mapp där filen lagras.                           |
| storageName   | string | Fråga  | Namn på lagringstjänsten.                        |

### Felrespons

| HTTP-kod | Beskrivning                                                             |
| -------- | ----------------------------------------------------------------------- |
| 401      | Inte auktoriserad – token saknas eller är ogiltig.                     |
| 404      | Hittades inte – den angivna filen, arbetsbladet eller sidbrytningsindexet finns inte. |
| 400      | Felaktig begäran – felaktig syntax eller ogiltiga parametrar.          |
| 500      | Internt serverfel – ett oväntat tillstånd uppstod.                     |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
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

## Molnsdk-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på din affärslogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Anteckningar:** DELETE-åtgärden stöder inte paginering och är underliegande de vanliga rate limits för Aspose.Cells Cloud API (standard: 100 begäranden per minut). Justera din klientlogik därefter.

**Se även**:  
- [/pictures/delete/](../delete/) – Ta bort en specifik bild från ett arbetsblad.  
- [/pictures/add/](../add/) – Lägg till en bild i ett arbetsblad.  
---