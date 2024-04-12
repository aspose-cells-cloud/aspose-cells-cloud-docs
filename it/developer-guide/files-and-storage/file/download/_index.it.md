---
title: Scarica Fil
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/file/download/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Scopri come scaricare il file con Aspose Cells Cloud REST API SDK che supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica `download file`.
 
## RSETAPI
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso del file, ad esempio "/cartella/file.ext"|
| storageName| corda| domanda| Nome dell'archivio|
| versioneId| corda| domanda| ID della versione del file da scaricare|
 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash

{
    Stream
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK Cloud
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.
 
I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
 
 

