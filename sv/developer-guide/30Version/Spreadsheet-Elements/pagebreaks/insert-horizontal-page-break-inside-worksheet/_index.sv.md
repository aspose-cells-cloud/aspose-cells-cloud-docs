---
title: "Lägg till horisontell sidbrytning"
second_title: "Dokument"
linktitle: "Lägg till horisontell sidbrytning"
type: docs
url: /sv/page-breaks/add-horizontal-page-break/
aliases: [  /sv/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "horisontell sidbrytning, Aspose.Cells Cloud, Excel API, REST, SDK, kalkylblad, cURL"
description: "Lär dig hur du lägger till en horisontell sidbrytning i ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Inkluderar begärandetext detaljer, ett cURL-exempel och SDK-kodfragment för flera programmeringsspråk."
weight: 30
ArticleTitle: "Lägg till horisontell sidbrytning – Aspose.Cells Cloud API"
---

**Lägg till horisontell sidbrytning**-API:et infogar en horisontell sidbrytning i ett Excel-kalkylblad.

**Förutsättningar och autentisering**  
Ett giltigt JWT-token krävs för alla anrop till Aspose.Cells Cloud API. Skaffa token via OAuth 2.0-flödet som beskrivs i autentiseringsguiden och inkludera den i begärandehuvudet som `Authorization: Bearer <jwt token>`. Målarkalkylbladet måste finnas på en lagringsplats som API:et har tillgång till (standardlagring eller en anpassad `storageName` som du anger).

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparameterar

| Parameter Name | Typ     | Plats  | Beskrivning                                                              |
| -------------- | ------- | ------ | ------------------------------------------------------------------------ |
| name           | string  | path   | Namn på Excel-filen.                                                    |
| sheetName      | string  | path   | Namn på kalkylbladet där brytningen ska läggas till.                   |
| cellname       | string  | query  | Cellreferens (t.ex. **A1**) som markerar början av sidbrytningen.      |
| row            | integer | query  | Nollbaserat radindex för sidbrytningen.                                 |
| column         | integer | query  | Nollbaserat kolumnindex för sidbrytningen.                              |
| startColumn    | integer | query  | Startkolumn för ett intervall vid infogning av brytning.               |
| endColumn      | integer | query  | Slutkolumn för ett intervall vid infogning av brytning.                |
| folder         | string  | query  | Mappväg som innehåller Excel-filen.                                    |
| storageName    | string  | query  | Namn på Aspose Cloud-lagringen.                                         |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt gränssnitt som låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för att säkerställa krypterad kommunikation
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
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

Exempel på ett felsvar när JWT-token saknas eller är ogiltig:

```json
{
  "Code": 401,
  "Status": "Obehörig",
  "Message": "Ogiltig eller saknad JWT-token."
}
```

**HTTP-statuskoder**

| Kod | Betydelse                  | Beskrivning                                             |
|-----|----------------------------|---------------------------------------------------------|
| 200 | OK                         | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                   | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast         | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel          | Oväntat serverfel.                                      |

För mer information om relaterade åtgärder, se API-sidorna för **[Hämta horisontella sidbrytningar](../get-horizontal-page-breaks/)** och **[Ta bort horisontell sidbrytning](../delete-horizontal-page-break/)**.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}