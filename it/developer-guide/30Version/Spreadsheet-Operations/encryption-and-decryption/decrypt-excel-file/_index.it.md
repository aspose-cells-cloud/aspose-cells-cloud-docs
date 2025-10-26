---
title: Decifrare un workboo Excel
second_title: Documen
linktitle: Decifrare un file Excel
type: docs
url: /it/excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/,/workbook/decrypt/]
keywords: REST API, spreadsheets, excel, decryp
description: "Cells.Cloud API per Excel opera: decifra una cartella di lavoro Excel"
weight: 50
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Decrittografa una cartella di lavoro Excel
---
Questo REST API decifra un Excel `workbook`.

**Parametro di query**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|cartella|corda|Cartella della cartella di lavoro originale.|
|Nome di archiviazione|corda|Nome dell'archivio.|

**Parametro del corpo della richiesta**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|crittografia|WorkbookEncryptionRequest||

**WorkbookEncryptionRequest**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|Tipo di crittografia|corda|XOR/Compatibile/EnhancedCryptographicProviderV1/StrongCryptographicProvider|
|Lunghezza chiave|intero||
|Password|corda||

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento Swagger**|
|:- |:- |:- |:- |
|/cells/{name}/encryption|ELIMINA|Decifrare un documento|[EliminaDecifraCartella di lavoro](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"EncryptionType\": \"XOR\", \"KeyLength\": 1280, \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
