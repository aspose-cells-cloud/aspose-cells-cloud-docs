---
title: Utilizzo del disco
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/storage/disc-usage/
keywords: Learn how to get disc-usage with Aspose Cells Cloud REST API
description: Scopri come ottenere l'utilizzo del disco con Aspose Cells Cloud REST API SDK che supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica `get disc usage`.
 
## RSETAPI
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/disc
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| storageName| corda| domanda| Nome dell'archivio|

 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK Cloud
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.
 
I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 