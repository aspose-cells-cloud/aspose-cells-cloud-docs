---
title: "Operazioni su Fogli di Calcolo"
second_title: "Documento"
type: docs
url: /spreadsheet-operations/
keywords: "Aspose Cells Cloud, API Excel, operazioni su fogli di calcolo, adattamento automatico, elaborazione in batch, protezione file, conversione, importazione/esportazione, elaborazione testo"
description: "Scopri come eseguire operazioni su fogli di calcolo come l'adattamento automatico, la conversione in batch, la protezione, la fusione e la sostituzione di testo utilizzando l'API REST di Aspose.Cells Cloud. Include note d'uso concise e suggerimenti con esempi di codice."
weight: 100
ArticleTitle: "Operazioni su Fogli di Calcolo – Guida all'API Aspose.Cells Cloud"
---

Le **Operazioni su Fogli di Calcolo** offrono una guida concise alle azioni più comuni che puoi eseguire sui workbook Excel con **Aspose.Cells Cloud** (v3.0). Che tu debba eseguire l'adattamento automatico delle colonne, elaborare più file in batch, proteggere i fogli di lavoro o manipolare il testo, l'API REST offre endpoint dedicati che funzionano in linguaggi come Python, C# e Java. L'elenco sottostante fornisce il link alla documentazione dettagliata per ogni operazione e include una breve nota d'uso per aiutarti a iniziare rapidamente.

**Prerequisiti**: Per chiamare questi endpoint devi disporre di una chiave API valida di Aspose.Cells Cloud e includere l'header `Authorization` (`Bearer <access-token>`). Gli esempi presuppongono la versione API v3.0.

- **[Opzioni di Adattamento Automatico](/cells/auto-fitter-options/)** – Regola automaticamente la larghezza delle colonne e l’altezza delle righe. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Elaborazione in batch di file Excel: conversione, blocco, protezione, divisione e sblocco](/cells/batch/)** – Esegui azioni in blocco (conversione, blocco, protezione, divisione, sblocco) su fino a 100 file per richiesta. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Comprimi e ripara file Excel](/cells/compress-and-repair-excel-files/)** – Riduce le dimensioni del file e risolve problemi strutturali. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Converti un file Excel in un altro formato o salvalo in modo differente](/cells/conversion-and-save-as/)** – Converti Excel in PDF, CSV, HTML, ecc., o cambia il formato di output. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[Opzioni per la conversione del workbook](/cells/convert-workbook-options/)** – Regola con precisione le impostazioni di conversione, come dimensioni della pagina, opzioni di rendering e protezione tramite password. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Crea file Excel o generare report Excel](/cells/creating-files-and-reports/)** – Genera nuovi workbook da zero o da modelli. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Vendite Q1", "value": 12345 }
  }
  ```
- **[Importa dati in file Excel ed esporta dati da file Excel](/cells/data-import-and-export/)** – Carica dati da CSV, JSON o database ed esporta dati dai fogli di lavoro. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Cifra, decifra e firma digitalmente file Excel](/cells/protect/)** – Applica protezione tramite password, crittografia o firme digitali. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[Informazioni sul file](/cells/file-info/)** – Recupera metadati come dimensione, formato e data di creazione. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Fondi e dividi file Excel](/cells/merge-and-split/)** – Combina più workbook in un unico file oppure dividi un workbook in file separati. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Cerca e sostituisci contenuti di testo all'interno dei file Excel](/cells/search-and-replace/)** – Trova e sostituisci stringhe in più fogli di lavoro. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Bozza",
    "newText": "Finale",
    "options": { "matchCase": false }
  }
  ```
- **[Elaborazione testo in Excel: aggiungi testo, rimuovi caratteri, tronca testo, aggiorna maiuscole/minuscole e altro](/cells/text-processing/)** – Esegui manipolazioni avanzate sui valori delle celle. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Inserisci filigrane o imposta sfondi nei file Excel](/cells/watermark-and-background/)** – Aggiungi filigrane di testo o immagine e imposta gli sfondi dei fogli di lavoro. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidenziale",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Lavorare con file Excel: calcolo formule, adattamento automatico, pulizia oggetti, ecc.](/cells/workbook/)** – Esegui compiti comuni sui workbook come il calcolo delle formule, la pulizia degli oggetti e l’adattamento automatico. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```