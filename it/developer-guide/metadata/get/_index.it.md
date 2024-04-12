---
title: Ottieni metadati dal file Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ottieni senza usare storag
type: docs
url: /it/metadata/get/
keywords: Get properties from Excel files
description: Aspose.Cells Cloud REST API supporta il recupero delle proprietà da file Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 23
---
Questo REST API indica di ottenere `metadata` da più file Excel.

```bash

POST https://api.aspose.cloud/v3.0/cells/metadata/get

```

- **Parametro di query**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| tipo| corda| TUTTO/Incorporato/Personalizzato|


- **Richiedi parametro corpo**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|file Excel| file di dati|Il file di dati viene salvato nella prima parte del contenuto in più parti.|

- **Risposta**

```bash
{
    [
        { 
            "Name":"test1",
            "Value":"test1",
            ...
        },
        { 
            "Name":"test2",
            "Value":"test3",
            ...
        }
    ]
}
```
- **Famiglia di SDK Cloud**

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Metadata-Get.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-MetaData-Get.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Metadata-Get.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}
{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMetadata-Get.py" >}}
{{< /tab >}}
{{< /tabs >}}
