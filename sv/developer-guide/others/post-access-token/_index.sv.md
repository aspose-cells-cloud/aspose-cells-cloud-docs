---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Dokument"
ArticleTitle: "Hämta åtkomsttoken med klient-ID och hemlighet"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, moln, åtkomsttoken, OAuth2, API, autentisering, REST, Excel, Office Cloud"
description: "Skaffa en OAuth2-åtkomsttoken för Aspose.Cells Cloud genom att anropa slutpunkten POST /cells/connect/token med ditt klient-ID och din hemlighet."
weight: 100
---

Hämta en åtkomsttoken med Cells Cloud Get Token API med ett klient-ID och en hemlighet.

## Post Access Token API

Innan du anropar slutpunkten, se till att du har:

* Ett registrerat Aspose Cloud-konto.  
* Ett **klient-ID** och en **klienthemlighet** som genererats i Aspose Cloud-portal.  

### Web-API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ   | Plats                         | Beskrivning                                           |
| ------------- | ----- | ----------------------------- | ----------------------------------------------------- |
| grant_type    | sträng | brödtext (form‑url‑encoded)   | Fixt värde `client_credentials` som krävs för OAuth. |
| client_id     | sträng | brödtext (form‑url‑encoded)   | Klientidentifieraren som utfärdats till dig.         |
| client_secret | sträng | brödtext (form‑url‑encoded)   | Hemligheten kopplad till klient-ID:t.                |

**Exempel på begäran (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=DITT_KLIENT_ID&client_secret=DIN_KLIENTHEMLIGHET"
```

### Svar

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**HTTP-statuskoder**

| Kod | Meningsinnehåll            | Beskrivning                                      |
|-----|----------------------------|--------------------------------------------------|
| 200 | OK                         | Filter tillämpades framgångsrikt; svaret innehåller åtgärd detaljer. |
| 400 | Felaktig begäran           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktorisering              | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast         | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel          | Oväntat serverfel. |

**Exempel på felhantering**

```json
{
  "error": "invalid_client",
  "error_description": "Klientautentisering misslyckades."
}
```

## Hur man använder Get public key API med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att komma igång. SDK:et abstraherar de underliggande HTTP-detaljerna, vilket gör att du kan hämta en åtkomsttoken för Cells med minimal kod.

Kolla in [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er. En SDK tar hand om detaljer på lågnivå så att du kan fokusera på dina projektuppgifter.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:  
---