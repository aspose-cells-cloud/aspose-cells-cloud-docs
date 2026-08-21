---
---
title: "Arbeta med Excel-rader – Aspose.Cells Cloud API"
ArticleTitle: "Arbeta med Excel-rader – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Rader"
type: docs
url: /sv/rows/
aliases: [/sv/working-with-rows/]
keywords: "Aspose.Cells, Excel-rader, REST API, kalkylarkshandtering"
description: "Hantera rader i Excel-filer med Aspose.Cells Cloud REST API. Stöder Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift."
weight: 100
---

## Arbeta med rader i en Excel-fil

**Senast uppdaterad: Juli 2026**

- [Hur man hämtar radinformation i ett Excel-ark.](/sv/cells/rows/get/row/)
- [Hur man lägger till en tom rad i ett Excel-ark.](/sv/cells/rows/add/row/)
- [Hur man kopierar rader i ett Excel-ark.](/sv/cells/rows/copy/)
- [Hur man döljer rader i ett Excel-ark.](/sv/cells/rows/hide/)
- [Hur man visar dolda rader i ett Excel-ark.](/sv/cells/rows/unhide/)
- [Hur man grupperar rader i ett Excel-ark.](/sv/cells/rows/group/)
- [Hur man avgrupperar rader i ett Excel-ark.](/sv/cells/rows/ungroup/)
- [Hur man tar bort en rad från ett ark](/sv/cells/rows/delete/)

Snabb API-referens för vanliga radoperationer:

| Operation      | HTTP-metod | Endpoint                                                               | Nyckelparametrar                       |
|----------------|------------|------------------------------------------------------------------------|----------------------------------------|
| [Hämta rad](https://docs.aspose.cloud/cells/rows/get/row/)     | GET        | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Lägg till rad](https://docs.aspose.cloud/cells/rows/add/row/) | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [Kopiera rader](https://docs.aspose.cloud/cells/rows/copy/)    | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Ta bort rad](https://docs.aspose.cloud/cells/rows/delete/)    | DELETE     | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Dölj rader](https://docs.aspose.cloud/cells/rows/hide/)       | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [Visa dolda rader](https://docs.aspose.cloud/cells/rows/unhide/)| POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [Gruppera rader](https://docs.aspose.cloud/cells/rows/group/)  | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [Avgruppera rader](https://docs.aspose.cloud/cells/rows/ungroup/)| POST     | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**Detaljer för begäran/svar**

- **Hämta rad**  
  *Begäran*: Inga krav på brödtext.  
  *Svar (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Fel*: 400 Bad Request (ogiltigt index), 404 Not Found (fil eller ark saknas).

- **Lägg till rad**  
  *Begäran (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Svar (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Fel*: 400 Bad Request (saknade/ogiltiga parametrar), 401 Unauthorized.

- **Kopiera rader**  
  *Begäran (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Svar (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Fel*: 400 Bad Request, 404 Not Found.

- **Ta bort rad**  
  *Begäran*: Inga krav på brödtext.  
  *Svar (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Fel*: 400 Bad Request, 404 Not Found.

- **Dölj rader**  
  *Begäran (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Svar (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Fel*: 400 Bad Request.

- **Visa dolda rader** – samma begäran som *Dölj rader*; samma svar, status ”Rows unhidden”.

- **Gruppera rader** – samma begäran som *Dölj rader*; svar med status ”Rows grouped”.

- **Avgruppera rader** – samma begäran som *Dölj rader*; svar med status ”Rows ungrouped”.

Alla operationer kräver en giltig OAuth 2.0/JWT-åtkomsttoken och lämplig SDK-version.  

---