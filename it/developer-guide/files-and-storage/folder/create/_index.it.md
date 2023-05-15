---
title: Crea cartella
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/folder/create/
keywords: Learn how to create folder with Aspose Cells Cloud REST API
description: Scopri come creare una cartella con Aspose Cells Cloud REST API L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica `create folder`.

## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero|Percorso della cartella da creare, ad esempio 'folder_1/cartella_2/' |
| storageName| corda| domanda| Nome di archiviazione|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
 

