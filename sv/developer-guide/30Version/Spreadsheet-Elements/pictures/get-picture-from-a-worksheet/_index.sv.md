---
title: "Hämta alla bilder i ett Excel-ark"
second_title: "Dokument"
linktype: "get-all"
type: docs
url: /pictures/get-all/
aliases: [/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel-ark, bild-API, hämta alla bilder, REST API, SDK"
description: "Hämta alla bildobjekt från ett Excel-ark via Aspose.Cells Cloud REST API."
ArticleTitle: "Hämta alla bilder i ett Excel-ark - Aspose.Cells Cloud API"
weight: 10
---

Detta REST API hämtar all bildinformation från ett Excel-ark.

**Förutsättningar**  
Innan du anropar detta slutställe, se till att du har:

- En giltig Aspose Cloud JWT-åtkomsttoken.  
- Målexcelfilen uppladdad till den valda lagringen.  
- Rätt lagringsnamn (om du använder en anpassad lagring).  
- Arknamnet som innehåller bilderna.

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Obs:** Använd HTTPS (TLS 1.2 eller högre) när du anropar API:et och inkludera en giltig JWT-token i `Authorization`-headern.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärningsparametrar**

| Parameternamn | Typ   | Plats  | Beskrivning                                      |
| ------------- | ----- | ------ | ------------------------------------------------ |
| name          | string | path   | Namnet på Excel-filen.                           |
| sheetName     | string | path   | Namnet på arket som innehåller bilderna.         |
| folder        | string | query  | Sökvägen till mappen där filen lagras.           |
| storageName   | string | query  | Namnet på lagringstjänsten.                      |

### Felsvar

| HTTP-kod | Beskrivning                                                              |
| -------- | ------------------------------------------------------------------------ |
| 401      | Inte auktoriserad – token saknas eller är ogiltig.                      |
| 404      | Hittades inte – den angivna filen, arket eller sidbrytningsindexet finns inte. |
| 400      | Ogiltig begäran – felaktig begäran syntax eller ogiltiga parametrar.    |
| 500      | Internt serverfel – ett oväntat tillstånd inträffade.                   |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Lyckat svar** – Ett lyckat anrop returnerar HTTP 200 med en JSON-svarskropp som innehåller ett `Pictures`-objekt med resurslänkar för varje bild.

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

Du kan ladda ner SDK:erna direkt från deras respektive pakethanterare (t.ex. NuGet för .NET, Maven Central för Java, Composer för PHP, npm för Node.js, PyPI för Python, CPAN för Perl och Go modules för Go).  

*Se även:* Lägg till en bild, Ta bort en bild, Uppdatera billedegenskaper.