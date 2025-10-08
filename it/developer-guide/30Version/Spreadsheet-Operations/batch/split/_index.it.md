---
title: Batch Spli
second_title: Documen
type: docs
url: /it/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API supporta la suddivisione in batch dei file. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Batch Split
---
Questo REST API indica il file idoneo `batch split`.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| BatchSplitRequest|| corpo||

**Proprietà BatchSplitRequest**

Nome | Tipo | Descrizione | Note
------------ | ------------- | ------------- | -------------
 SourceFolder | stringa | | [facoltativo]SourceStorage | stringa | | [facoltativo]MatchCondition | MatchConditionRequest | | [facoltativo]Format | stringa | | [facoltativo]FromIndex | intero | | [facoltativo]ToIndex | intero | | [facoltativo]OutFolder | stringa | | [facoltativo]SaveOptions | SaveOptions | | [facoltativo]**Proprietà MatchConditionRequest**

Nome | Tipo | Descrizione | Note
------------ | ------------- | ------------- | -------------
 RegexPattern | stringa | | [facoltativo]FullMatchConditions | stringa[]| | [facoltativo]The[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sui tuoi compiti suddivisi. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

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
{{< /tab >}}

{{< /tabs >}}
