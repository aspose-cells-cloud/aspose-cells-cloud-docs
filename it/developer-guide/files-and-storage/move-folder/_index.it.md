---
---
title: "Aspose.Cells Cloud API per spostare le cartelle – Sposta rapidamente le cartelle nel cloud"
second_title: "Documento"
ArticleTitle: "Gestione di file Excel basata sul cloud – Sposta rapidamente le cartelle nel cloud"
linktitle: "Sposta cartella"
type: docs
url: /it/move-folder/
keywords: "Aspose.Cells, Sposta cartella, Archiviazione cloud, API Excel"
description: "Scopri come spostare cartelle nell'archiviazione cloud di Aspose.Cells tramite l'API RESTful per lo spostamento delle cartelle. Include endpoint, parametri, esempi cURL, codici di errore ed esempi di SDK per C#, Java, Python e altro ancora."
weight: 100
---

Questa API sposta una cartella da una posizione all'altra all'interno dell'archiviazione cloud di Aspose.Cells. Aiuta a organizzare i file e gestire in modo efficiente l'archiviazione cloud.

## **API Excel: Sposta cartella**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Esempio di richiesta cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### I parametri della richiesta dell'API **moveFolder** sono

| Nome parametro  | Tipo   | Posizione | Descrizione                                                       |
| --------------- | ------ | --------- | ----------------------------------------------------------------- |
| srcPath         | string | Path      | Percorso completo della cartella da spostare, ad esempio `FolderA/`. |
| destPath        | string | Query     | Percorso di destinazione in cui verrà spostata la cartella, ad esempio `FolderB/`. |
| srcStorageName  | string | Query     | (Opzionale) Nome dell'archivio di origine.                        |
| destStorageName | string | Query     | (Opzionale) Nome dell'archivio di destinazione.                   |

**Dettagli dei parametri**

- **srcPath** – obbligatorio. Il percorso della cartella di origine.
- **destPath** – obbligatorio. Il percorso della cartella di destinazione.
- **srcStorageName** – opzionale. Identificatore dell'archivio di origine.
- **destStorageName** – opzionale. Identificatore dell'archivio di destinazione.

### **Risposta**

In caso di esito positivo, l'API restituisce un corpo di risposta vuoto con codice di stato HTTP **200 OK**. Gli errori vengono restituiti come oggetti JSON contenenti un campo `error`.

**Codici di stato HTTP**

| Codice HTTP | Stato HTTP            | Descrizione                                                        |
| ----------- | --------------------- | ------------------------------------------------------------------ |
| 200         | OK                    | L'API Web è stata chiamata correttamente; la risposta contiene i dettagli dell'operazione. |
| 400         | Bad Request           | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401         | Unauthorized          | Token JWT non valido o mancante.                                   |
| 413         | Payload Too Large     | Il file caricato supera il limite di dimensione.                  |
| 500         | Internal Server Error | Errore imprevisto del server.                                      |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

L'utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sui compiti del proprio progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK: