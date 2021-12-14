---
title: "Calculate all formulas in a Workbook"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /workbook/calculate-all-formulas/
aliases: [/calculate-all-formulas-in-a-workbook/]
keywords: "REST API, spreadsheets, excel, calculate, formulas"
description: "Cells.Cloud API for Excel operate: calculate all formulas on the workbook."
weight: 140
---

This REST API `calculate` all formulas on Excel workbook.


**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|ignoreError|string| true/false|
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|options|CalculationOptions|The data file saves into request body.|


**CalculationOptions**
|Parameter Name|Type|Description|
| :- | :- | :- |
|CalcStackSize|integer| |
|IgnoreError|string|true/false|
|PrecisionStrategy|string| |
|Recursive|string|true/false|


## REST API*

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/{name}/calculateformula|POST|Calculate Formula|[PostWorkbookCalculateFormula](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"CalcStackSize\": 1, \"IgnoreError\": true, \"PrecisionStrategy\": \"string\", \"Recursive\": true}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}


## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="7" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" tabName7="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "" "f21c488545888fe78bbd97e47790246b" "Examples-.NET-CellsWorkbookPostWorkbookCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Workbook-PostWorkbookCalculateFormula-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Workbook-post_workbook_calculate_formula-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Workbook-PostWorkbookCalculateFormula-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Workbook-CalculateFormulas-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "92c0f4d6c417e88e16cce17e10dd3287" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "2a8718092583a1d495bac5034f80a503" >}}

{{< /tab >}}

{{< /tabs >}}
