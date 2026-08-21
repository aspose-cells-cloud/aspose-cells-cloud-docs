---
title: "Aspose.Cells Cloud Excel Textsökning Web API – Sök efter text i fjärrarbetsblad"
second_title: "Dokument"
ArticleTitle: "Sök efter text i fjärrarbetsblad i Excel-kalkylark – Hitta specifik data"
linktitle: "Sök i innehåll i fjärrarbetsblad"
type: docs
url: /sv/search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, textsökning, fjärrarbetsblad"
description: "Sök efter text, siffror eller formler i ett fjärrkalkylblad med Aspose.Cells Cloud API. Stöder skiftlägesokänslig sökning och lösenordsskyddade filer."
weight: 100
---

## **Sök i innehåll i fjärrarbetsblad**

Sök programmatiskt efter specifik text i valfritt Excel-kalkylblad med Aspose.Cells Cloud API. Tjänsten kan hitta text, siffror eller formler i filer som lagras i molnlagring, vilket möjliggör automatiserade arbetsflöden för dataupptäckt, innehållsanalys och granskning av kalkylark.

### **Webb-API**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Förfrågningsparametrar**

| Parameternamn | Typ    | Path/Query String/HTTP Body | Beskrivning                                                                                       |
| ------------- | ------ | --------------------------- | ------------------------------------------------------------------------------------------------- |
| name          | String | Path                        | **Obligatoriskt.** Filnamnet på målkalkylarket (t.ex. `annual_report.xlsx`).                     |
| worksheet     | String | Path                        | **Obligatoriskt.** Kalkylbladet i kalkylarket där sökningen ska utföras.                         |
| searchText    | String | Query                       | **Obligatoriskt.** Den exakta textsträngen eller siffran som ska hittas.                          |
| ignoreCase    | Boolean| Query                       | **Valfritt.** När värdet är `true` är sökningen skiftlägesokänslig. Standard är `false`.          |
| folder        | String | Query                       | **Valfritt.** Sökvägen till mappen som innehåller kalkylarket. Om utelämnas används rotmappen.    |
| storageName   | String | Query                       | **Valfritt.** Namnet på en anpassad konfigurerad molnlagring. Om utelämnas används standardlagring.|
| region        | String | Query                       | **Valfritt.** Språkinställning (t.ex. `sv-SE`) som kan påverka textjämförelse.                   |
| password      | String | Query                       | **Valfritt.** Lösenord för ett lösenordsskyddat kalkylark. Utelämna om filen inte är krypterad.   |

### **Svar**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Array med matchningar. Varje post innehåller cellens adress (`cellName`), den matchade strängen (`text`) och hur många gånger den förekommer i cellen (`occurrences`).
- **code** – HTTP-statuskod som returneras av tjänsten.
- **status** – Textuell beskrivning av resultatet.

### **Felkoder**

- **400 Bad Request** – Ogiltig API-URI eller felaktigt formade parametrar.
- **401 Unauthorized** – Saknad eller ogiltig OAuth 2.0-token.
- **404 Not Found** – Kalkylarket eller kalkylbladet kan inte hittas.
- **500 Server Error** – Ett oväntat tillstånd uppstod vid bearbetning av förfrågan.

## Var bör vi använda sökning i innehåll i kalkylbladet med Spreadsheet API?

- **Granskning av kalkylark för efterlevnad:** Hitta känsliga termer (t.ex. "Konfidentiellt") snabbt i hela filen.
- **Korsbladad datakoppling:** Hitta ett projektnummer eller ett kundnamn som förekommer på flera blad.
- **Mallverifiering:** Efter att rapporter har genererats, bekräfta att platshållare som `{{Date}}` har ersatts.
- **Historisk datamining:** Sök efter specifika händelsekoder i äldre kalkylark för att förstå tidigare affärslogik.

## Varför bör du använda sökning i innehåll i kalkylbladet med Spreadsheet API?

- **Utvecklarvänligt:** SDK:er för många språk accelererar utvecklingen och är helt dokumenterade.
- **Lägre arbetskostnad:** Minskar behovet av personal som håller sig till manuell datakonsolidering.
- **Betala för användning:** Du betalar endast för de API-anrop som du faktiskt gör.
- **Ingen underhållsarbete:** Inga servrar att hantera, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.
- **Bevarar avancerat Excel-format** vid export av resultat till PDF eller andra format.

## Hur man använder sökning efter trasiga länkar i kalkylbladet med Spreadsheet API med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att accelerera utvecklingen. SDK hanterar de underliggande detaljerna, så att du enkelt kan implementera sökning i innehåll i kalkylblad för kalkylark med minimal kod. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.