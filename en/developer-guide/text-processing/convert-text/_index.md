---
title: "Aspose.Cells Cloud Web API - Convert Text to Numbers in Excel & Clean Special Characters"
second_title: "Document"
ArticleTitle: "Excel Data Cleaner - Convert Text to Numbers & Remove Unwanted Characters"
linktitle: "Convert Text"
type: docs
url: /convert-text/
keywords: "Aspose.Cells convert text, Excel text to numbers, remove special characters Excel, replace line breaks Excel, normalize accented characters, Excel data cleaning API"
description: "Convert text‑formatted numbers to numeric values, replace unwanted characters and line breaks, and normalize accented characters in Excel files using Aspose.Cells Cloud API."
weight: 100
---

Clean Excel data by converting text‑formatted numbers to numeric values, replacing unwanted characters and line breaks, and normalizing accented characters to standard letters with the Aspose.Cells API.

## Overview

**Convert numbers‑as‑text, strip junk, swap accents—one call, zero formulas.**

- **Convert numbers stored as text to numbers**: Transform numeric data stored as text into true numbers, ensuring accurate calculations and proper data representation.
- **Replace specific characters**: Replace all occurrences of specified characters in the selected cells at once to standardize your data.
- **Convert line breaks to space, comma or semicolon**: Improve readability by converting line breaks to spaces, commas, or semicolons, creating a more organized and visually appealing presentation.
- **Replace accented characters**: If your data is in different languages, you can swap accented characters like “é” or “ü” with their non‑accented counterparts, enhancing consistency and clarity.

## **ConvertText API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/content/convert/text
```

### The request parameters of **convertText** API are

| Parameter Name   | Type   | Path/Query String/HTTPBody | Description                                                                                                                                                           |
| ---------------- | ------ | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | File   | FormData                   | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc.                                                                             |
| convertTextType  | String | Query                      | Specifies the type of text conversion to apply, such as converting text‑formatted numbers to numeric values, or converting accented characters to plain equivalents.  |
| sourceCharacters | String | Query                      | Specifies the characters, strings, or patterns to be replaced or removed from the text (e.g., `"é,è,ê"`, `"#N/A"`, `"\\n"` for line breaks).                          |
| targetCharacters | String | Query                      | Specifies the replacement characters or strings that will replace the source characters (e.g., `"e"` for accented letters, `""` for removal, `" "` for line breaks).  |
| worksheet        | String | Query                      | _(Optional)_ The name of the worksheet where text conversion will be applied. If omitted, the operation applies to the first worksheet.                               |
| range            | String | Query                      | _(Optional)_ The cell range where text conversion will be applied (e.g., `"A1:C10"`). If omitted, the operation applies to all used cells in the specified worksheet. |
| outPath          | String | Query                      | _(Optional)_ The cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder.                            |
| outStorageName   | String | Query                      | The name of the cloud storage where the output file will be stored.                                                                                                   |
| region           | String | Query                      | _(Optional)_ Sets the locale for text conversion rules, particularly relevant for language‑specific character handling (e.g., `"en-US"`, `"fr-FR"`).                  |
| password         | String | Query                      | _(Optional)_ If the uploaded spreadsheet is password‑protected, provide the password to open and process the file.                                                    |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token, or invalid client ID and secret.
- **404 Not Found**: The spreadsheet file is not accessible.
- **500 Server Error**: The spreadsheet encountered an anomaly while obtaining calculation data.

## Where should we use the Convert Text API?

- **Number Format Correction**: Convert numbers stored as text (e.g., “123.45”) into a numeric format suitable for calculations.
- **Special Character Cleanup**: Remove unnecessary special symbols, extra spaces, or invisible characters from the data.
- **Line Break Handling**: Replace line breaks in cells with spaces or other delimiters.
- **Accent Character Normalization**: Convert accented letters (e.g., “é”, “ñ”) to standard letters (“e”, “n”).
- **CSV File Preprocessing**: Standardize text format before importing CSV files into Excel.

## Why should you use the Convert Text API?

- **Automatic Format Conversion**: Convert text‑formatted numbers into calculable values in bulk with a single request.
- **Character Standardization**: Uniformly handle special characters, diacritics, and encoding issues.
- **Data Consistency**: Ensure that the text format is completely uniform across the entire dataset.
- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and providing comprehensive documentation. Compared with building custom text‑processing solutions, this significantly reduces development workload.
- **Cost‑Effective**: You can convert text without first uploading the workbook, which saves storage space and reduces costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/ConvertText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Convert Text for cells with minimal code.  
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
