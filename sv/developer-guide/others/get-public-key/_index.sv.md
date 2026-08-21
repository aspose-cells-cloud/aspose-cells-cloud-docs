---
---
title: "Aspose.Cells Cloud API – Hämta offentlig nyckel (v4.0) | REST-dokumentation"
secondtitle: "Dokument"
articletitle: "Hämta offentlig nyckel"
linktitle: "Hämta offentlig nyckel"
type: docs
url: /sv/get-public-key/
keywords: "Aspose.Cells, offentlig nyckel, RSA, API, moln"
description: "Hämta den RSA-offentliga nyckel som används för kryptering av data med Aspose.Cells Cloud. Innehåller endpoint, parametrar, exempel på begäran/svar, statuskoder och exempel på hur SDK:er används."
weight: 100
---

Denna API hämtar den offentliga nyckeln från ett asymmetriskt kryptografiskt algoritmsystem.

**Sammanfattning:** Använd Aspose.Cells API för att hämta offentlig nyckel för att erhålla den RSA-offentliga nyckeln (2048-bitars) som krävs för att kryptera data när du arbetar med Excel-filer i molnet. Endpoint returnerar nyckeln i JSON-format och är säkrad med OAuth 2.0.

## **API för att hämta offentlig nyckel**

**Förutsättningar:**  
För att kunna anropa denna endpoint måste du först ha ett giltigt OAuth 2.0-åtkomsttoken som innehåller scope:et `Cells.Read`.

### **Webb-API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Exempel på begäran (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäranparametrar:**

| Parameternamn | Typ   | Plats  | Beskrivning                                                                     |
| ------------- | ----- | ------ | ------------------------------------------------------------------------------- |
| Authorization | string | Header | Bearer-token för OAuth2-autentisering (obligatoriskt).                          |
| Accept        | string | Header | Önskat svarsformat, t.ex. `application/json` (valfritt, standard är JSON).      |

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request (Felaktig begäran) | Saknade eller ogiltiga parametrar (t.ex. filformat som inte stöds). |
| 401 | Unauthorized (Ej auktoriserad) | Ogiltig eller saknad JWT-token.                                  |
| 413 | Payload Too Large (För stor nyttolast) | Den uppladdade filen överskrider storleksgränsen.             |
| 500 | Internal Server Error (Internt serverfel) | Oväntat serverfel.                                              |

## Hur du använder API:et för att hämta offentlig nyckel med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör det möjligt för dig att utföra REST-interaktioner direkt från din webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna så att du bara behöver implementera hämtning av offentlig nyckel för cells med minimal kod.  
Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Här följer konkreta exempel för de vanligaste programmeringsspråken:

---