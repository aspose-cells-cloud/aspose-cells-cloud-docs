---
title: "Ottieni Fogli di Lavoro con Foglio di Calcolo Locale"
ArticleTitle: "Ottieni Fogli di Lavoro con Foglio di Calcolo Locale – Aspose.Cells Cloud"
second_title: "Documento"
linktype: "docs"
url: /cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, Fogli di Lavoro, Foglio di Calcolo Locale, API"
description: "Recupera un elenco completo dei fogli di lavoro dal foglio di calcolo locale attualmente attivo."
weight: 1000
---

## Ottieni Fogli di Lavoro con Foglio di Calcolo Locale di Aspose.Cells Cloud Web Services

Questa endpoint accede all'applicazione di fogli di calcolo locale (ad esempio Excel) tramite interop o un'API locale, raccoglie il nome e il tipo (ad esempio standard, grafico, con macro) di ogni foglio di lavoro e restituisce l'insieme come array JSON strutturato. Viene tipicamente utilizzata per popolare un'interfaccia utente di selezione dei fogli di lavoro o per eseguire un'analisi dei contenuti del foglio di calcolo.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | File   | FormData (Corpo HTTP)            | Carica il file del foglio di calcolo. |
| region         | String | Query                            | Impostazione di area/lingua del foglio di calcolo (ad esempio `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. *(opzionale)* |
| password       | String | Query                            | La password per aprire il file del foglio di calcolo. *(opzionale)* |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
|----------------|------|-------------|
| Spreadsheet    | File | Carica il file del foglio di calcolo. |

### **Risposta**

```json
{
  "Worksheets": [
    {
      "Name": "Foglio1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Grafico1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... fogli di lavoro aggiuntivi
  ]
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | L'elenco dei fogli di lavoro è stato recuperato correttamente. |
| 400 | Richiesta Non Validata | Richiesta non valida (ad esempio URL malformato o dati obbligatori mancanti). |
| 401 | Non Autorizzato | L'autenticazione non è riuscita o non sono state fornite credenziali. |
| 404 | Non Trovato | Il file sorgente non è accessibile. |
| 413 | Payload Troppo Grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore Interno del Server | Il foglio di calcolo ha riscontrato un'anomalia durante il recupero dei dati. |

## Come Utilizzare l'Endpoint Ottieni Fogli di Lavoro con Foglio di Calcolo Locale con gli SDK

### Specifica dell'Endpoint Ottieni Fogli di Lavoro con Foglio di Calcolo Locale

La [Specifiche dell'API Ottieni Fogli di Lavoro con Foglio di Calcolo Locale](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizza HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Foglio1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Grafico1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... fogli di lavoro aggiuntivi
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

Utilizzare un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells Cloud utilizzando vari SDK:
`[DA COMPLETARE]`