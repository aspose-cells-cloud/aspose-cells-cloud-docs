﻿---
title: Ripara il file Excel
second_title: Aspose.Cells Cloud Documen
type: docs
linktitle: Ripara il file Excel
url: /it/repair-excel-files/
keywords: Repair Excel, ODS, WPS, and so on files
description: Ripara i file Excel utilizzando Aspose.Cells Cloud REST API. API supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift per una rapida integrazione nei tuoi progetti.
weight: 39
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Riparazione
---
Questo REST API indica i file `repair` Excel.

- Ripara XLS, XLSX, XLSM, XLSB, ODS e così via.
- Supporta più file.

Aspose.Cells Cloud Excel Repair recupera i dati dai file corrotti Excel online senza installazione. I file corrotti Excel possono essere un problema perché non riesci ad aprirli. Puoi provare l'app Aspose.Cells Cloud Excel Repair per recuperare i dati dai file corrotti Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| file| file| formData| File da caricare|
| formato| corda| domanda| Formato di output, il valore predefinito è null, il formato di output è uguale al formato del file di input.|

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/repair" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash

{
    "Files":
    [
        {
            "Filename":"xxxx1.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        {
            "Filename":"xxxx2.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
