---
title: "Aspose.Cells Cloud Web API - Convert text"
second_title: " Aspose.Cells Cloud – Online, Short-Code,"
linktitle: "Convert Text"
type: docs
url: /convert-text/
keywords: ""
description: "Indicates converting the numbers stored as text into the correct number format, replacing unwanted characters and line breaks with the desired characters, and converting accented characters to their equivalent characters without accents. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

Indicates converting the numbers stored as text into the correct number format, replacing unwanted characters and line breaks with the desired characters, and converting accented characters to their equivalent characters without accents.

## Overview

**Convert numbers-as-text, strip junk, swap accents—one call, zero formulas.**

- **Convert numbers stored as text to numbers**: Transform numeric data stored as text to numbers, ensuring accurate calculations and proper data representation.
- **Replace specific characters**: Replace all occurrences of specified characters in all the selected cells at once to standardize your information.
- **Convert line breaks to space, comma or semicolon**: Improve the readability of your sheets by converting line breaks to space, comma, or semicolon, creating a more organized and visually appealing presentation.
- **Replace accented characters**: If your data is in different languages, you have the option to swap accented characters like "é" or "ü" with their non-accented counterparts. This enhances consistency and clarity in your text.

## **ConvertText API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/convert/text
```

### The request parameters of **convertText** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|convertTextType|String|Query|Indicates the conversion of text type.|
|sourceCharacters|String|Query|Indicates the source characters.|
|targetCharacters|String|Query|Indicates the target characters.|
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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Merge Local Spreadsheet API?

## Why should you use the Merge Local Spreadsheet API?

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/ConvertText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Convert text for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
