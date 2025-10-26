---
title: Scarica il file da Aspose.Cells AP
second_title: Developer Guide for Aspose.Cells AP
linktitle: Scarica il file AP
type: docs
url: /it/download-file/
keywords: Aspose.Cells API, Download File, REST API, Excel File, Office Cloud, Spreadsheet Download, File Management, File Retrieval, CSV, PDF, JSON, Markdow
description: Scopri come utilizzare Aspose.Cells API per scaricare file tra cui Excel, PDF, CSV e in modo più efficiente
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Scarica file Excel, Recupera file vuoto Cells
---
## **Excel API: Scarica file**

```
GET http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Descrizione della funzione**

 IL**ScaricaFile** API consente di recuperare i file archiviati nel cloud storage Aspose. Questa funzionalità è essenziale per gestire e accedere a vari formati di file, tra cui fogli di calcolo, PDF e CSV.

###  I parametri di richiesta di**ScaricaFile** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| sentiero| Corda| Sentiero| Il percorso del file che vuoi scaricare.|
| Nome di archiviazione| Corda| Domanda| Nome dell'archivio da cui verrà recuperato il file.|
| ID versione| Corda| Domanda| Identificativo della versione del file da scaricare, se applicabile.|

### **Descrizione della risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
