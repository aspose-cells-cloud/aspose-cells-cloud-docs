---
title: Crea un workboo Excel vuoto
second_title: Aspose.Cells Cloud Documen
linktitle: Workboo vuoto
type: docs
url: /it/workbook/create/empty-workbook/
aliases: [/create-an-empty-excel-workbook/,/workbook/new/]
keywords: How to create an Excel workbook
description: Aspose.Cells Cloud REST API come creare una cartella di lavoro Excel vuota. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
Questo REST API indica di creare un `empty workbook`.

**Parametro di ricerca**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
|templateFile|corda||
|file di dati|corda||
|isWriteOver|corda| vero falso|
|cartella|corda|Cartella di lavoro originale.|
|storageName|corda|Nome di archiviazione.|

**Parametro del corpo della richiesta**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
|dati|file||


## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento alla risorsa**|
|:- |:- |:- |:- |
|/celle/{nome}|METTERE|Crea una cartella di lavoro vuota|[Put Cartella di lavoro Crea](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate)|


 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** strumento da riga di comando per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" -H "accept: application/json" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{
  "Status": "string",
  "Workbook": {
    "FileName": "string",
    "Links": [
      {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Names": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Settings": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "IsWriteProtected": "string",
    "IsProtected": "string",
    "IsEncryption": "string",
    "Password": "string"
  }
}

```

{{< /tab >}}

{{< /tabs >}}



## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-CreateEmptyWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "ad2ef2b72254d01920fc05d3ae506375" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "9e868bc0e2c275d9552372e65ca554b3" >}}

{{< /tab >}}

{{< /tabs >}}
