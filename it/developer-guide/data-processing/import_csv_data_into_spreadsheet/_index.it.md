---
title: "Importare dati CSV in un foglio di calcolo"
ArticleTitle: "Importare dati CSV in un foglio di calcolo – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Importare dati CSV in un foglio di calcolo"
type: docs
url: /cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, importazione CSV, foglio di calcolo, API"
description: "Importa un file CSV in un foglio di calcolo locale utilizzando l’API Aspose.Cells Cloud."
weight: 100
---

## Importazione di dati CSV in un foglio di calcolo tramite i servizi web Aspose.Cells Cloud

Importa un file CSV in un foglio di calcolo locale. Il metodo analizza il file CSV, mappa i dati alla struttura delle celle del foglio di calcolo e salva il file localmente. I formati di foglio di calcolo supportati includono .xlsx e .ods.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro        | Tipo    | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                          |
|-----------------------|---------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | File    | FormData                         | File di dati da caricare.                                                                                                            |
| Spreadsheet           | File    | FormData                         | File del foglio di calcolo da caricare.                                                                                              |
| worksheet             | String  | Query                            | Foglio di calcolo in cui importare i dati CSV. (obbligatorio)                                                                        |
| startcell             | String  | Query                            | Posizione iniziale per l'importazione dei dati. (obbligatorio)                                                                       |
| insert                | Boolean | Query                            | Controlla il comportamento di inserimento. true: inserisce i dati; false: sovrascrive i dati esistenti. Default: true (opzionale)   |
| convertNumericData    | Boolean | Query                            | Indica se le stringhe nel file di testo devono essere convertite in dati numerici. Default: true (opzionale)                        |
| splitter              | String  | Query                            | Delimitatore utilizzato per suddividere i campi CSV. Default: "," (opzionale)                                                       |
| outPath               | String  | Query                            | (Opzionale) Percorso della cartella in cui è salvato il workbook. Default: null (opzionale).                                        |
| outStorageName        | String  | Query                            | Nome dello storage per il file di output. (opzionale)                                                                               |
| fontsLocation         | String  | Query                            | Utilizza font personalizzati. (opzionale)                                                                                            |
| region                | String  | Query                            | Impostazione di regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. (opzionale) |
| password              | String  | Query                            | Password per aprire il file del foglio di calcolo. (opzionale)                                                                      |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA COMPLETARE] | [DA COMPLETARE] | [DA COMPLETARE] |

### **Risposta**

```json
{
  "file": "<stream binario del foglio di calcolo risultante>"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | I dati CSV sono stati importati correttamente e il file del foglio di calcolo risultante viene restituito. |
| 400 | Richiesta non valida | I parametri della richiesta non sono validi o l'URL è malformato. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | Il file sorgente non è accessibile. |
| 413 | Payload troppo grande | I file caricati superano il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un anomalia nel recupero dei dati da parte del foglio di calcolo. |

## Come utilizzare l’importazione di dati CSV in un foglio di calcolo con gli SDK

### Specifica dell'importazione di dati CSV in un foglio di calcolo

La [Specifica dell'API Importazione di dati CSV in un foglio di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<stream binario del foglio di calcolo risultante>"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[DA COMPLETARE]`
---