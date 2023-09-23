﻿---
title: Kryptera en Excel workboo
second_title: Aspose.Cells Cloud Documen
linktitle: Kryptera
type: docs
url: /sv/workbook/encrypt/
aliases: [/encrypt-excel-workbooks/]
keywords: Encrypt Excel workbook
description: Aspose.Cells Cloud REST API stöder kryptering Excel arbetsbok. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 20
---
Denna REST API krypterar en Excel `workbook`.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng|Lagringsnamn.|

**Begär kroppsparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|kryptering|WorkbookEncryptionRequest||

**WorkbookEncryptionRequest**
|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|EncryptionType|sträng|XOR/Compatible/EnhancedCryptographicProviderV1/StrongCryptographicProvider|
|KeyLength|heltal||
|Lösenord|sträng||


## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger Link**|
|:- |:- |:- |:- |
|/celler/{namn}/kryptering|POSTA|Kryptera Excel Dokument|[PostEncryptDocument](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.

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

## Cloud SDK-familj

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:


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