---
title: Carica il file sul cellulare Aspose
second_title: Developer Guide for File Uploa
linktitle: Carica file
type: docs
url: /it/upload-file/
keywords: Aspose, file upload, Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, upload Excel files, match blank cell
description: Guida completa su come caricare file utilizzando Aspose Cells API, inclusi parametri e struttura della risposta
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, abbina tutte le celle vuote in un foglio di lavoro Excel, carica file
---
## **Aspose Cells API: Carica file**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Descrizione della funzione**

 IL**caricareFile** API consente agli sviluppatori di caricare i file direttamente sullo storage cloud per l'elaborazione con Aspose Cells.

###  I parametri di richiesta di**caricareFile** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| Carica file| File| FormData|Carica i file sullo storage cloud.|
| sentiero| Corda| Sentiero| Percorso di destinazione nell'archiviazione cloud. Specifica il percorso in cui caricare il file.|
| Nome di archiviazione| Corda| Domanda| Nome dell'archivio in cui verrà caricato il file.|

### **Descrizione della risposta**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) fornisce una descrizione dettagliata di API, consentendo agli sviluppatori di eseguire interazioni REST direttamente da un browser web.

## Aspose Cells API SDK

 L'utilizzo di un SDK migliora l'efficienza dello sviluppo gestendo i dettagli di basso livello, consentendo agli sviluppatori di concentrarsi sulle attività del progetto. Visita[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come chiamare i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
