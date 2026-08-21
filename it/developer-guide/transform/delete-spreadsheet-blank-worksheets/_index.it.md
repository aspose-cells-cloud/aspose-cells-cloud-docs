---
title: "Aspose.Cells Cloud Web API - Eliminazione automatica di fogli di calcolo vuoti/bianchi"
second_title: "Documento"
ArticleTitle: "Elimina tutti i fogli vuoti in Excel – Guida alla rimozione dei fogli vuoti"
linktype: "Elimina fogli di calcolo vuoti"
type: docs
url: /it/delete-spreadsheet-blank-worksheets/
keywords: "Aspose.Cells Cloud, elimina fogli di calcolo vuoti, Excel API, pulizia del workbook, ottimizzazione del foglio di calcolo"
description: "Utilizza l’API Aspose.Cells Cloud per eliminare automaticamente i fogli di calcolo vuoti o bianchi dai file Excel. Scopri come identificare e rimuovere i fogli privi di dati, formule, grafici o oggetti, migliorando le prestazioni e l’organizzazione del workbook."
weight: 100
---

Elimina automaticamente tutti i fogli di calcolo vuoti dai file Excel utilizzando l’API Aspose.Cells Cloud. La nostra API intelligente rileva e rimuove i fogli privi di dati, formule, grafici, commenti o oggetti, preservando tutti i fogli effettivamente popolati. Supporta l’elaborazione in batch, l’automazione cloud e l’integrazione senza problemi per i flussi di lavoro aziendali di pulizia dei workbook.

## **API DeleteSpreadsheetBlankWorksheets**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-worksheets
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome del parametro | Tipo   | Percorso / Stringa di query / Corpo HTTP | Descrizione                                                                                                                                                                                                                     |
| :----------------- | :----- | :---------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet        | File   | FormData                                  | **Obbligatorio**. Il file workbook Excel da pulire. Supporta formati come `.xlsx`, `.xls`, `.xlsm`, `.xlsb` e `.ods`.                                                                                                          |
| outPath            | String | Query                                     | **Facoltativo**. Il percorso della cartella di destinazione all’interno dell’archiviazione cloud in cui verrà salvato il file di output. Se lasciato vuoto o impostato su `null`, il file elaborato verrà salvato nella posizione predefinita o nella stessa directory del file sorgente. |
| outStorageName     | String | Query                                     | **Obbligatorio**. Il nome del servizio di archiviazione cloud configurato in cui deve essere salvato il file di output (ad esempio `MyFirstStorage`). Questo parametro specifica quale spazio di archiviazione utilizzare per scrivere i risultati.                         |
| region             | String | Query                                     | **Facoltativo**. L’impostazione regionale/linguistica applicata durante l’elaborazione del workbook, ad esempio `en-US` o `zh-CN`. Può influenzare la gestione di date, numeri e formati di testo.                                  |
| password           | String | Query                                     | **Facoltativo**. La password necessaria per aprire un file Excel protetto da password. Può essere omessa se il file caricato non è crittografato.                                                                                |

## **Risposta**

L’API restituisce il workbook elaborato come flusso di file.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

- **Codice di stato di successo:** `200 OK` – il workbook è stato elaborato e il file pulito viene restituito nel corpo della risposta.  
- **Content‑Type:** `application/octet-stream`

### Codici di errore

- **400 Bad Request**: URI dell’API Aspose.Cells Cloud non valido.  
- **401 Unauthorized**: Token di accesso non valido, oppure client ID o segreto non validi.  
- **404 Not Found**: Il file del foglio di calcolo non è accessibile.  
- **500 Server Error**: Si è verificata un’anomalia nel recupero dei dati di calcolo del foglio di calcolo.

## Dove utilizzare l’API Delete Spreadsheet Blank Worksheets?

- **Pulizia post-consolidamento dati**: Dopo aver combinato dati da più file di origine in un unico workbook, rimuovi automaticamente i fogli residui o di sola placeholder creati durante il processo ma privi di dati.  
- **Generazione di report basata su modelli**: In flussi di lavoro che utilizzano modelli Excel con più fogli predefiniti, pulisci tutti i fogli di modello non utilizzati dopo aver popolato solo quelli necessari con i dati.  
- **Pipeline di elaborazione dati automatizzata (ETL)**: Come passaggio di pre-elaborazione per sanificare i workbook Excel ricevuti da vari sistemi o caricamenti utente, prima dell’analisi, archiviazione o integrazione successiva, garantendo che vengano elaborati solo i fogli effettivamente contenenti dati.  
- **Ottimizzazione e migrazione di workbook legacy**: Durante l’aggiornamento o il consolidamento di vecchi file Excel spesso accumulati di numerosi fogli vuoti o obsoleti nel tempo.  
- **Portali per contenuti generati dagli utenti**: Pulisci e standardizza i workbook inviati dagli utenti tramite applicazioni web o moduli, rimuovendo i fogli vuoti accidentali per mantenere una qualità professionale e coerente dei file.  

## Perché utilizzare l’API Delete Spreadsheet Blank Worksheets?

- **Semplice per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido, accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, riduce significativamente il carico di lavoro di sviluppo.  
- **Riduzione dei costi del personale**: Riduce la necessità di figure dedicate alla consolidazione di documenti.  
- **Pay-per-use**: Nessun investimento iniziale, si paga solo per le chiamate API effettivamente utilizzate.  
- **Costi di manutenzione nulli**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.  

## Come utilizzare l’API Delete Spreadsheet Blank Worksheets con gli SDK

### Specifica dell’API Delete Spreadsheet Blank Worksheets

La [specificazione dell’API Delete Spreadsheet Blank Worksheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankWorksheets) definisce un’interfaccia di programmazione accessibile pubblicamente, consentendo di effettuare interazioni REST direttamente da un browser web.

### Utilizzo degli SDK Aspose.Cells Cloud

L’utilizzo dell’SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendo di eliminare i fogli di calcolo vuoti con poche righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l’elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankWorksheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankWorksheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankWorksheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankWorksheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankWorksheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankWorksheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankWorksheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankWorksheets.go" >}}
{{</tab>}}
{{< /tabs >}}