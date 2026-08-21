---
title: "Convertire Grafico in PDF"
ArticleTitle: "Convertire Grafico in PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, conversione grafico"
description: "Converte un grafico di un foglio di calcolo su un drive locale in PDF."
weight: 100
---

## Convertire Grafico in PDF tramite i Servizi Web Aspose.Cells Cloud

Questo metodo legge un grafico da un file di foglio di calcolo fornito tramite caricamento locale, lo converte nel formato PDF e restituisce il risultato convertito. L'elaborazione avviene interamente sul server cloud, pertanto non è richiesta alcuna memorizzazione intermediata. Il percorso del file sorgente e il formato di destinazione devono essere corretti e sono necessari gli opportuni permessi per leggere il file sorgente. Errori come file mancanti, problemi di accesso o fallimenti nella conversione daranno luogo a risposte HTTP di errore appropriate.

### Endpoint API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro   | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione |
|------------------|--------|----------------------------------|-------------|
| Spreadsheet      | File   | FormData                         | Caricamento del file di foglio di calcolo. |
| worksheet        | String | Query                            | Nome del foglio di calcolo. |
| chartIndex       | Integer| Query                            | Indice del grafico all'interno del foglio. |
| outPath          | String | Query                            | (Opzionale) Percorso della cartella in cui è memorizzato il workbook. Il valore predefinito è null. |
| outStorageName   | String | Query                            | Nome dell'archivio per il file di output. |
| fontsLocation    | String | Query                            | Utilizzo di caratteri personalizzati. |
| region           | String | Query                            | Impostazioni regionali/linguistiche del foglio di calcolo (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password         | String | Query                            | La password per aprire il file di foglio di calcolo. |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Caricamento del file di foglio di calcolo. |

### **Risposta**

```json
{
  "ResponseFile": "stream binario del file PDF"
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Grafico convertito correttamente in PDF; file PDF binario restituito. |
| 400 | Richiesta Non Validata | Parametri della richiesta non validi o URL malformato. |
| 401 | Non Autorizzato | Autenticazione fallita o assenza di credenziali. |
| 404 | Non Trovato | File sorgente non accessibile. |
| 413 | Payload Troppo Grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore Interno del Server | Si è verificato un errore durante l'elaborazione della conversione. |

## Come Utilizzare la Funzionalità di Convertire Grafico in PDF con gli SDK

### Specifica della Conversione del Grafico in PDF

La [Specifiche dell'API Converti Grafico in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}
{< tab tabNum="1" >}
```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "stream binario del file PDF"
}
```
{< /tab >}
{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

Utilizzare un SDK rappresenta il metodo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---