---
title: Esiste spazio di archiviazione
second_title: Documen
linktitle: Esiste spazio di archiviazione
type: docs
url: /it/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Scopri come verificare se esiste spazio di archiviazione utilizzando Aspose.Cells REST API. Questa guida fornisce informazioni dettagliate sull'endpoint API, parametri di richiesta e descrizioni delle risposte
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel
---
## **Excel API : Esiste spazio di archiviazione**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Descrizione della funzione**

 IL**storageExists**API verifica se esiste uno storage specificato nel servizio cloud Aspose.Cells. Questa funzionalità è fondamentale per garantire che tutte le operazioni che dipendono dallo storage possano procedere senza errori.

###  I parametri di richiesta di**storageExists** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Nome di archiviazione|Corda|Sentiero|Nome dell'archivio di cui verificare l'esistenza.|

### **Descrizione della risposta**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) definisce un'interfaccia di programmazione accessibile al pubblico, che consente agli sviluppatori di interagire senza problemi con REST API direttamente da un browser web.

## Excel API SDK

 L'utilizzo di un SDK è l'approccio più efficiente per accelerare lo sviluppo. Un SDK astrae i dettagli di implementazione di basso livello, consentendo agli sviluppatori di concentrarsi sulle attività del progetto. Per un elenco completo degli SDK Cloud Aspose.Cells disponibili, visitare il sito https://www.sdk.com/cloud-sdk/.[Repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come effettuare chiamate API ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
