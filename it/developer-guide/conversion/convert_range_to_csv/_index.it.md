---
title: "Converti Intervallo in CSV"
ArticleTitle: "Converti Intervallo in CSV – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Converti Intervallo in CSV"
type: docs
url: /it/cells/convert/range/csv
aliases: []
keywords: "convertire, csv, intervallo, Aspose.Cells"
description: "Converte un intervallo di un foglio di calcolo presente su un disco locale in un file CSV."
weight: 1
---

## Converti Intervallo in CSV di Aspose.Cells Cloud Web Services

Questa operazione legge un file di foglio di calcolo dal filesystem locale, converte un intervallo specificato in formato CSV e restituisce direttamente il risultato convertito. Funziona interamente sul server cloud, pertanto non è necessario alcun caricamento intermedio nello storage cloud. L'API supporta parametri opzionali come caratteri personalizzati, ridimensionamento automatico righe/columnne, impostazioni locali e cartelle di lavoro protette da password.

### Endpoint API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro   | Tipo    | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                                            |
|------------------|---------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                         | Carica il file di foglio di calcolo.                                                                                                   |
| worksheet        | String  | Query                            | Nome del foglio di calcolo. **Obbligatorio**.                                                                                         |
| range            | String  | Query                            | Area di celle, ad esempio `A1:C10`. **Obbligatorio**.                                                                                 |
| outPath          | String  | Query                            | (Opzionale) Percorso della cartella in cui è salvata la cartella di lavoro. Il valore predefinito è null.                              |
| outStorageName   | String  | Query                            | Nome dello Storage per il file di output.                                                                                             |
| fontsLocation    | String  | Query                            | Utilizza caratteri personalizzati.                                                                                                     |
| AutoRowsFit      | Boolean | Query                            | (Opzionale) Ridimensiona automaticamente tutte le righe nei fogli di calcolo.                                                         |
| AutoColumnsFit   | Boolean | Query                            | (Opzionale) Ridimensiona automaticamente tutte le colonne nei fogli di calcolo.                                                       |
| region           | String  | Query                            | Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione numerica, l'analisi delle date e il comportamento specifico della localizzazione. |
| password         | String  | Query                            | La password per aprire il file di foglio di calcolo.                                                                                  |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Nessuno        | N/A  | Nessun parametro nel corpo della richiesta. |

### **Risposta**

```json
{
  "ResponseFile": "flusso binario del file (contenuto CSV)"
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | L'intervallo è stato convertito con successo e il file CSV è restituito nel corpo della risposta. |
| 400 | Richiesta Non Validata | URL non valido o parametri obbligatori mancanti. |
| 401 | Non Autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 413 | Payload Troppo Grande | La dimensione del payload della richiesta supera il limite consentito. |
| 500 | Errore Interno del Server | Si è verificato un anomalia durante l'ottenimento dei dati di conversione del foglio di calcolo. |

## Come Utilizzare la Funzionalità Converti Intervallo in CSV con gli SDK

### Specifica Converti Intervallo in CSV

La [Specifiche API Converti Intervallo in CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizza HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "ContenutoCsvCodificatoInBase64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose Cells Cloud utilizzando diversi SDK:
`[DA COMPLETARE]`
---