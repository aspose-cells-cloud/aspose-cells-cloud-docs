---
title: "Lavorare con la formattazione condizionale di Excel"
second_title: "Documento"
linktitle: "Formattazione condizionale"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, Formattazione condizionale, Aspose.Cells Cloud, API"
description: "L'API Aspose.Cells Cloud per Excel fornisce endpoint per recuperare, aggiungere, modificare ed eliminare le regole di formattazione condizionale, consentendo un'analisi visiva dinamica dei dati del foglio di calcolo."
weight: 100
ArticleTitle: "Lavorare con la formattazione condizionale di Excel – Guida API"
---

La formattazione condizionale in Excel consente di evidenziare le celle con un colore specifico in base al valore della cella stessa.

Utilizza la formattazione condizionale per esplorare e analizzare visivamente i dati, rilevare problemi critici e identificare modelli e tendenze.

La formattazione condizionale facilita l'evidenziazione di celle o intervalli di celle interessanti, l'enfasi su valori insoliti e la visualizzazione dei dati mediante barre dei dati, scale di colori e set di icone che corrispondono a specifiche variazioni nei dati.

Una formattazione condizionale modifica l'aspetto delle celle in base alle condizioni specificate. Se le condizioni sono vere, l'intervallo di celle viene formattato; se le condizioni sono false, l'intervallo di celle rimane invariato. Sono disponibili molte condizioni predefinite e puoi anche crearne di personalizzati (inclusi quelli che utilizzano una formula che restituisce **VERO** o **FALSO**).

L'API Aspose.Cells Cloud fornisce un insieme di endpoint per gestire le regole di formattazione condizionale in modo programmatico. Le seguenti operazioni sono disponibili:

- **Ottieni formattazioni condizionali del foglio di calcolo** – Recupera tutte le regole di formattazione condizionale applicate a un foglio di calcolo.  
  - **Metodo:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Parametri:** `fileName` (stringa, obbligatorio), `sheetName` (stringa, obbligatorio), parametri facoltativi di query come `folder`, `storageName`  
  - **Esempio cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Ottieni formattazione condizionale** – Restituisce una specifica regola di formattazione condizionale tramite il suo identificatore.  
  - **Metodo:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Parametri:** `index` (intero, obbligatorio) identifica la posizione della regola.  
  - **Esempio cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Aggiungi area di celle per la condizione di formattazione** – Aggiunge un intervallo di celle che verrà interessato dalla formattazione condizionale specificata.  
  - **Metodo:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Corpo della richiesta (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Esempio cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Aggiungi condizione per la condizione di formattazione** – Definisce una nuova condizione (ad esempio, valore o formula) per una regola di formattazione esistente.  
  - **Metodo:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Corpo della richiesta (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Esempio cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Aggiungi condizione di formattazione** – Crea una regola completa di formattazione condizionale, inclusi tipo e stile.  
  - **Metodo:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Corpo della richiesta (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Esempio cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Cancella tutte le formattazioni condizionali** – Rimuove tutte le regole di formattazione condizionale dal foglio di calcolo di destinazione.  
  - **Metodo:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Esempio cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Rimuovi area di celle dalla formattazione condizionale** – Elimina un'area di celle precedentemente definita da una regola di formattazione condizionale.  
  - **Metodo:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Esempio cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Rimuovi formattazione condizionale** – Elimina un'intera regola di formattazione condizionale dal foglio di calcolo.  
  - **Metodo:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Esempio cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Questi esempi illustrano il metodo HTTP richiesto, il modello di URL, i parametri chiave e i payload di richiesta di esempio per ciascuna operazione. Utilizza l'SDK appropriato (C#, Java, Python, ecc.) per snippet di codice specifici del linguaggio, se preferito.