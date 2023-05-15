---
title: Copia cartella
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/folder/copy/
keywords: Learn how to copy folder with Aspose Cells Cloud REST API
description: Scopri come copiare la cartella con Aspose Cells Cloud REST API L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica `copy folder`.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| srcPath| corda| sentiero| Percorso della cartella di origine, ad esempio '/src'|
| destPath| corda| domanda| Percorso della cartella di destinazione, ad esempio '/dst'|
| srcStorageName| corda| domanda| Nome dell'archiviazione di origine|
| destStorageName| corda| domanda| Nome dell'archiviazione di destinazione|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 