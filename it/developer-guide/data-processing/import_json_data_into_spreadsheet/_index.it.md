---
title: "Importa dati JSON in un foglio di calcolo"
ArticleTitle: "Importa dati JSON in un foglio di calcolo – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Importa dati JSON in un foglio di calcolo"
type: docs
url: /it/cells/import/data/json
aliases: []
keywords: "Importa JSON, Aspose.Cells, Foglio di calcolo, API"
description: "Importa un file di dati JSON in un foglio di calcolo locale."
weight: 1
---

## Importa dati JSON in un foglio di calcolo tramite i servizi web di Aspose.Cells Cloud

Importa un file di dati JSON in un foglio di calcolo locale. Il metodo analizza il JSON, mappa i dati alla struttura delle celle del foglio di calcolo e salva il file localmente. I formati di foglio di calcolo supportati includono .xlsx e .ods.

### Endpoint API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| datafile       | File   | FormData                         | Carica il file di dati. |
| Spreadsheet    | File   | FormData                         | Carica il file del foglio di calcolo. |
| worksheet      | string | Query                            | Foglio di calcolo in cui importare i dati JSON. |
| startcell      | string | Query                            | Posizione iniziale per l'importazione dei dati |
| insert         | boolean| Query                            | Controlla il comportamento di inserimento. true: inserisce i dati; false: sovrascrive i dati esistenti. (Predefinito: true) |
| outPath        | string | Query                            | (Facoltativo) Percorso della cartella in cui è memorizzato il workbook. Il valore predefinito è null. |
| outStorageName | string | Query                            | Nome dell'archivio per il file di output. |
| fontsLocation  | string | Query                            | Usa caratteri personalizzati. |
| region         | string | Query                            | Impostazione di area/geolocalizzazione del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password       | string | Query                            | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA DEFINIRE] | [DA DEFINIRE] | [DA DEFINIRE] |

### **Risposta**

```json
{
  "file": "stream binario"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | File generato e restituito correttamente. |
| 400 | Richiesta non valida | URL non valido. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File sorgente non accessibile. |
| 413 | Payload troppo grande | [DA DEFINIRE] |
| 500 | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante il recupero dei dati. |

## Come usare l'importazione di dati JSON in un foglio di calcolo con gli SDK

### Specifica per l'importazione di dati JSON in un foglio di calcolo

La [Specifiche dell'API Importa dati JSON in un foglio di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}
{< tab tabNum="1" >}
```bash
# Usa HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "stream binario"
}
```
{< /tab >}
{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[DA DEFINIRE]`
---