---
---
title: "Aspose.Cells Cloud Move File API – Interfaccia per lo spostamento rapido di file nel cloud"
second_title: "Documento"
ArticleTitle: "Soluzione efficiente per la gestione di file Excel nel cloud – Interfaccia per lo spostamento rapido di file nel cloud"
linktitle: "Sposta file"
type: docs
url: /it/move-file/
keywords: "Aspose.Cells, Move File API, Archiviazione cloud, API Excel, Gestione file"
description: "Come spostare i file tra cartelle nell'archiviazione cloud di Aspose.Cells utilizzando l'API Move File v4.0 – endpoint, parametri, esempi e link agli SDK."
weight: 100
---

L'API **moveFile** sposta un file da una posizione all'altra all'interno dell'archiviazione cloud di Aspose.Cells. Ti aiuta a organizzare i file e gestire l'archiviazione in modo efficiente.

## **API Excel: Sposta file**

### API Web

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri della richiesta dell'API **moveFile** sono

| Nome parametro  | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                              |
| --------------- | ------ | ------------------------------------ | -------------------------------------------------------- |
| srcPath         | Stringa | Percorso                             | Il percorso di origine del file da spostare.             |
| destPath        | Stringa | Stringa di query                     | Il percorso di destinazione in cui verrà spostato il file. |
| srcStorageName  | Stringa | Stringa di query                     | Il nome dell'archivio di origine, se applicabile.        |
| destStorageName | Stringa | Stringa di query                     | Il nome dell'archivio di destinazione, se applicabile.   |
| versionId       | Stringa | Stringa di query                     | L'ID della versione del file, se applicabile.            |

### **Risposta**

Una richiesta riuscita restituisce **HTTP 200 OK** con un corpo JSON vuoto.

```json
{}
```

**Codici di stato HTTP**

| Codice HTTP | Stato HTTP            | Descrizione                                                           |
| ----------- | --------------------- | --------------------------------------------------------------------- |
| 200         | OK                    | API web chiamata correttamente; la risposta contiene i dettagli dell'operazione. |
| 400         | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401         | Non autorizzato       | Token JWT non valido o mancante.                                      |
| 413         | Payload troppo grande | Il file caricato supera il limite di dimensione.                      |
| 500         | Errore interno del server | Errore imprevisto del server.                                        |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Utilizzare un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK: