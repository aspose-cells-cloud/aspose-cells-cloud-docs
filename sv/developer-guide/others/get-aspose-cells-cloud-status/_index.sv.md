---
title: "Aspose.Cells Cloud Web API – Hämta status för Aspose Cells Cloud"
second_title: "Dokument"
ArticleTitle: "Hämta status för Aspose Cells Cloud"
linktitle: "Hämta status för Aspose Cells Cloud"
type: docs
url: /sv/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud API, hälsokontroll, Excel, REST"
description: "Övervaka hälsostatus för Aspose.Cells Cloud-tjänsten i realtid."
weight: 100
---

Hämta hälsostatus för Aspose.Cells Cloud-tjänsten i realtid.

**Förutsättningar:** För att anropa denna API måste du skaffa ett Bearer-åtkomsttoken med dina Aspose Cloud-klientuppgifter. Inkludera token i `Authorization`-huvudet som `Bearer {access_token}`.

## **Hämta status för Aspose.Cells Cloud**

### **Webb-API**

Slutpunkten använder HTTP-metoden **GET** och kräver inget begärandetextinnehåll.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar:**

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-begärandetext | Beskrivning                                |
| ------------- | ----- | ------------------------------------- | ------------------------------------------ |
| Authorization | String | Header                               | Bearer-token för autentisering (obligatorisk). |
| format        | String | Fråga                                 | Önskat svarsformat, t.ex. `json`.          |

### **Svar**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Svarschema**

| Fält      | Typ               | Beskrivning                                |
| --------- | ----------------- | ------------------------------------------ |
| status    | string            | Tjänstens hälsostatus (`OK`, `Degraded`, etc.). |
| service   | string            | Namn på tjänsten.                          |
| timestamp | string (ISO‑8601) | Tidpunkten för hälsokontrollen.            |

API:et returnerar ett standard-JSON-svar som innehåller den aktuella hälsostatusen för Aspose.Cells Cloud-tjänsten.

**HTTP-statuskoder**

- **200 OK** – Tjänsten är i ordentligt skick och svaret innehåller statusinformationen.
- **401 Unauthorized** – Saknar eller ogiltig autentiseringstoken.
- **503 Service Unavailable** – Tjänsten är för tillfället nere för underhåll eller upplever problem.

## Hur man använder API:et för att hämta status för Aspose.Cells Cloud med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Genom att använda SDK:n förenklas integrationen och minskar mängden kod som behöver skrivas. SDK:n hanterar de underliggande detaljerna, så att du med minimal ansträngning kan hämta körstatusen för Aspose.Cells Cloud. Se [GitHub-förvaret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.