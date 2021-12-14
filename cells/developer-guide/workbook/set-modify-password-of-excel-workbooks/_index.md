---
title: "Set modify password of an Excel workbook"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /workbook/modify-password/
aliases: [/set-modify-password-of-excel-workbooks/]
keywords: "set a password of workbook, modify a password of workbook, set a password of spreadsheets using SDK for Python, modify a password of spreadsheets, protect the workbook from changes"
description: "REST API provides the ability to set or modify password of a workbook. SDKs are available for .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more languages."
weight: 100
---

This REST API modify Excel `workbook` `password`.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|password|PasswordRequest| |

**PasswordRequest**

|Parameter Name|Type|Description|
| :- | :- | :- |
|Password|string| |


## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/{name}/writeProtection|PUT|Write Protect a Document|[PutDocumentProtectFromChanges](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: application/json" \
-d "{ \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "" "f21c488545888fe78bbd97e47790246b" "Examples-.NET-CellsWorkbookPutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-workbook-SetModifyPassword-set-modify-password.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Workbook-PutDocumentProtectFromChanges-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Document-protect_document_from_changes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "SetModifyPassword.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Workbook-SetModifyPassword-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-SetModifyPassword-set-modify-password.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Workbook-SetModifyPassword-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "b115c4b25d06a781e0cbfc6781661127" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cloud" "460c8cbed8fdb9831132460e379628ac" >}}

{{< /tab >}}

{{< /tabs >}}
