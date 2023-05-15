---
title: Esporta oggetto OLE
second_title: Aspose.Cells Cloud Documen
linktitle: OLE Ogg
type: docs
url: /it/export/excel-ole-object/
keywords: Export Excel OLE object to kinds of format files
description: Aspose.Cells Cloud REST API supporta l'esportazione di oggetti OLE Excel in tipi di file di formato. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
- **RIPOSO API**

|**API**|**Tipo**|**Descrizione**|**Collegamento spavaldo**|
|:- |:- |:- |:- |
|/celle/esporta|INVIARE|Esporta Excel dal contenuto della richiesta in un formato|[PostExport](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)|


 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** strumento da riga di comando per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.



- **Richiesta**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Risposta**

```bash
{
    "Files": [{
        "Filename": "OLESlide.ppt",
        "FileSize": 390,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "OLEDoc.docx",
        "FileSize": 382,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **Famiglia di SDK cloud**

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-shape-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export-shape-tiff.php" >}}

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

{{< /tabs >}}
