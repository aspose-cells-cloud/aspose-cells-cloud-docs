---
title: "Add Background in Workbook"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /workbook/add-background/
aliases: [/working-with-workbook/]
keywords: "REST API, spreadsheets, excel, background image"
description: "Cells.Cloud API for Excel operate: workbook add background."
weight: 160
---

This REST API add `background` into Excel work sheet.


**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|picPath|string|picture position.|
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|datafile|data file |The data file saves into request body.|

## REST API*

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/background|PUT|Add background in excel file|[PutWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

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

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Perl" tabName6="Ruby" tabName7="PHP" tabName8="Node.js" tabName9="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "4f5e06ec874b8b698dfa0e5359c85f96" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "b47350fc841e7c7e8889b1f57723ad94" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "bef09b36e0e7b769022bd810898dbd73" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "a984b922e2a7373755fb877e8754452b" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "7b9fa1a76c49c164d034342a2a59d4e0" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "a56d3fa3fff9c61191ee3e869ec51cdd" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "4a63cab36bb9f03e4e58bc30267b60b8" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cloud" "4009896954c23f8a1394b3757a30ee9d" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "d3b449b5e5e2cdbb25da9e8de37bdccc" >}}

{{< /tab >}}

{{< /tabs >}}
