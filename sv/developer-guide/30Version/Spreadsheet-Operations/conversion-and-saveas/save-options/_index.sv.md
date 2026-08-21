---
title: "Sparalternativ"
second_title: "Dokument"
linktype: "Sparalternativ"
type: docs
url: /sv/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Arbetsbok, REST API, Filformat, PDF, CSV, JSON, HTTP-komprimering, Diagramcache, Namnade intervall, Mappskapande"
description: "Beskriver SaveOptions-egenskaperna i Aspose.Cells Cloud REST API, vilket möjliggör utvecklare att konfigurera beteende för sparande av arbetsböcker över flera filformat och alternativ såsom HTTP-komprimering, uppdatering av diagramcache och automatiskt mappskapande."
weight: 79
ArticleTitle: "Sparalternativ – Aspose.Cells Cloud REST API-dokumentation"
---

# SaveOptions-egenskaper

SaveOptions möjliggör kontroll över hur en arbetsbok sparas vid användning av Aspose.Cells Cloud REST API. Genom att konfigurera dessa alternativ kan du aktivera HTTP-komprimering, ange utdatafilformat, hantera temporär lagring och styra ytterligare beteenden såsom uppdatering av diagramcache och automatiskt mappskapande.

**Förutsättningar**  
- En autentiserad Aspose.Cells Cloud-session (OAuth 2.0 eller JWT).  
- Målarbetsboken måste laddas eller skapas via API:et före sparning.

| Namn                      | Typ        | Beskrivning                                                                                      | Anteckningar      |
| ------------------------- | ---------- | ------------------------------------------------------------------------------------------------ | ----------------- |
| **EnableHTTPCompression** | **bool?**  | Aktiverar HTTP-komprimering för svaret.                                                          | [valfritt]        |
| **SaveFormat**            | **string** | Anger målfilformatet för sparande av arbetsboken.                                                 | [valfritt]        |
| **ClearData**             | **bool?**  | Gör arbetsboken tom efter filsparande.                                                            | [valfritt]        |
| **CachedFileFolder**      | **string** | Den mapp som används för temporär lagring av stora data.                                          | [valfritt]        |
| **ValidateMergedAreas**   | **bool?**  | Anger om sammanfogade områden ska valideras före filsparande. Standardvärdet är false.            | [valfritt]        |
| **RefreshChartCache**     | **bool?**  | Uppdaterar diagramcache-data före sparande.                                                       | [valfritt]        |
| **CreateDirectory**       | **bool?**  | Om true och mappen inte finns, skapas den automatiskt före filsparande.                           | [valfritt]        |
| **SortNames**             | **bool?**  | Sorterar namnade intervall alfabetiskt vid sparande.                                              | [valfritt]        |

**Begäran**  
- **Metod:** `POST` (eller `PUT`, beroende på åtgärd)  
- **Slutpunkt:** `/cells/workbook/save`  
- **Huvuden:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **Brödtext:** JSON-representation av `SaveOptions`-modellen (tabellen ovan) kombinerad med arbetsboksinnehållet eller referensen.

**Exempel på svar**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Arbetsboken sparades framgångsrikt."
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltigt eller saknat JWT-token. |
| 413 | Payload för stor            | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

**Anteckningar / Kommentarer**  
- När **CreateDirectory** är inställt på `true` kommer API:et automatiskt att skapa målmappen om den inte redan finns.  
- Aktivering av **EnableHTTPCompression** kan minska payload-storleken för stora arbetsböcker, men klienten måste stödja gzip/deflate-dekodning.  
- **RefreshChartCache** bör användas när diagram är beroende av dynamisk data som kan ha ändrats sedan arbetsboken skapades.