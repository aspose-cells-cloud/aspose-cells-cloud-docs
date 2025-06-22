---
title: Abbina tutte le celle vuote in un foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Abbina cella vuota
type: docs
url: /it/autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: Match all blank cells in the filter list on an Excel worksheet
description: Il Cloud Aspose.Cells API supporta la corrispondenza di tutte le celle vuote nell'elenco dei filtri su un foglio di lavoro Excel. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel
---
Questo REST API indica a `match` tutti gli `blank cell` nell'elenco dei filtri su un foglio di lavoro Excel.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
 
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| Nome del foglio| corda| sentiero||
| Indice del campo| intero| domanda||
| cartella| corda| domanda||
| Nome di archiviazione| corda| domanda| nome di archiviazione.|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}
