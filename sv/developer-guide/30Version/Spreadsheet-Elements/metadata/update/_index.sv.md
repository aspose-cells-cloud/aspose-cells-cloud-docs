---
title: "Uppdatera metadata"
second_title: "Dokument"
linktitle: "Uppdatera utan att använda lagring"
type: docs
url: /metadata/update/
keywords: "metadata, Excel, Aspose.Cells Cloud, REST API, uppdatera, kalkylark"
description: "Aspose.Cells Cloud REST API möjliggör uppdatering av metadata i Excel-filer. Den stöder flera SDK:er (C#, Java, Python, Ruby, Go etc.) för sömlös integration över olika programmeringsspråk."
weight: 35
ArticleTitle: "Uppdatera metadata – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API uppdaterar **metadata** i flera Excel-filer.

**Förutsättningar:** En aktiv Aspose Cloud-konto, ett giltigt JWT-åtkomsttoken och de Excel-filer som ska laddas upp.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameternamn      | Typ    | Plats            | Beskrivning                                   |
| ------------------ | ------ | ---------------- | --------------------------------------------- |
| file               | fil    | formData         | Den Excel-fil som ska laddas upp.             |
| DocumentProperties | objekt | HTTP-body (JSON) | Dokumentegenskaper som ska ställas in för Excel-filen. |

**Anteckningar:** Du kan ladda upp upp till 10 filer i en enda begäran. De som stöds inkluderar `.xlsx`, `.xls` och `.csv`. Den totala storleken på begäran får inte överskrida 100 MB.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PostMetadata) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

Begäran kräver ett **Authorization**-huvud med en Bearer JWT-token. Se till att token genereras med dina Aspose Cloud-klientuppgifter.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Molnsdk-familj

Att använda en sdk är det bästa sättet att påskynda utvecklingen. En sdk hanterar detaljer på låg nivå, så att du kan fokusera på dina projekts uppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även:**  
- [Hämta metadata](/metadata/get/)  
- [Ta bort metadata](/metadata/delete/)  
---