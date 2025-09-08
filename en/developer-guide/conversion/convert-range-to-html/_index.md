---
title: "Aspose.Cells Cloud Web API - Converting Spreadsheet Range to HTML"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Converting Spreadsheet Range to Html"
linktitle: "Convert Range to HTML"
type: docs
url: /convert-range-to-html/
keywords: "Convert range to html, Spreadsheet, Excel"
description: "Convert a range from a local spreadsheet/Excel file to an html file with the Aspose.Cells Cloud Web API."
weight: 100
kwords: "Convert range to html, Spreadsheet, Excel"
---

Convert a range from a local spreadsheet/Excel file to a html file with the Aspose.Cells Cloud Web API.

## **Convert Range to Html API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **Request Parameters:**

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description                                           |
|------------------|--------|------------------------------|-------------------------------------------------------|
| Spreadsheet      | File   | FormData                     | Upload the spreadsheet file.                          |
| worksheet        | String | Query                        | Name of the worksheet within the spreadsheet.        |
| range            | String | Query                        | The cell area to convert, e.g., A1:C10.              |
| outPath          | String | Query                        | (Optional) The folder path where the workbook is stored. Default is null. |
| outStorageName   | String | Query                        | Name of the output file storage.                      |
| fontsLocation     | String | Query                        | Specify custom fonts to use.                          |
| region           | String | Query                        | The spreadsheet region setting.                        |
| password         | String | Query                        | Password for opening the spreadsheet file.            |

### **Response Structure**

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

## Why should you use the Convert Range to Html API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Range to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) provides a publicly accessible programming interface, enabling you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel range to html for cells with minimal code.
Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
