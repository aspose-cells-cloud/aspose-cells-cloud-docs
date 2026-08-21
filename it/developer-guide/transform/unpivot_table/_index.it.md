---
title: "Unpivot Table"
ArticleTitle: "Unpivot Table – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Unpivot Table"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Unpivot, Trasformazione"
description: "Inverti righe e colonne nel foglio elettronico."
weight: 1
---

## L'operazione Unpivot Table di Aspose.Cells Cloud Web Services

Inverti righe e colonne nel foglio elettronico.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo    | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                            |
|------------------|---------|----------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                         | Carica il file del foglio elettronico.                                                                                 |
| worksheet        | String  | Query                            | Nome del foglio di calcolo.                                                                                            |
| index            | Integer | Query                            | Intervallo di dati specificato.                                                                                        |
| skipEmptyValue   | Boolean | Query                            | Salta i valori vuoti (valore predefinito: true).                                                                       |
| outPath          | String  | Query                            | (Opzionale) Percorso della cartella in cui è memorizzato il file di lavoro. Il valore predefinito è null.               |
| outStorageName   | String  | Query                            | Nome dell'archivio per il file di output.                                                                              |
| region           | String  | Query                            | Impostazione di regione/lingua del foglio elettronico (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password         | String  | Query                            | Password per aprire il file del foglio elettronico.                                                                    |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| N/A            | N/A  | Nessun parametro nel corpo della richiesta. |

### **Risposta**

```json
{
  "File": "stream binario del foglio elettronico con operazione Unpivot applicata"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Il file del foglio elettronico con operazione Unpivot applicata viene restituito. |
| 400 | Richiesta non valida | Parametri della richiesta non validi. |
| 401 | Non autorizzato | Autenticazione non riuscita o token JWT mancante/invalido. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Errore imprevisto nel server. |

## Come utilizzare l'operazione Unpivot Table con gli SDK

### Specifica dell'operazione Unpivot Table

La [Specifiche dell'API Unpivot Table](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizza HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "stream binario del foglio elettronico con operazione Unpivot applicata"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[TBD]`
---