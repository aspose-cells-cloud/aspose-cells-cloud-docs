---
title: "Aspose.Cells Cloud Web API - Converting Spreadsheet Range to CSV"
second_title: "Aspose.Cells Cloud"
ArticleTitle: Converting Spreadsheet Range to CSV
linktitle: "Convert Range to CSV"
type: docs
url: /convert-range-to-csv/
keywords: "Convert range to csv, convert spreadsheet to csv, Aspose API, cloud conversion, Excel to csv"
description: "Convert a specified range from a local spreadsheet file to a CSV format using the Excel API, ensuring seamless cloud execution."
weight: 100
kwords: range to csv, convert spreadsheet to csv, Aspose API, cloud conversion, Excel to csv
---

Convert a range from a local spreadsheet/Excel file to a [CSV](https://docs.fileformat.com/spreadsheet/csv/) file with the Aspose.Cells Cloud Web API.

## **Convert Range to CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|worksheet|String|Query|The worksheet name of Spreadsheet/Excel|
|range|String|Query|Specify the cell area (e.g., A1:C10).|
|outPath|String|Query|(Optional) The folder path where the workbook will be stored. Default is null.|
|outStorageName|String|Query|Name of the output file storage.|
|fontsLocation|String|Query|Specify custom fonts if required.|
|region|String|Query|Defines the spreadsheet region setting.|
|password|String|Query|Password required to open the spreadsheet file.|

## **Response Structure**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Why should you use the Convert Chart to Pdf API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Chart to Pdf API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) outlines a publicly accessible API, enabling REST interactions directly from a web browser.

## Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel range to csv for cells with minimal code.
Explore the complete list of Aspose.Cells Cloud SDKs in our [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:
