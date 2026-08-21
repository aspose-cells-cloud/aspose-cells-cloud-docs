---
title: "Aspose.Cells Cloud Folder Copy API – Copia rapida di cartelle nel cloud"
second_title: "Documento"
ArticleTitle: "Soluzione di gestione di file Excel basata sul cloud – Spiegazione dettagliata della funzionalità di copia in batch dell'API Aspose.Cells Copy Folder"
linktype: "docs"
url: /it/copy-folder/
keywords: "Copia cartella, Aspose.Cells Cloud, API REST, Archiviazione cloud, Gestione fogli di calcolo"
description: "Scopri come copiare cartelle nell'archiviazione Aspose.Cells Cloud con una singola chiamata REST. Include endpoint, parametri, richieste di esempio, codici di errore ed esempi di SDK."
weight: 100
---

L'API **CopyFolder** duplica una cartella esistente all'interno dell'archiviazione Aspose.Cells Cloud. Questa funzionalità è utile per creare backup, riorganizzare i dati o preparare una gerarchia di cartelle per ulteriori elaborazioni, senza dover spostare manualmente i file.

## **API Excel: Copia cartella**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### L'API CopyFolder accetta i seguenti parametri

| Nome parametro    | Obbligatorio | Tipo   | Posizione (Path/Query) | Descrizione                                                            |
| ----------------- | ------------ | ------ | ---------------------- | ---------------------------------------------------------------------- |
| `srcPath`         | Sì           | String | Path                   | Il percorso della cartella sorgente da copiare.                        |
| `destPath`        | Sì           | String | Query                  | Il percorso in cui verrà creata la nuova cartella.                     |
| `srcStorageName`  | No           | String | Query                  | Il nome dell'archivio che contiene la cartella sorgente.               |
| `destStorageName` | No           | String | Query                  | Il nome dell'archivio di destinazione in cui la cartella deve essere copiata. |

### Risposta di esempio

Una chiamata riuscita restituisce **HTTP 200** con un corpo JSON vuoto:

```json
{}
```

**Richiesta cURL di esempio**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                   |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

L'utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce automaticamente i dettagli di basso livello e consente di concentrarsi sulle attività del progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}