---
title: Ottieni la versione del file
second_title: Documen
linktitle: Ottieni la versione del file
type: docs
url: /it/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Recupera e gestisci le versioni dei file archiviati nel Cloud Aspose.Cells, migliorando la gestione dei documenti e la collaborazione
weight: 100
kwords: Ottieni versioni file, Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, gestione documenti
---
## **Excel API: Ottieni versioni file**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Descrizione della funzione**

 IL**OttieniVersioniFile** API consente agli utenti di recuperare le diverse versioni di un file specificato archiviate nel Cloud Aspose.Cells. Questa funzionalità è fondamentale per mantenere l'integrità dei documenti e monitorare le modifiche nel tempo.

###  I parametri di richiesta di**OttieniVersioniFile** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| sentiero| Corda| Sentiero| Percorso del file di cui recuperare le versioni.|
| Nome di archiviazione| Corda| Domanda| Nome dell'archivio in cui si trova il file.|

### **Descrizione della risposta**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)fornisce un'interfaccia di programmazione completa per eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 L'utilizzo di un SDK semplifica lo sviluppo astraendo le complessità di basso livello, consentendo agli sviluppatori di concentrarsi sulle funzionalità principali. Esplora[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells in vari linguaggi di programmazione:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}
