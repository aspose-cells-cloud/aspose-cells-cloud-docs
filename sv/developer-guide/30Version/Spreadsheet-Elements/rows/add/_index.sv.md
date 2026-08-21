---
title: "Hur man lägger till rader i ett Excel-ark"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /sv/rows/add/
keywords: "Aspose.Cells, lägg till rader, Excel API, REST, C#, Java, Python, Node.js"
description: "Steg-för-steg-guide för att lägga till en eller flera rader i ett Excel-ark med Aspose.Cells Cloud REST API, inklusive kodexempel i C#, Java, Python och Node.js."
weight: 20
ArticleTitle: "Lägg till rader i Excel-ark med Aspose.Cells Cloud API – Steg-för-steg-guide"
---

## Hur man lägger till rader i ett Excel-ark

Detta artikeln förklarar hur du infogar en enskild tom rad eller flera rader i ett befintligt ark med Aspose.Cells Cloud REST API. Se till att du har en giltig API-nyckel och lämpligt SDK installerat innan du går vidare.

**Förutsättningar**  
- [ ] Aspose.Cells Cloud-konto med aktiv prenumeration.  
- [ ] API-nyckel/åtkomsttoken genererad från Aspose Clouds instrumentpanel.  
- [ ] Ett av de stödda SDK:erna (C#, Java, Python, Node.js) installerat och konfigurerat.  

**API-referens**  
- **HTTP-metod:** `POST`  
- **Slutpunkt:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **Obligatoriska sökvägsparametrar:**  
  - `fileName` – Namnet på Excel-filen som lagras i molnet.  
  - `sheetName` – Namnet på det ark där rader ska läggas till.  
- **Frågeparametrar:**  
  - `startrow` – Nollbaserat index för raden dit infogningen börjar.  
  - `totalRows` – Antal rader att infoga.  
  - `folder` – (Valfritt) Sökväg till mappen i molnet där filen finns.  
  - `storage` – (Valfritt) Lagringsnamn om du använder en icke-standardlagring.  
- ** Begäransinnehåll (JSON-exempel):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **cURL-exempel**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **Lyckat svar (HTTP 200):** Returnerar uppdaterad information om arket, inklusive det nya antalet rader.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Felaktigt svarsexempel (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "Ogiltig startrow-parameter. Den måste vara ett icke-negativt heltal."
  }
  ```

- **Statuskoder:**  

  | Kod | Betydelse                                 |
  |-----|-------------------------------------------|
  | 200 | Rader har lagts till utan problem         |
  | 400 | Ogiltiga parametrar eller felaktigt JSON  |
  | 401 | Autentisering misslyckades                |
  | 404 | Fil eller ark hittades inte               |
  | 500 | Serverfel                                  |

Här nedan finns snabblänkar till detaljerade exempel för att lägga till rader:

- [Hur man lägger till en tom rad i ett Excel-ark](/sv/cells/rows/add/row/)
- [Hur man lägger till flera rader i ett Excel-ark](/sv/cells/rows/add/rows/)
---