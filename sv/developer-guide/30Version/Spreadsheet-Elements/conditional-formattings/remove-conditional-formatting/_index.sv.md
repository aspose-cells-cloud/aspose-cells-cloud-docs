---
title: "Ta bort villkorsformatering – Aspose.Cells Cloud API-referens"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Villkorsformatering, Ta bort, API, Excel, Moln"
description: "Ta bort en villkorsformateringsregel från ett kalkylblad med Aspose.Cells Cloud REST API. Inkluderar parametrar, autentisering, exempel på begäran/svar och SDK-utdrag."
weight: 60
---

# Ta bort villkorsformatering

## Bakgrund
Villkorsformatering låter dig tillämpa visuella stilar på celler som uppfyller specifika kriterier (t.ex. markera värden större än ett tröskelvärde). I automatiseringsscenario kan du behöva ta bort en befintlig regel. Denna slutpunkt tar bort en villkorsformateringsregel från ett kalkylblad i en Excel-arbetsbok som lagras i Aspose Cloud-lagring.

## Förutsättningar
- Ett **Aspose Cloud**-konto med **Cells**-produkten aktiverad.  
- Ett **JWT-åtkomsttoken** genererat via OAuth 2.0-klientautentiseringsflödet.  
- Arbetsboken (`{name}`) måste redan finnas i den angivna **mappen** och **lagringen** (om någon finns).  
- API-version **v3.0** (standard) används i URL:erna nedan.

## Autentisering
Alla Aspose.Cells Cloud-slutpunkter kräver **JWT-tokenbaserad autentisering**.

```http
Authorization: Bearer <access_token>
```

### Skaffa en åtkomsttoken (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Svar**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Använd den returnerade `access_token` i `Authorization`-headern för varje begäran.

## HTTP-begäran

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Pathparametrar

| Namn        | Typ     | Obligatorisk | Beskrivning |
|-------------|---------|--------------|-------------|
| `name`      | sträng  | Ja           | Arbetsbokens filnamn (t.ex. `Book1.xlsx`). |
| `sheetName` | sträng  | Ja           | Kalkylbladet som innehåller villkorsformateringen. |
| `index`     | heltal  | Ja           | Nollbaserat index för villkorsformateringsregeln som ska tas bort. |

### Frågeparametrar

| Namn          | Typ    | Obligatorisk | Beskrivning |
|---------------|--------|--------------|-------------|
| `folder`      | sträng | Nej          | Molnmapp där arbetsboken finns. |
| `storageName` | sträng | Nej          | Namn på Aspose Cloud-lagrings tjänsten. |

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Lyckat svar

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                  | Beskrivning                                         |
|-----|----------------------------|-----------------------------------------------------|
| 200 | OK                         | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering saknas       | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast         | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel          | Oväntat serverfel. |

## Felaktiga svar

| HTTP-kod | Orsak | Exempel på brödtext |
|----------|-------|---------------------|
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Ogiltigt parametervärde." }` |
| **401**  | Auktorisering saknas – saknad eller ogiltig JWT-token. | `{ "Code":"401", "Message":"Åtkomsttoken saknas eller är ogiltig." }` |
| **404**  | Hittades inte – arbetsboken eller kalkylbladet finns inte. | `{ "Code":"404", "Message":"Filen hittades inte." }` |
| **500**  | Internt serverfel – oväntat serverfel. | `{ "Code":"500", "Message":"Ett oväntat fel uppstod." }` |

## SDK-exempel
Följande utdrag visar hur du anropar åtgärden **Ta bort villkorsformatering** med de officiella Aspose.Cells Cloud SDK:erna.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// Konfigurera API-klient
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Ta bort villkorsformatering
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Villkorsformatering borttagen.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Villkorsformatering borttagen.")
```

*(Ytterligare SDK-utdrag för Ruby, Go, Perl och Swift finns i [GitHub-lagret](https://github.com/aspose-cells-cloud).)*

## Se även
- **Autentiseringsguide** – [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI-specifikation** – Detaljerad schemadefinition för denna slutpunkt (öppnas i ny flik)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI-specifikation</a>`  
- **Översikt över villkorsformatering** – Lär dig hur du skapar, uppdaterar och visar formateringsregler.  
- **Aspose.Cells Cloud SDK:er** – Fullständig lista över stödda språk på [GitHub-lagret](https://github.com/aspose-cells-cloud).  

---  

*Den här sidan följer standardmallen för Aspose.Cells Cloud API-dokumentation, innehåller en sektion för förutsättningar och följer riktlinjer för tillgänglighet och SEO.*