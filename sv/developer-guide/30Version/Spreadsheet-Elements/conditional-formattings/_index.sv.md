---
title: "Arbeta med villkorsstyrd formatering i Excel"
second_title: "Document"
linktype: "Villkorsstyrd formatering"
type: docs
url: /sv/conditional-formattings/
aliases: [/sv/working-with-conditional-formatting/]
keywords: "Excel, villkorsstyrd formatering, Aspose.Cells Cloud, API"
description: "Aspose.Cells Cloud API för Excel tillhandahåller slutpunkter för att hämta, lägga till, ändra och ta bort regler för villkorsstyrd formatering, vilket möjliggör dynamisk visuell analys av data i kalkylblad."
weight: 100
ArticleTitle: "Arbeta med villkorsstyrd formatering i Excel – API-guide"
---

Villkorsstyrd formatering i Excel gör det möjligt att markera celler med en specifik färg beroende på cellens värde.

Använd villkorsstyrd formatering för att underlätta visuell undersökning och analys av data, upptäcka kritiska problem samt identifiera mönster och trender.

Villkorsstyrd formatering gör det enkelt att markera intressanta celler eller cellområden, understryka ovanliga värden samt visualisera data med hjälp av datarutor, färgskalor och ikonuppsättningar som motsvarar specifika variationer i data.

En villkorsstyrd formatering ändrar en cells utseende beroende på de villkor du anger. Om villkoren är sanna formateras cellområdet; om villkoren är falska förblir cellområdet oförändrat. Det finns många inbyggda villkor, och du kan även skapa egna (inklusive genom att använda en formel som utvärderas till **SANT** eller **FALSKT**).

Aspose.Cells Cloud API erbjuder en uppsättning slutpunkter för att hantera regler för villkorsstyrd formatering programmatiskt. Följande åtgärder är tillgängliga:

- **Hämta villkorsstyrda formateringar i kalkylblad** – Hämtar alla tillämpade regler för villkorsstyrd formatering i ett kalkylblad.  
  - **Metod:** `GET`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Parametrar:** `fileName` (sträng, obligatorisk), `sheetName` (sträng, obligatorisk), valfria frågeparametrar som `folder`, `storageName`  
  - **Exempel på cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Hämta villkorsstyrd formatering** – Returnerar en specifik regel för villkorsstyrd formatering med dess identifierare.  
  - **Metod:** `GET`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Parametrar:** `index` (heltal, obligatorisk) identifierar regelns position.  
  - **Exempel på cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Lägg till cellområde för formatvillkor** – Lägger till ett cellområde som den angivna villkorsstyrda formateringen ska påverka.  
  - **Metod:** `POST`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Request Body (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Exempel på cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Lägg till villkor för formatvillkor** – Definierar ett nytt villkor (t.ex. värde eller formel) för en befintlig formateringsregel.  
  - **Metod:** `POST`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Request Body (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Exempel på cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Lägg till formatvillkor** – Skapar en komplett regel för villkorsstyrd formatering, inklusive typ och stil.  
  - **Metod:** `POST`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Request Body (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Exempel på cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Rensa alla formatvillkor** – Tar bort alla regler för villkorsstyrd formatering från målkalkylbladet.  
  - **Metod:** `DELETE`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Exempel på cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Ta bort cellområde från villkorsstyrd formatering** – Tar bort ett tidigare definierat cellområde från en regel för villkorsstyrd formatering.  
  - **Metod:** `DELETE`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Exempel på cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Ta bort villkorsstyrd formatering** – Tar bort en hel regel för villkorsstyrd formatering från kalkylbladet.  
  - **Metod:** `DELETE`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Exempel på cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Dessa exempel visar den nödvändiga HTTP-metoden, URL-mönstret, viktiga parametrar samt exempel på begäransinnehåll för varje åtgärd. Använd lämpligt SDK (t.ex. C#, Java, Python etc.) för språkspecifika kodexempel om så önskas.