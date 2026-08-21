---
title: "Lavorare con le righe di Excel – API Cloud di Aspose.Cells"
ArticleTitle: "Lavorare con le righe di Excel – API Cloud di Aspose.Cells"
second_title: "Documento"
linktitle: "Righe"
type: docs
url: /it/rows/
aliases: [  /it/working-with-rows/ ]
keywords: "Aspose.Cells, righe Excel, API REST, manipolazione di fogli elettronici"
description: "Manipola le righe nei file Excel utilizzando l’API REST di Aspose.Cells Cloud. Supporta Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift."
weight: 100
---

## Lavorare con le righe in un file Excel

**Ultimo aggiornamento: luglio 2026**

- [Come ottenere informazioni su una riga in un foglio di calcolo Excel.](/cells/rows/get/row/)
- [Come aggiungere una riga vuota in un foglio di calcolo Excel.](/cells/rows/add/row/)
- [Come copiare righe in un foglio di calcolo Excel.](/cells/rows/copy/)
- [Come nascondere righe in un foglio di calcolo Excel.](/cells/rows/hide/)
- [Come mostrare righe precedentemente nascoste in un foglio di calcolo Excel.](/cells/rows/unhide/)
- [Come raggruppare righe in un foglio di calcolo Excel.](/cells/rows/group/)
- [Come scindere un raggruppamento di righe in un foglio di calcolo Excel.](/cells/rows/ungroup/)
- [Come eliminare una riga da un foglio di calcolo](/cells/rows/delete/)

Riferimento rapido all’API per le operazioni comuni sulle righe:

| Operazione          | Metodo HTTP | Endpoint                                                               | Parametri chiave                       |
|---------------------|-------------|------------------------------------------------------------------------|----------------------------------------|
| [Ottieni riga](https://docs.aspose.cloud/cells/rows/get/row/)     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Aggiungi riga](https://docs.aspose.cloud/cells/rows/add/row/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [Copia righe](https://docs.aspose.cloud/cells/rows/copy/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Elimina riga](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Nascondi righe](https://docs.aspose.cloud/cells/rows/hide/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [Mostra righe](https://docs.aspose.cloud/cells/rows/unhide/)  | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [Raggruppa righe](https://docs.aspose.cloud/cells/rows/group/)    | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [Scindere raggruppamento righe](https://docs.aspose.cloud/cells/rows/ungroup/)| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**Dettagli richiesta / risposta**

- **Ottieni riga**  
  *Richiesta*: Nessun corpo richiesto.  
  *Risposta (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Errori*: 400 Bad Request (indice non valido), 404 Not Found (file o foglio mancante).

- **Aggiungi riga**  
  *Corpo richiesta (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Risposta (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Errori*: 400 Bad Request (parametri mancanti o non validi), 401 Unauthorized.

- **Copia righe**  
  *Corpo richiesta (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Risposta (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Errori*: 400 Bad Request, 404 Not Found.

- **Elimina riga**  
  *Richiesta*: Nessun corpo.  
  *Risposta (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Errori*: 400 Bad Request, 404 Not Found.

- **Nascondi righe**  
  *Corpo richiesta (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Risposta (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Errori*: 400 Bad Request.

- **Mostra righe** – stesso payload di *Nascondi righe*; risposta identica, stato “Rows unhidden”.

- **Raggruppa righe** – stesso payload di *Nascondi righe*; stato della risposta “Rows grouped”.

- **Scindere raggruppamento righe** – stesso payload di *Nascondi righe*; stato della risposta “Rows ungrouped”.

Tutte le operazioni richiedono un token di accesso OAuth 2.0/JWT valido e una versione dell'SDK appropriata.