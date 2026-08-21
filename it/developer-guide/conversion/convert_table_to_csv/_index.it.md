---
---
title: "Convertire Tabella in CSV"
ArticleTitle: "Convertire Tabella in CSV – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Convertire Tabella in CSV"
type: docs
url: /cells/convert/table/csv
aliases: []
keywords: "Convertire Tabella CSV, Aspose.Cells, API Cloud"
description: "Converte una tabella di un foglio di calcolo presente su un disco locale in un file CSV."
weight: 1
---

## La conversione della tabella in CSV dei servizi web Aspose.Cells Cloud

Questo metodo legge un file di foglio di calcolo dal file system locale, converte la tabella specificata in un file CSV e restituisce il risultato convertito. Opera interamente sul server cloud, quindi non è richiesto alcun caricamento intermediato nello storage cloud. Il percorso del file sorgente e il formato di destinazione devono essere specificati correttamente, ed è necessario disporre delle autorizzazioni appropriate per leggere il file sorgente. Errori come file mancanti, percorsi inaccessibili o fallimenti nella conversione genereranno le eccezioni appropriate.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome Parametro   | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione |
|------------------|--------|----------------------------------|-------------|
| Spreadsheet      | File   | FormData                         | Carica il file di foglio di calcolo. |
| worksheet        | String | Query                            | Nome del foglio di calcolo. |
| tableName        | String | Query                            | Nome della tabella |
| outPath          | String | Query                            | (Opzionale) Percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è null. |
| outStorageName   | String | Query                            | Nome dello Storage per il file di output. |
| fontsLocation    | String | Query                            | Utilizza i caratteri personalizzati. |
| AutoRowsFit      | Boolean| Query                            | (Opzionale) Adatta automaticamente tutte le righe nei fogli di calcolo. |
| AutoColumnsFit   | Boolean| Query                            | (Opzionale) Adatta automaticamente tutte le colonne nei fogli di calcolo. |
| region           | String | Query                            | Impostazione regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password         | String | Query                            | La password per aprire il file di foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| *Nessuno* | *Nessuno* | *Non è richiesto alcun corpo della richiesta; il file viene inviato come multipart/form-data.* |

### **Risposta**

```json
{
  "file": "flusso binario del file CSV generato"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | La tabella è stata convertita correttamente e il file CSV è restituito. |
| 400 | Richiesta non valida | Parametri della richiesta non validi o URL mal formati. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File sorgente non accessibile o inesistente. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante la conversione. |

## Come utilizzare la conversione della tabella in CSV con gli SDK

### Specifica della conversione della tabella in CSV

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv" rel="noopener noreferrer">Specifica dell'API Convert Table to CSV</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "flusso binario del file CSV generato"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells Cloud utilizzando vari SDK:
`[TBD]`
---