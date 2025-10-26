---
title: "Aspose.Cells Cloud Web API - Trim character"
second_title: "Document"
ArticleTitle: "Trim character in a spreadsheet file – Online, Short-Code"
linktitle: "Trim Character"
type: docs
url: /trim-character/
keywords: "API, Excel API, Trim Content, Remote Spreadsheet, Cloud Storage, Text Trim, REST API"
description: "The TrimSpreadsheetContent API is designed to process and trim content within a spreadsheet. This API allows users to remove extra spaces, line breaks, or other unnecessary characters from the content of selected cells. It is particularly useful for cleaning up data entries and ensuring consistency in spreadsheet formatting "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

The trim character API is designed to process and trim content within a spreadsheet. This API allows users to remove extra spaces, line breaks, or other unnecessary characters from the content of selected cells. It is particularly useful for cleaning up data entries and ensuring consistency in spreadsheet formatting

## **Overview**

- **Trim the first and last spaces**
  - Remove extra spaces at the beginning and end of text
  - Improve data appearance neatness and readability
  
- **Processing of extra spaces between words**
  - Eliminate extra spaces between words
  - Solve the format confusion caused by multi-source data

- **Special spaces removed**
  - Specially clear non-breaking spaces
  - Ensure data accuracy and consistency

- **Line break management**
  - Remove extra or all line breaks.
  - Keep cell content organized and professional looking

## **TrimCharacter API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/trim
```

### The request parameters of **trimCharacter** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|trimContent|String|Query|Specify the trim content.|
|trimLeading|Boolean|Query|Specify to trim content from the beginning.|
|trimTrailing|Boolean|Query|Specify to trim content from the end.|
|trimSpaceBetweenWordTo1|Boolean|Query|Remove excess spaces between words within a cell.|
|trimNonBreakingSpaces|Boolean|Query|Remove non-breaking spaces.|
|removeExtraLineBreaks|Boolean|Query|Remove extra line breaks.|
|removeAllLineBreaks|Boolean|Query|Remove all line breaks.|
|worksheet|String|Query|Specify the worksheet of spreadsheet.|
|range|String|Query|Specify the worksheet range of spreadsheet.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|

### **Response**

```json
{
File
}
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Merge Local Spreadsheet API?

## Why should you use the Merge Local Spreadsheet API?

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/TrimCharacter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Trim character for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}

[](images/source001.png)
[](images/target001.png)
