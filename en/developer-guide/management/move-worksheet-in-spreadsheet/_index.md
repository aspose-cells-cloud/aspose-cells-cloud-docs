---
title: "Aspose.Cells Cloud Excel: Move Worksheet Web API – Change Sheet Position Programmatically"
second_title: "Document"
ArticleTitle: "How to Move Worksheets in Excel – Rearrange Sheet Order & Position"
linktitle: "Move Worksheet in Spreadsheet"
type: docs
url: /move-worksheet-in-spreadsheet/
keywords: "move worksheet API, rearrange sheets API, change sheet order API, Excel tab management API, Aspose Cells REST API, automate sheet positioning, workbook organization API, spreadsheet structure API, cloud Excel automation, batch sheet rearrangement"
description: "Learn how to move worksheets within Excel workbooks to reorganize sheet order and optimize workbook structure. Change worksheet positions, rearrange tabs for better workflow, and automate sheet organization for professional spreadsheet management."
weight: 100
---

Programmatically move worksheets within Excel workbooks using the Aspose.Cells Cloud API. Change sheet positions, reorder tabs, and optimize workbook structure through RESTful API calls. Perfect for automating spreadsheet organization and creating standardized workbook layouts.

## **Move worksheet from Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | **Required**. The source Excel workbook file (.xlsx, .xls, etc.) containing the worksheet to be repositioned. |
| worksheet | String | Query | **Required**. The exact name of the worksheet to move (e.g., `Summary`, `RawData_2024`). |
| position | Integer | Query | **Required**. The new zero‑based index position for the worksheet. For example, `0` moves it to the first position, `2` moves it to become the third sheet. |
| outPath | String | Query | **Optional**. The target folder path in cloud storage where the reorganized workbook will be saved. If `null` or omitted, it defaults to the source file's directory. |
| outStorageName | String | Query | **Required**. The name identifier of your configured cloud storage service (e.g., `TeamDrive`) where the output file will be stored. |
| region | String | Query | **Optional**. The locale setting (e.g., `es-MX`) to apply, which may influence certain formatting rules during the save operation. |
| password | String | Query | **Optional**. The decryption password required to open and modify a password‑protected workbook. Omit if the file is not encrypted. |

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

## Where should we use the Move Worksheet in Spreadsheet API?

- **Standardized Report Generation**: After monthly or quarterly reports are automatically generated, the `Summary` or `Executive Overview` worksheet is moved to the top of the workbook to ensure that core conclusions are presented when the file is opened.  
- **Data Processing Pipeline**: After processing raw worksheets from different data sources in the ETL process, the `Processed_Data` worksheet that has been cleaned and transformed is moved to a logical position in the workbook (e.g., in the middle), creating a clear process structure with the original data and analysis results.  
- **User‑Customized File Delivery**: After a user selects a preferred layout through a configuration interface (such as placing the chart page at the top), the system automatically rearranges the worksheet order in the workbook according to the selection and delivers the personalized file.

## Why should you use the Move Worksheet in Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development and comes with comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.  
- **Reduced Labor Costs**: Reduces the need for personnel dedicated to document consolidation.  
- **Pay‑per‑Use**: No upfront investment; you only pay for the API calls you actually use.  
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Move Worksheet in Spreadsheet API with SDKs

### Move Worksheet in Spreadsheet API Specification

The [Move Worksheet in Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) provides a publicly accessible programming interface to facilitate direct REST interactions from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to move worksheets in the spreadsheet with concise code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.  
The following code examples demonstrate how to call the Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}