---
title: "Aspose.Cells Cloud Text Trimming Web API - Remove Extra Spaces & Line Breaks"
second_title: "Document"
ArticleTitle: "Excel Data Cleaner - Trim Characters, Spaces & Line Breaks Automatically – Online, Short-Code"
linktitle: "Trim Character"
type: docs
url: /trim-character/
keywords: "Excel text trimming API, remove extra spaces Excel, delete line breaks Excel, clean spreadsheet content, Aspose.Cells trim characters, Excel data cleaning tool, trim unnecessary characters, normalize cell formatting, Excel content cleanup API"
description: "Clean Excel data by trimming extra spaces, removing line breaks, and eliminating unnecessary characters from selected cells with Aspose.Cells Trim Character API. Ensure consistent spreadsheet formatting and data quality."
weight: 100
---

Automatically trim unnecessary characters, extra spaces, and line breaks from Excel cells using Aspose.Cells Trim Character API. Clean data entries and maintain consistent formatting across your spreadsheets.

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

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/content/trim
```

### The request parameters of **trimCharacter** API are

| Parameter Name          | Type    | Path/Query String/HTTPBody | Description                                                                                                                                                         |
| :---------------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet             | File    | FormData                   | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc.                                                                           |
| trimContent             | String  | Query                      | Specifies the specific characters or strings to be trimmed from cell content. Can be a single character, multiple characters, or a custom pattern.                  |
| trimLeading             | Boolean | Query                      | When `true`, removes the specified characters from the beginning of each cell's content.                                                                            |
| trimTrailing            | Boolean | Query                      | When `true`, removes the specified characters from the end of each cell's content.                                                                                  |
| trimSpaceBetweenWordTo1 | Boolean | Query                      | When `true`, reduces multiple consecutive spaces between words to a single space within each cell.                                                                  |
| trimNonBreakingSpaces   | Boolean | Query                      | When `true`, removes non-breaking space characters (Unicode U+00A0) from the cell content.                                                                          |
| removeExtraLineBreaks   | Boolean | Query                      | When `true`, reduces multiple consecutive line breaks to a single line break within each cell.                                                                      |
| removeAllLineBreaks     | Boolean | Query                      | When `true`, removes all line break characters from the cell content.                                                                                               |
| worksheet               | String  | Query                      | _(Optional)_ The name of the worksheet where text trimming will be applied. If omitted, the operation applies to the first worksheet.                               |
| range                   | String  | Query                      | _(Optional)_ The cell range where text trimming will be applied (e.g., `"A1:C10"`). If omitted, the operation applies to all used cells in the specified worksheet. |
| outPath                 | String  | Query                      | _(Optional)_ The cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder.                          |
| outStorageName          | String  | Query                      | The name of the cloud storage where the output file will be stored.                                                                                                 |
| region                  | String  | Query                      | _(Optional)_ Sets the locale for text processing, which may affect space and line break handling for specific languages (e.g., `"en-US"`, `"ar-SA"`).               |
| password                | String  | Query                      | _(Optional)_ If the uploaded spreadsheet is password-protected, provide the password to open and process the file.                                                  |

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
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Trim Character API?

- **User Input Normalization**: Clean up manual user input table data, removing excess spaces and line breaks.
- **Customer Database Maintenance**: Clean up redundant spaces and formatting issues in customer names, addresses, and contact details.
- **Automated Report Cleanup**: Cleans up the data source format before generating automated reports.
- **Data Migration Preparation**: Clean up formatting issues before data is migrated to the new system

## Why should you use the Trim Character API?

- **Reduced Labor Costs**: Eliminate time-consuming manual efforts for data cleaning
- **Reduced Error Cost**: Avoid analysis errors caused by formatting issues
- Pay Per Use: No fixed fees, only the actual throughput is billed
- **Zero Infrastructure Investment**: No need to maintain servers or software
- **Multi-format Support**: Supports multiple format processing such as XLSX, XLS, CSV, ODS, etc
- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Cost-Effective**: You can remove deduplicate characters without first uploading the workbook, which saves storage space and reduces costs.

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
