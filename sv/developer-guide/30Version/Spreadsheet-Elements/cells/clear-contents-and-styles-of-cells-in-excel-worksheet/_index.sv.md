---
title: "Rensa innehåll och stilar i celler i ett Excel-ark"
type: docs
url: /sv/clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
keywords:
  - Aspose.Cells
  - Excel API
  - rensa cellinnehåll
  - rensa cellstilar
  - moln kalkylark
  - REST API
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att rensa cellinnehåll och stilar i ett Excel-ark, med cURL-exempel och SDK-kodstycken."
ArticleTitle: "Rensa innehåll och stilar i celler i ett Excel-ark – Aspose.Cells Cloud API"
---

Innan du använder **Clear Contents and Styles**-ändpunkten, se till att du har:

* En giltig **JWT-token** som du har hämtat från Aspose.Cells Cloud-autentiseringsflödet.  
* Arbetsboken uppladdad till din valda lagringsplats (eller tillgänglig via `folder`-parametern).  
* Den nödvändiga SDK-versionen installerad om du föredrar att arbeta med någon av de språkspecifika klientbiblioteken.

Denna REST API rensar cellernas innehåll i en Excel-fil.

## PostClearContents API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                    | Beskrivning                                           |
|-----|------------------------------|-------------------------------------------------------|
| 200 | OK                           | Filter tillämpades framgångsrikt; svaret innehåller detaljer om åtgärden. |
| 400 | Felaktig förfrågan           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering saknas         | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel            | Oväntat serverfel. |

## Hur du använder PostClearContents API med SDK:er

### PostClearContents API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Rensa innehåll och stilar i celler i ett Excel-ark",
  "description": "Hur du använder Aspose.Cells Cloud REST API för att rensa cellinnehåll och stilar i ett Excel-ark.",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2023-07-08",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud – Rensa innehåll och stilar i celler"
    }
  },
  "keywords": "Aspose.Cells, Excel API, rensa cellinnehåll, rensa cellstilar, REST API, moln kalkylark"
}
</script>