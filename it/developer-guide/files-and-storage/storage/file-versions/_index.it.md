---
title: Versione file
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/storage/file-versions/
keywords: Learn how to get file version with Aspose Cells Cloud REST API
description: Scopri come ottenere la versione del file con Aspose Cells Cloud REST API L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica ottenere `file versions`.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso del file, ad esempio '/file.ext'|
| storageName| corda| domanda| Nome di archiviazione|

 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 