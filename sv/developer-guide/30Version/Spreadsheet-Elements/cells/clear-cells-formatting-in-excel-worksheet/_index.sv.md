---
title: "Rensa cellformatering i ett Excel-ark"
type: docs
url: /clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, Rensa cellformatering, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Använd Aspose.Cells Cloud REST API för att rensa cellformatering i ett Excel-ark. Innehåller begärandedetaljer, ett cURL-exempel och SDK-kodavsnitt för flera språk."
ArticleTitle: "Rensa cellformatering i ett Excel-ark - Aspose.Cells Cloud API"
---

**Obs:** Alla Aspose.Cells Cloud API-anrop måste göras över **HTTPS**. HTTP-slutpunkter är föråldrade och kan blockeras av webbläsare.

- **Metod:** POST  
- **Slutpunkt:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

Denna REST API rensar cellformatering i en Excel-fil och är en del av Aspose.Cells Cloud-svitens funktioner för att rensa cellformatering i Excel-ark.

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
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

**Svarschema**

| Fält   | Typ     | Beskrivning                                   |
|--------|---------|-----------------------------------------------|
| Code   | heltal  | HTTP-statuskod returnerad av API:et (t.ex. 200). |
| Status | sträng  | Resultat av åtgärden (`OK` vid lyckad åtgärd).   |

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostClearFormats API med SDK:er

### PostClearFormats API-specifikation

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI-specifikation</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
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

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även**

- [Rensa cellinnehåll och -stilar](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [Ange cellstil](https://docs.aspose.cloud/cells/set-cell-style)
---