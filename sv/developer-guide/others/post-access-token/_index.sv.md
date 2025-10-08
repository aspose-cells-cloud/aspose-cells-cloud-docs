---
title: Aspose.Cells Molnwebb API - Åtkomsttoke för post
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Åtkomsttoke för post
type: docs
url: /sv/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Hämta en åtkomsttoken med hjälp av Cells Cloud Get Token API, som fungerar som en proxytjänst som vidarebefordrar användarförfrågningar till Aspose Cloud-autentiseringsservern och returnerar den resulterande åtkomsttoken till klienten på ett säkert sätt.
weight: 100
kwords: Excel, Office Moln, REST API, Autentisering, Tokenhantering, Middleware-integration, Säker API, Aspose Moln
---
Hämta en åtkomsttoken med hjälp av Cells Cloud Get Token API med klient-ID och hemlighet.

## **Åtkomsttoken för post API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| Klient-ID| sträng| fråga| Klient-ID|
| Klienthemlighet| sträng| fråga| Klienthemlighet|

### **Svar**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## Så här använder du Get public key API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att accelerera utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera en åtkomsttoken för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.nt. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
