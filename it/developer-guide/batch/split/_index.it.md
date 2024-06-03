---
title: Divisione batch
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API supporta file suddivisi in batch. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Divisione batch
---
Questo REST API indica `batch split` del file idoneo.
 
## RSETAPI
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
|BatchSplitRequest|| corpo||

**Proprietà BatchSplitRequest**
 
Nome | Digitare | Descrizione | Appunti
------------ | ------------- | ------------- | -------------
 Cartella di origine | stringa | | [facoltativo]SorgenteStorage | stringa | | [opzionale]Condizione di corrispondenza | MatchConditionRequest | | [facoltativo]Formato | stringa | | [facoltativo]DaIndice | intero | | [facoltativo]ToIndex | intero | | [facoltativo]Cartella esterna | stringa | | [facoltativo]SalvaOpzioni | SalvaOpzioni | | [opzionale]**Proprietà MatchConditionRequest**
 
Nome | Digitare | Descrizione | Appunti
------------ | ------------- | ------------- | -------------
 Modello Regex | stringa | | [opzionale]CondizioniFullMatch | stringa[]| | [facoltativo]Il[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchsplit) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.
 
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
 
## Famiglia di SDK Cloud
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività suddivise. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.
 
I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

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

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}

