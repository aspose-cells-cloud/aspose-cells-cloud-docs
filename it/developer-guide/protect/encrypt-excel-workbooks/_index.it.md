---
title: Crittografare un workboo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Cripta
type: docs
url: /it/workbook/encrypt/
aliases: [/encrypt-excel-workbooks/]
keywords: Encrypt Excel workbook
description: Aspose.Cells Cloud REST API supporta la crittografia Excel cartella di lavoro. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
Questo REST API crittografa un Excel `workbook`.

**Parametro di ricerca**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
|cartella|corda|Cartella di lavoro originale.|
|storageName|corda|Nome di archiviazione.|

**Parametro del corpo della richiesta**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
|crittografia|WorkbookEncryptionRequest||

**WorkbookEncryptionRequest**
|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
|Tipo di crittografia|corda|XOR/Compatible/EnhancedCryptographicProviderV1/StrongCryptographicProvider|
|Lunghezza chiave|numero intero||
|Parola d'ordine|corda||


## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento spavaldo**|
|:- |:- |:- |:- |
|/celle/{nome}/crittografia|INVIARE|Crittografare il documento Excel|[PostEncryptDocument](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument)|

 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** strumento da riga di comando per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"EncryptionType\": \"XOR\", \"KeyLength\": 128, \"Password\": \"mateen\"}"

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

## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostEncryptDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-EncryptWorkbook-encrypt-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostEncryptDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-encrypt_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DecryptExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-EncryptWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-EncryptWorkbook-encrypt-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-EncryptWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b126fc35b8677c4d085726ef83a8a873" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "55c256cbd15c8b96f9ee3c40e4ad2300" >}}

{{< /tab >}}

{{< /tabs >}}
