---
title: "Lägg till en digital signatur i en Excel-arbetsbok"
ArticleTitle: "Lägg till en digital signatur i en Excel-arbetsbok – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Digital signatur"
type: docs
url: /sv/excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, digital signatur, Excel-arbetsbok, REST API, .pfx, JWT, signatur-API"
description: "Lär dig hur du lägger till en digital signatur i en Excel-arbetsbok med Aspose.Cells Cloud REST API (v4.0). Inkluderar slutpunkt, parametrar, autentisering, svarsschema, felhantering och SDK-exempel för flera språk."
weight: 35
---


**Förutsättningar:**  
Innan du anropar denna slutpunkt ska du säkerställa att du har:

- En giltig JWT-åtkomsttoken som du har fått via Aspose Cloud-autentisering.  
- Målarbetsboken redan uppladdad till ditt Aspose Cloud-lager.  
- En digital signaturfil i formatet `.pfx` eller `.p12` samt dess lösenord.

Detta REST API lägger till en **digital signatur** i en Excel-arbetsbok.

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:en är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameter Namn          | Typ    | Plats                | Beskrivning                                             |
| ------------------------ | ------ | -------------------- | ------------------------------------------------------- |
| **name**                 | string | `<code>path</code>`  | Namnet på arbetsboken.                                  |
| **digitalsignaturefile** | string | `<code>query</code>` | Sökvägen till den digitala signaturfilen (`.pfx` eller `.p12`). |
| **password**             | string | `<code>query</code>` | Lösenord för arbetsboken, om den är skyddad.            |
| **folder**               | string | `<code>query</code>` | Mapp där arbetsboken lagras.                            |
| **storageName**          | string | `<code>query</code>` | Namn på det lagringstjänst som ska användas.            |

*Obs: Om filnamnet innehåller specialtecken ska du URL-koda det innan du lägger till det i frågesträngen.*

### Felhantering

| HTTP-status | Betydelse                                               |
| ----------- | ------------------------------------------------------- |
| 200         | Signatur tillagd utan problem.                          |
| 400         | Felaktig begäran – saknade eller ogiltiga parametrar.   |
| 401         | Auktoriseringsfel – ogiltig eller utgången OAuth-token. |
| 403         | Åtkomst nekad – otillräckliga rättigheter eller nekad åtkomst. |
| 500         | Internt serverfel – oväntat fel.                        |

### HTTP-status och felaktiga svarsmeddelanden

| HTTP-status | Kod                 | Beskrivning                                                |
| ----------- | ------------------- | ---------------------------------------------------------- |
| 400         | BadRequest          | Saknade eller ogiltiga parametrar.                         |
| 401         | Unauthorized        | Ogiltig eller saknad åtkomsttoken.                         |
| 404         | NotFound            | Den angivna arbetsboken hittades inte i den givna mappen/lagret. |
| 500         | InternalServerError | Oväntat serverfel.                                         |


## Hur du använder PostDigitalSignature API med SDK:er

### PostDigitalSignature API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att anropa Aspose.Cells-webbtjänster. Exemplet nedan visar en begäran till API:et:

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
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

**Svarsschema**  
API:et returnerar ett JSON-objekt med följande fält:

| Fält         | Typ    | Beskrivning                                           |
| ------------ | ------ | ----------------------------------------------------- |
| `Code`       | int    | HTTP-liknande statuskod som indikerar resultatet.     |
| `Status`     | string | Kort text som beskriver utfallet (t.ex. `OK`).       |
| `SignatureId`| string | Identifierare för den tillagda digitala signatur (valfritt). |
| `Message`    | string | Ytterligare information eller feldetaljer (valfritt). |

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK förenklar integrationen och minskar mängden kod som behöver skrivas. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}