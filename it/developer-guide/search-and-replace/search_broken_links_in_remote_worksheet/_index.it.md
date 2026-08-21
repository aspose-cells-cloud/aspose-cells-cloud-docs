---
title: "SearchBrokenLinksInRemoteWorksheet"
ArticleTitle: "Cerca link rotti nel foglio di calcolo remoto – Aspose.Cells Cloud API"
second_title: "Documenti"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, Cerca link rotti, Foglio di calcolo remoto"
description: "Cerca link rotti nel foglio di calcolo di un file spreadsheet memorizzato nel cloud remoto."
weight: 100
---

## La funzione Cerca link rotti nel foglio di calcolo remoto dei servizi web Aspose.Cells Cloud

Questo metodo consente di cercare link rotti all’interno di un foglio di calcolo di un file spreadsheet archiviato in un archivio cloud remoto. Esamina tutti i fogli e le celle per identificare gli iperlink che non puntano più a destinazioni valide, come URL non più raggiungibili o riferimenti esterni mancanti. L’operazione viene eseguita in remoto nell’ambiente cloud, senza richiedere il download del file sul computer locale.

### Endpoint Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|------|----------------------------------|-------------|
| name | string | Percorso | Nome del file del foglio di calcolo da analizzare. |
| worksheet | string | Percorso | Specifica il foglio di calcolo in cui effettuare la ricerca. |
| folder | string | Query | Percorso della cartella in cui è memorizzato il foglio di calcolo. (facoltativo) |
| storageName | string | Query | (Facoltativo) Nome dell’archivio se si utilizza un archivio cloud personalizzato. Se omesso, viene utilizzato l’archivio predefinito. |
| region | string | Query | Impostazioni di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l’analisi delle date e il comportamento specifico della lingua. |
| password | string | Query | Password necessaria per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| — | — | Nessun corpo della richiesta è richiesto per questa operazione. |

### **Risposta**

```json
{
  "Links": [
    {
      "SheetName": "Foglio1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Elenco dei link rotti recuperato correttamente. |
| 400 | Richiesta non valida | Parametri della richiesta non validi o URL malformato. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File sorgente non accessibile. |
| 413 | Payload troppo grande | Entità della richiesta troppo grande. |
| 500 | Errore interno del server | Il foglio di calcolo ha riscontrato un’anomalia durante il recupero dei dati. |

## Come utilizzare la funzione Cerca link rotti nel foglio di calcolo remoto con gli SDK

### Specifica della funzione Cerca link rotti nel foglio di calcolo remoto

La [specificazione dell’API Cerca link rotti nel foglio di calcolo remoto](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) definisce un’interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Usa HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Foglio1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L’utilizzo di un SDK è il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose Cells Cloud utilizzando vari SDK:
`[DA COMPLETARE]`
---