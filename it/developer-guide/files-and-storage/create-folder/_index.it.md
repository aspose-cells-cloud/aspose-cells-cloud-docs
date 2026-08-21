---
title: "Crea cartella – Aspose.Cells Cloud API | Gestione archiviazione Excel"
second_title: "Documento"
ArticleTitle: "Crea cartella – Aspose.Cells Cloud API"
linktype: "docs"
url: /it/create-folder/
keywords: "Aspose.Cells, API cloud, Crea cartella, Gestione archiviazione, Excel"
description: "Crea una nuova cartella nell’archivio cloud di Aspose.Cells Cloud tramite una semplice richiesta PUT. Visualizza il formato della richiesta, i parametri, la risposta e la gestione degli errori."
weight: 100
---

L'operazione **createFolder** crea una nuova cartella nella posizione specificata nell’archivio cloud utilizzato dall’API Excel. Questo è essenziale per organizzare i file e mantenere una gerarchia strutturata delle directory.

## **API Excel: Crea cartella**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### I parametri della richiesta dell'API **createFolder** sono

| Nome parametro | Tipo   | Posizione | Obbligatorio | Default | Descrizione                                                                 |
| -------------- | ------ | --------- | ------------ | ------- | --------------------------------------------------------------------------- |
| `path`         | String | Percorso  | Sì           | –       | Il percorso della cartella da creare (ad esempio, `miaCartella/sottoCartella`). |
| `storageName`  | String | Query     | No           | –       | Il nome dell’archivio da utilizzare. Se omesso, viene applicato l’archivio predefinito. |

### Descrizione della risposta

```json
{}
```

L'operazione non restituisce alcun contenuto in caso di esito positivo. I codici di stato HTTP tipici sono i seguenti:

**Codici di stato HTTP**

| Codice HTTP | Stato HTTP            | Descrizione                                                                 |
| ----------- | --------------------- | --------------------------------------------------------------------------- |
| 200         | OK                    | L'API Web è stata richiamata correttamente; la risposta contiene i dettagli dell'operazione. |
| 400         | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401         | Non autorizzato       | Token JWT non valido o mancante.                                            |
| 413         | Payload troppo grande | Il file caricato supera il limite di dimensione.                           |
| 500         | Errore interno del server | Errore imprevisto nel server.                                               |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/miaCartella/sottoCartella" \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}