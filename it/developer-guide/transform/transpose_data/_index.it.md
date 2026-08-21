---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "TransposeData"
type: docs
url: /it/cells/transpose
aliases: [  /it/cells/transpose ]
keywords: "TransposeData, Aspose.Cells, API cloud, foglio di calcolo, trasporre"
description: "Scambia righe e colonne nel foglio di calcolo."
weight: 1000
---

## La TransposeData dei servizi web Aspose.Cells Cloud

Scambia righe e colonne nel foglio di calcolo.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo   | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                                            |
|------------------|--------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                        | Carica il file del foglio di calcolo.                                                                                                  |
| worksheet        | String | Query                           | Nome del foglio di calcolo.                                                                                                            |
| cellArea         | String | Query                           | Intervallo di dati specificato.                                                                                                        |
| outPath          | String | Query                           | (Opzionale) Percorso della cartella in cui è salvato il workbook. Il valore predefinito è null.                                        |
| outStorageName   | String | Query                           | Nome dell'archivio per il file in uscita.                                                                                             |
| region           | String | Query                           | Impostazione di regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password         | String | Query                           | Password per aprire il file del foglio di calcolo.                                                                                    |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA DEFINIRE]  | [DA DEFINIRE] | [DA DEFINIRE] |

### **Risposta**

```json
{
  "file": "flusso binario del foglio di calcolo trasposto"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Il file del foglio di calcolo trasposto viene restituito. |
| 400 | Richiesta non valida | Parametri di input non validi o richiesta malformata. |
| 401 | Non autorizzato | Autenticazione non riuscita o token JWT mancante/non valido. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Errore imprevisto del server. |

## Come utilizzare la TransposeData con gli SDK

### Specifica della TransposeData

La [Specifiche dell'API TransposeData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "flusso binario del foglio di calcolo trasposto"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

Utilizzare un SDK è il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto.Consulta l'<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">archivio GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[DA DEFINIRE]`
---