---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Convertire foglio di calcolo in PDF – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "ConvertWorksheetToPdf"
type: docs
url: /it/cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, convertire foglio di calcolo in PDF, API"
description: "Converte un foglio di calcolo di un file in formato PDF utilizzando Aspose.Cells Cloud."
weight: 10
---

## ConvertWorksheetToPdf di Aspose.Cells Cloud Web Services

Questo metodo legge un file di foglio di calcolo dal filesystem locale, lo converte in un file PDF e restituisce il risultato convertito. È necessario specificare correttamente il percorso del file sorgente e il formato di destinazione. Assicurarsi che siano presenti le autorizzazioni necessarie per leggere il file sorgente e scrivere il file convertito, se applicabile. Il processo di conversione avviene interamente sul server cloud, eliminando la necessità di qualsiasi archiviazione cloud o download esterno.

Le funzionalità chiave includono conversione nativa cloud, riduzione del carico delle risorse cloud e un flusso di lavoro semplificato.

### Endpoint Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo    | Percorso/Query String/Corpo HTTP | Descrizione                                                                                                                            |
|------------------|---------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                         | Carica il file di foglio di calcolo.                                                                                                   |
| worksheet        | String  | Query                            | Nome del foglio di calcolo.                                                                                                            |
| outPath          | String  | Query                            | (Facoltativo) Percorso della cartella in cui è memorizzato il libro di lavoro. Il valore predefinito è null.                          |
| outStorageName   | String  | Query                            | Nome dell'archiviazione per il file di output.                                                                                        |
| fontsLocation    | String  | Query                            | Utilizza font personalizzati.                                                                                                          |
| AutoRowsFit      | Boolean | Query                            | (Facoltativo) Adatta automaticamente tutte le righe nei fogli di calcolo.                                                             |
| AutoColumnsFit   | Boolean | Query                            | (Facoltativo) Adatta automaticamente tutte le colonne nei fogli di calcolo.                                                          |
| region           | String  | Query                            | Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password         | String  | Query                            | La password per aprire il file di foglio di calcolo.                                                                                  |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA DEFINIRE]  |      |             |

### **Risposta**

```json
{
  "file": "<flusso binario del PDF generato>"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Il foglio di calcolo è stato convertito con successo in PDF e restituito come flusso di file. |
| 400 | Richiesta non valida | Parametri della richiesta non validi o URL malformato. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File sorgente non accessibile. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificata un'anomalia durante la conversione del foglio di calcolo. |

## Come utilizzare ConvertWorksheetToPdf con gli SDK

### Specifica ConvertWorksheetToPdf

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf" rel="noopener noreferrer">Specifiche dell'API ConvertWorksheetToPdf</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token jwt>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flusso binario del PDF generato>"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[DA DEFINIRE]`
---