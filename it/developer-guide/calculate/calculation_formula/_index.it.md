---
title: "Calcola Formula"
ArticleTitle: "Calcola Formula – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Calcola Formula"
type: docs
url: /it/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, calcola formula, foglio di calcolo, API"
description: "Calcola una formula in un foglio di calcolo utilizzando l'API Aspose.Cells Cloud."
weight: 100
---

## La funzione Calcola Formula dei Web Service Aspose.Cells Cloud

Calcola una formula specificata in un foglio di calcolo fornito e restituisce il foglio di calcolo risultante come flusso di file. Questa operazione supporta l'elaborazione in base alle impostazioni locali tramite il parametro **region** e può aprire file protetti da password.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome Parametro | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione |
|----------------|--------|--------------------------------------|-------------|
| Spreadsheet    | File   | FormData                             | Carica il file del foglio di calcolo. |
| worksheet      | String | Query                                | Nome del foglio di calcolo contenente la formula. |
| formula        | String | Query                                | La formula da calcolare (es. `=SUM(A1:B2)`). |
| region         | String | Query                                | Impostazione di area/geolocalizzazione del foglio di calcolo (es. `it-IT`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico per le impostazioni locali. |
| password       | String | Query                                | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA DEFINIRE] | [DA DEFINIRE] | [DA DEFINIRE] |

### **Risposta**

```json
{
  "File": "<flusso binario del foglio di calcolo risultante>"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Calcolo completato con successo; il file del foglio di calcolo risultante viene restituito. |
| 400 | Richiesta non valida | Uno o più parametri della richiesta sono mancanti o non validi. |
| 401 | Non autorizzato | Autenticazione fallita o token JWT mancante/non valido. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare la funzione Calcola Formula con gli SDK

### Specifica della funzione Calcola Formula

La [Specifica dell'API Calcola Formula](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=it-IT&password=MyPassword" \
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
  "File": "<flusso binario del foglio di calcolo risultante>"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[DA DEFINIRE]`
---