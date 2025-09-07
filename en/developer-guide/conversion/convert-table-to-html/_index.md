---
title: "Aspose.Cells Cloud Web API - Convert Spreadsheet Table to HTML"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Convert Spreadsheet Table to HTML"
linktitle: "Convert Table to HTML"
type: docs
url: /convert-table-to-html/
keywords: "Excel Table to HTML, Spreadsheet Conversion, HTML Generation, Cloud API, REST API, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Services"
description: "Easily convert tables from local spreadsheet files into HTML format using our cloud-based API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, HTML, PDF, CSV, JSON, Markdown, Match blank cells in Excel"
---

Convert a local spreadsheet/Excel table to a html file with the Aspose.Cells Cloud Web API.

## **Convert Table to Html API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | Upload the spreadsheet file to be converted. |
| worksheet | String | Query | The worksheet name of Spreadsheet/Excel |
| tableName | String | Query | The name of the table to convert. |
| outPath | String | Query | (Optional) The folder path where the converted file will be stored. The default value is null. |
| outStorageName | String | Query | The designated storage name for the output file. |
| fontsLocation | String | Query | Specify custom fonts for the conversion. |
| region | String | Query | Define the spreadsheet region settings. |
| password | String | Query | The password required to access the spreadsheet file. |

### **Response**

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

## Why should you use the Convert Table to Pdf API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Table to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) outlines a publicly accessible programming interface, allowing you to perform REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel table to html for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
