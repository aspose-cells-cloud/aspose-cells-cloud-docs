---
title: Ottieni l'elenco dei file - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Ottieni file Lis
type: docs
url: /it/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Scopri come recuperare un elenco di file da una cartella specificata utilizzando Aspose.Cells API. Questa guida fornisce dettagli sui parametri di richiesta, sulla struttura della risposta ed esempi di codice in vari linguaggi di programmazione
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Gestione file cloud, Ottieni file Lis
---
## **Excel API: Ottieni elenco file**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Descrizione della funzione**

 IL**getFilesList**API consente agli utenti di recuperare un elenco completo di file e cartelle contenuti in una directory specificata nell'archivio cloud Aspose.Cells. Questo endpoint è fondamentale per la gestione efficiente dei file e supporta vari formati di file.

###  I parametri di richiesta di**getFilesList** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| sentiero| Corda| Sentiero| Percorso della cartella nell'archiviazione cloud da cui recuperare l'elenco dei file.|
| Nome di archiviazione| Corda| Domanda| Nome dell'archivio a cui accedere.|

### **Descrizione della risposta**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) definisce un'interfaccia di programmazione accessibile al pubblico che consente interazioni REST direttamente da un browser Web, facilitando l'integrazione e i test.

## Excel API SDK

 Utilizzare un SDK è l'approccio ottimale per accelerare il processo di sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del progetto. Per un elenco completo degli SDK Cloud Aspose.Cells, visita il sito[Repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice illustrano come richiamare i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
