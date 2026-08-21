---
title: "Aspose.Cells Cloud – Kontrollera tjänstens hälsa (API)"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud-hälsokontroll"
linktype: "Kontrollera hälsostatus för molntjänsten"
type: docs
url: /sv/check-cloud-service-health/
keywords: "Aspose.Cells Cloud, API-hälsokontroll, REST-status, övervakning av molntjänst"
description: "Övervaka Aspose.Cells Cloud-hälsotillstånd i realtid. Lär dig om GET /v4.0/cells/status/check-slutpunkten, parametrar, svarsformat och SDK-exempel."
weight: 100
---

Kontrollera hälsostatusen för Aspose.Cells Cloud-tjänster.

**Förutsättningar**  
För att kunna anropa den här slutpunkten behöver du ett giltigt Aspose Cloud-åtkomsttoken. Skaffa token genom att registrera ett program i Aspose Cloud Dashboard och använda client-id och client-secret för att begära en Bearer-token via OAuth2-tokenslutpunkten. Inkludera token i `Authorization`-hoofdet enligt nedan.

## **Kontrollera hälsotillstånd för molntjänsten**

### **Webb-API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäranparametrar**

| Parameter     | Typ    | Obligatorisk | Beskrivning                                                       |
| ------------- | ------ | ------------ | ----------------------------------------------------------------- |
| Authorization | header | Ja           | Bearer-token för autentisering (`Authorization: Bearer <token>`). |
| detail        | query  | Nej          | Ställ in till `true` för att inkludera detaljerad komponentinformation. |
| Accept        | header | Nej          | Önskat svarsformat, standard är `application/json`.              |

### **Svar**

Tjänsten returnerar ett JSON-innehåll när begäran lyckas.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Driftarbetar",
    "storage": "Driftarbetar",
    "database": "Driftarbetar"
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                             |
| --- | --------------------- | ------------------------------------------------------- |
| 200 | OK                    | Tjänsten är frisk; se JSON-exemplet ovan.               |
| 401 | Obehörig              | Ogiltig eller saknad autentiseringstoken.               |
| 503 | Tjänsten otillgänglig | Tjänsten är för närvarande sjuk eller under underhåll. |
| 4xx | Klientfel             | Felaktiga begäranparametrar eller felaktigt formatad begäran. |
| 5xx | Serverfel             | Oväntat serverfel; försök igen senare.                  |

## Hur du använder Aspose.Cells Cloud-status-API:t med SDK:er

### OpenAPI-specifikation

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI-specifikation</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att snabba upp utvecklingen. SDK:en hanterar de underliggande detaljerna, vilket gör att du kan implementera en hälsokontroll för Cells med minimal kod.  
Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förteckningen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Nedan finns exempel på kodstycken som visar hur du anropar hälsokontrollslutpunkten med de vanligaste SDK:erna.

---