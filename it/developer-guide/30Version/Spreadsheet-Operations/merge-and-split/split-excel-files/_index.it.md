---
title: "Dividere un file Excel in più file"
ArticleTitle: "Come dividere un file Excel in più file utilizzando l'API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Dividere un file Excel"
type: docs
url: /it/split-multi-excel-files/
aliases: [  /it/split/multi-files/ ]
keywords: "Excel, Aspose.Cells Cloud, API REST, dividere cartella di lavoro, file multipli, JPEG, PNG, PDF, CSV, JSON"
description: "L'API REST Aspose.Cells Cloud consente di dividere una cartella di lavoro Excel in più file in vari formati. Questa documentazione fornisce i parametri di richiesta, un esempio cURL e campioni di codice SDK per linguaggi come C#, Java, PHP, Ruby, Node.js, Python, Perl e Go."
weight: 130
---

Questa API REST divide la **cartella di lavoro** Excel in più file in diversi formati.

> **Prerequisiti** – Per utilizzare questa API è necessario ottenere un token JWT valido, assicurarsi di utilizzare una versione SDK supportata e verificare che la cartella di lavoro sia archiviata in una posizione di archiviazione supportata. L'API impone inoltre limiti di dimensione del file, descritti nelle linee guida della piattaforma.

## API PostWorkbookSplit

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro       | Tipo    | Posizione   | Descrizione                                                                                  | Obbligatorio |
| -------------------- | ------- | ----------- | -------------------------------------------------------------------------------------------- | ------------ |
| files[]              | file    | formData    | Una o più cartelle di lavoro Excel da **dividere**. Utilizzare `file1`, `file2`, … nella richiesta. | Sì           |
| format               | string  | Query       | Format di output desiderato per i file risultanti.                                          | No           |
| from                 | integer | Query       | Indice iniziale del foglio di lavoro.                                                        | No           |
| to                   | integer | Query       | Indice finale del foglio di lavoro.                                                          | No           |
| horizontalResolution | integer | Query       | Risoluzione orizzontale dell'immagine.                                                       | No           |
| verticalResolution   | integer | Query       | Risoluzione verticale dell'immagine.                                                         | No           |
| outFolder            | string  | Query       | Cartella di output per i file risultanti.                                                    | No           |
| splitNameRule        | string  | Query       | Regola di denominazione applicata ai file risultanti.                                        | No           |
| folder               | string  | Query       | Cartella contenente la cartella di lavoro originale.                                         | No           |
| storageName          | string  | Query       | Nome dell'archiviazione da utilizzare.                                                       | No           |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[nome file1]",
        "Filesize" : [dimensione file],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[nome file2]",
        "Filesize" : [dimensione file],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[nome file3]",
        "Filesize" : [dimensione file],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                          |
|--------|-----------------------------|------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PostWorkbookSplit con gli SDK

### Specifica dell'API PostWorkbookSplit

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}