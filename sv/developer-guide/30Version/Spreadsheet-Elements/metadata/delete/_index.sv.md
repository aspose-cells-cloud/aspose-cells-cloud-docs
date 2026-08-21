---
title: "Ta bort metadata från Excel-filer"
second_title: "Dokument"
linktitle: "Ta bort utan att använda lagring"
type: docs
url: /sv/metadata/delete/
keywords: "Aspose.Cells, ta bort metadata, Excel-API, arbetsboksegenskaper"
description: "Ta bort arbetsboksmetadata (författare, titel, anpassad) via Aspose.Cells Cloud API. Inkluderar slutpunkt, autentisering, parametrar, cURL- och SDK-exempel."
weight: 55
ArticleTitle: "Ta bort metadata från Excel-filer – Aspose.Cells Cloud-dokumentation"
---

**Översikt**  
Åtgärden Ta bort metadata tar bort permanent alla arbetsboksegenskaper (standard och anpassade) från den uppladdade Excel-filen/filerna och returnerar den/dessa bearbetade filen/filerna i svaret.

**Förutsättningar**  
- En giltig Aspose.Cells Cloud JWT-token (fås via OAuth 2.0-autentiseringsflödet).  
- API-version **v3.0** (den slutpunkt som används i detta exempel).  
- För användning av SDK: installera lämplig Aspose.Cells Cloud SDK för ditt programmeringsspråk (t.ex. via NuGet, Maven, npm, pip, CPAN eller Go-moduler).

Detta REST-API tar bort **metadata** från en eller flera Excel-filer. Det tar bort arbetsboksegenskaper såsom författare, titel och anpassad data, och returnerar de rensade filerna.

## a API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäringsparametrar**

| Parameternamn | Typ   | Plats     | Beskrivning                                                |
| ------------- | ----- | --------- | ---------------------------------------------------------- |
| file          | fil   | formData  | Excel-fil att ladda upp för **metadata**-borttagning      |
| type          | sträng | query     | Åtgärdstyp; ställ in på **all** för att ta bort all **metadata** |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Felaktiga svar** kan inkludera:

- **400 Bad Request** – saknad fil eller ogiltigt `type`-värde.  
- **401 Unauthorized** – ogiltig eller saknad JWT-token.  
- **500 Internal Server Error** – serverseit bearbetningsfel.

API:n returnerar ett JSON-objekt som innehåller ett `Error`-fält med detaljer för varje fall.

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Metadata borttagna, fil returnerad |
| 400 | Bad Request | Saknad fil eller ogiltigt `type` |
| 401 | Unauthorized | Ogiltig eller saknad JWT |
| 500 | Internal Server Error | Serverbearbetningsfel |

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se i <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}