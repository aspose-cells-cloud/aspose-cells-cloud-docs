---
---
title: "Importare dati XML in un foglio di calcolo"
ArticleTitle: "Importare dati XML in un foglio di calcolo – Aspose.Cells Cloud API"
second_title: "Documenti"
linktype: "Importare dati XML in un foglio di calcolo"
type: docs
url: /cells/import/data/xml
aliases: []
keywords: "Importare XML, Aspose.Cells, API"
description: "Importa un file di dati XML in un foglio di calcolo locale utilizzando Aspose.Cells Cloud."
weight: 1000
---

## Importare dati XML in un foglio di calcolo dei servizi web Aspose.Cells Cloud

Importa un file di dati XML in un foglio di calcolo locale. Il metodo analizza il file XML, mappa i dati alla struttura delle celle del foglio di calcolo e salva il file in locale. I formati di foglio di calcolo supportati includono .xlsx e .ods.

### Endpoint API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro | Tipo    | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                            |
|---------------------|---------|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile            | File    | FormData                             | Carica il file di dati.                                                                                                                |
| Spreadsheet         | File    | FormData                             | Carica il file del foglio di calcolo.                                                                                                  |
| worksheet           | String  | Query                                | Foglio di calcolo in cui importare i dati XML.                                                                                        |
| startcell           | String  | Query                                | Posizione iniziale per l'importazione dei dati                                                                                       |
| insert              | Boolean | Query                                | Controlla il comportamento di inserimento. true: inserisce i dati; false: sovrascrive i dati esistenti. Default: **true**            |
| outPath             | String  | Query                                | (Opzionale) Il percorso della cartella in cui è memorizzato il foglio di calcolo. Default: null.                                     |
| outStorageName      | String  | Query                                | Nome dell'archivio per il file di output.                                                                                             |
| fontsLocation       | String  | Query                                | Utilizza font personalizzati.                                                                                                          |
| region              | String  | Query                                | Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password            | String  | Query                                | La password per aprire il file del foglio di calcolo.                                                                                 |

### Parametro del corpo della richiesta

| Nome del parametro | Tipo | Descrizione |
|--------------------|------|-------------|
| *None*             | -    | -           |

### **Risposta**

```json
{
  "file": "<stream binario del foglio di calcolo aggiornato>"
}
```

**Codici di stato della risposta**

| Codice | Significato             | Descrizione                                                                                           |
|--------|-------------------------|-------------------------------------------------------------------------------------------------------|
| 200    | OK                      | I dati XML sono stati importati correttamente e il file del foglio di calcolo aggiornato viene restituito. |
| 400    | Richiesta non valida    | URL della richiesta non valido o parametri obbligatori mancanti.                                   |
| 401    | Non autorizzato         | Autenticazione non riuscita o credenziali non fornite.                                              |
| 404    | Non trovato             | File sorgente non accessibile.                                                                       |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione consentito.                                         |
| 500    | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante il recupero dei dati.                        |

## Come utilizzare l'importazione di dati XML in un foglio di calcolo con gli SDK

### Specifica per l'importazione di dati XML in un foglio di calcolo

La [Specifica dell'API Importare dati XML in un foglio di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Usa HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<stream binario del foglio di calcolo aggiornato>"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---