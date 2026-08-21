---
title: "Eliminare colonne vuote da Excel con l'API Aspose.Cells Cloud – Esempio rapido REST"
second_title: "Documenti"
ArticleTitle: "Come eliminare colonne vuote in Excel – Automatizzare la pulizia delle colonne"
linktitle: "Eliminare colonne vuote"
type: docs
url: /delete-spreadsheet-blank-columns/
keywords: "eliminare colonne vuote Excel API, Aspose.Cells Cloud, REST API, pulizia Excel, automazione fogli di calcolo"
description: "Scopri come rimuovere colonne vuote dai file Excel utilizzando l'API REST Aspose.Cells Cloud. Include endpoint, esempi di autenticazione, richieste/risposte e codice SDK in C#, Java, Python e altri linguaggi."
weight: 100
---

Utilizza l'API Aspose.Cells Cloud per eliminare automaticamente tutte le colonne vuote dai fogli di calcolo Excel. La nostra API intelligente rileva e rimuove le colonne le cui celle non contengono dati, formule, commenti, grafici o oggetti. L'API supporta l'elaborazione in batch, l'automazione nel cloud e un'integrazione REST fluida per flussi di lavoro di pulizia dei fogli di calcolo di livello enterprise.

**Contesto:**  
Le colonne vuote spesso compaiono dopo l'importazione di dati, la generazione di modelli o la migrazione di file legacy. Rimuovere queste colonne vuote migliora le dimensioni del file, le prestazioni di rendering e l'accuratezza dei processi successivi di elaborazione dei dati. L'API Elimina colonne vuote nei fogli di calcolo fornisce un metodo rapido ed efficiente lato server per pulire i fogli di calcolo senza intervento manuale.

## **API DeleteSpreadsheetBlankColumns**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta

| Nome parametro     | Tipo   | Posizione                 | Descrizione                                                                                                                  |
| ------------------ | ------ | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | Form‑Data (multipart)     | Il file Excel da elaborare.                                                                                                  |
| **outPath**        | String | Query                     | Opzionale. Cartella di destinazione nello storage cloud per il file pulito. Se omesso, il risultato viene restituito nel corpo della risposta. |
| **outStorageName** | String | Query                     | Opzionale. Nome dello storage cloud in cui salvare l'output.                                                                |
| **region**         | String | Query                     | Opzionale. Identificatore delle impostazioni locali (ad esempio, `en-US`, `de-DE`).                                          |
| **password**       | String | Query                     | Opzionale. Password per aprire un file protetto.                                                                             |

### Risposta

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

### Codici di errore

- **400 Bad Request** – Parametri di richiesta non validi o URI malformati.
- **401 Unauthorized** – Token di accesso mancante o non valido.
- **404 Not Found** – Il file specificato non è stato trovato.
- **500 Server Error** – Una condizione imprevista ha impedito all'API di elaborare il file.

## Quando utilizzare l'API Elimina colonne vuote nei fogli di calcolo

- **Flussi di lavoro di importazione e pulizia dei dati** – Rimuovi immediatamente colonne vuote finali o strutturali dopo aver caricato dati da CSV, database o API web.
- **Generazione di report e dashboard** – Assicura che i report finali abbiano un layout pulito, senza colonne vuote superflue.
- **Pipeline ETL** – Preprocessa i file Excel prima di caricarli in data warehouse come Snowflake o BigQuery.
- **Integrazione di sistemi** – Normalizza i file Excel forniti dai partner prima di ulteriori elaborazioni.
- **Automazione in batch di documenti** – Rimuovi colonne segnaposto dai modelli generati in massa.
- **Contenuti generati dagli utenti** – Pulisci i file Excel caricati da portali web prima dell'archiviazione o dell'analisi.
- **Migrazione di dati legacy** – Semplifica gli archivi di fogli di calcolo vecchi rimuovendo colonne vuote storiche.

## Perché utilizzare questa API?

- **Semplice per gli sviluppatori** – Gli SDK sono disponibili per C#, Java, Python, PHP, Ruby, Node.js, Go e altri linguaggi, riducendo lo sforzo di sviluppo.
- **Conveniente** – Pricing a consumo elimina i costi iniziali per l’infrastruttura.
- **Zero manutenzione** – Nessun server da gestire; il servizio viene aggiornato continuamente da Aspose.

## Come utilizzare l'API Elimina colonne vuote nei fogli di calcolo con gli SDK

### Specifica dell'API

La [Specifica dell'API Elimina colonne vuote nei fogli di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankColumns) fornisce la definizione OpenAPI completa e gli esempi.

### Utilizzo degli SDK Aspose.Cells Cloud

Gli SDK astraggono i dettagli HTTP di basso livello, consentendo di eliminare le colonne vuote con poche righe di codice. Consulta il repository GitHub ufficiale per l'elenco completo dei linguaggi supportati: <https://github.com/aspose-cells-cloud>.

I seguenti esempi di codice mostrano come chiamare l'API con vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
---