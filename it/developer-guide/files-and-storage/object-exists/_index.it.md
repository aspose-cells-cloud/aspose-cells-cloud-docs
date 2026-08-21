---
title: "API Object Exists – Verifica la presenza di file/cartelle in Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "API Object Exists – Verifica la presenza di file o cartelle in Aspose.Cells Cloud"
linktitle: "Object Exists"
type: docs
url: /it/object-exists/
keywords: "Aspose.Cells, archiviazione cloud, oggetto esistente, esistenza file, esistenza cartella, API"
description: "Utilizza l'API Object Exists per verificare rapidamente se un file o una cartella esiste nell'archiviazione cloud di Aspose.Cells. Supporta il nome opzionale dello storage e l'ID di versione, e funziona con oggetti versionati."
weight: 100
---

L'**API Object Exists** consente agli sviluppatori di determinare se un file o una cartella specifico è presente nell'archiviazione cloud di Aspose.Cells. Restituisce un semplice valore booleano che indica l'esistenza e se il percorso punta a una cartella.

## **API Excel: Object Exists**

### API Web

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ rappresenta il percorso completo del file o della cartella nello storage.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Obbligatorio | Descrizione                                                                 |
| -------------- | ------ | --------- | ------------ | --------------------------------------------------------------------------- |
| `path`         | string | Path      | Sì           | Percorso completo del file o della cartella.                               |
| `storageName`  | string | Query     | No           | Nome dello storage; se omesso, assume lo storage primario come predefinito.|
| `versionId`    | string | Query     | No           | Identificatore specifico della versione del file (se il controllo versioni è abilitato). |

**Codici di stato HTTP**

| Codice HTTP | Stato HTTP            | Descrizione                                                         |
| ----------- | --------------------- | ------------------------------------------------------------------- |
| 200         | OK                    | La chiamata API Web è andata a buon fine; la risposta contiene i dettagli dell'operazione. |
| 400         | Bad Request           | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401         | Unauthorized          | Token JWT non valido o mancante.                                    |
| 413         | Payload Too Large     | Il file caricato supera il limite di dimensione.                   |
| 500       | Internal Server Error | Errore imprevisto del server.                                       |

### **Risposta**

Una chiamata riuscita restituisce un payload JSON con due proprietà:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` se il file o la cartella esiste; altrimenti `false`.
- **IsFolder** – `true` quando il percorso punta a una cartella; `false` per un file.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK. Se un Gist non si carica, viene fornito un esempio statico sotto ogni scheda.