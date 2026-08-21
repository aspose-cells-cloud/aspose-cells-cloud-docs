---
title: "Aspose.Cells Cloud – API per l'eliminazione di file"
second_title: "Documentazione"
ArticleTitle: "Aspose.Cells Cloud – API per l'eliminazione di file"
linktitle: "Eliminazione file"
type: docs
url: /it/delete-file/
keywords: "Aspose Cells, API per l'eliminazione di file, Archiviazione cloud Excel, API REST, Gestione file"
description: "Elimina un file Excel dall'archiviazione cloud Aspose.Cells Cloud utilizzando l'API REST per l'eliminazione dei file. Include endpoint, parametri, autenticazione e codice di esempio."
weight: 100
---

L'API **deleteFile** rimuove il file specificato dall'archiviazione cloud, consentendoti di gestire in modo efficiente risorse e dati.

## **API Excel: Eliminazione file**

### API Web

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                                                                      |
| :------------- | :----- | :------- | :----------------------------------------------------------------------------------------------- |
| `path`         | string | Path     | Percorso URL‑codificato del file che deve essere eliminato.                                     |
| `storageName`  | string | Query    | Nome dell’archiviazione in cui risiede il file. Ignorare se viene utilizzata l’archiviazione predefinita. |
| `versionId`    | string | Query    | Identificatore di una versione specifica del file da eliminare. Se omesso, viene rimossa l’ultima versione. |

### Descrizione della risposta

Una richiesta riuscita restituisce **HTTP 200** con un corpo della risposta vuoto. Non viene restituito alcun payload JSON.

```json
{}
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400  | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413  | Payload troppo grande | Il file caricato supera il limite di dimensione.                  |
| 500  | Errore interno del server | Errore imprevisto del server.                                     |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando diversi SDK.

---