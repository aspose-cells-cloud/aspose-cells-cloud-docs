---
title: "Aspose.Cells Cloud File Copy API - Un'interfaccia per la copia rapida e le operazioni in batch di file Excel nel cloud"
second_title: "Documento"
ArticleTitle: "Soluzione di gestione dei file Excel basata sul cloud – Spiegazione dettagliata della funzionalità di copia in batch dell'API Aspose.Cells Copy File"
linktitle: "Copia file"
type: docs
url: /it/copy-file/
keywords: "Aspose.Cells, CopyFile API, copia file Excel, archiviazione cloud, API REST"
description: "Scopri come utilizzare l'API Aspose.Cells Cloud CopyFile per duplicare in modo efficiente i file Excel e gestirli tra diverse posizioni di archiviazione."
weight: 100
---

L'API **copyFile** consente agli utenti di duplicare un file Excel da un percorso sorgente specificato a un percorso di destinazione, supportando varie opzioni di archiviazione.

## **API Excel: Copia file**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### I parametri della richiesta dell'API **copyFile** sono i seguenti

| Nome del parametro | Tipo   | Percorso/Query String/HTTPBody | Descrizione                                              |
|--------------------|--------|--------------------------------|----------------------------------------------------------|
| srcPath            | String | Percorso                       | Il percorso sorgente del file da copiare.                |
| destPath           | String | Query                          | Il percorso di destinazione in cui verrà salvato il file.|
| srcStorageName     | String | Query                          | Il nome dell'archiviazione sorgente.                     |
| destStorageName    | String | Query                          | Il nome dell'archiviazione di destinazione.              |
| versionId          | String | Query                          | ID della versione facoltativo del file da copiare.       |

### **Risposta**

L'operazione non restituisce alcun contenuto in caso di esito positivo. I codici di stato HTTP tipici sono i seguenti:

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                         |
|--------|-------------------------|---------------------------------------------------------------------|
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                    |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                   |
| 500    | Errore interno del server| Errore imprevisto nel server.                                       |

## Come utilizzare l'API Copia File con gli SDK?

### Specifica dell'API Copia File

La [Specifica dell'API Copia File](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) fornisce un'interfaccia di programmazione accessibile pubblicamente per effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
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

### Utilizzo degli SDK di Aspose.Cells Cloud

Utilizzare gli SDK rappresenta il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello, consentendo di convertire i dati di tabelle di fogli elettronici in immagini con un numero minimo di righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose.Cells utilizzando diversi SDK: