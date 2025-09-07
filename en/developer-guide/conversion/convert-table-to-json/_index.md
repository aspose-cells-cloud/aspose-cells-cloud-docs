---
title: "Aspose.Cells Cloud Web API - Convert Spreadsheet Table to JSON"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Convert Spreadsheet Table to Json"
linktitle: "Convert Table to JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cells"
description: "Convert a local spreadsheet table to JSON format efficiently using the Excel API. This method enables seamless file processing without the need for cloud storage."
weight: 100
kwords: "Excel API, JSON conversion, cloud file conversion, spreadsheet, REST API, Aspose.Cells, local drive processing, file format conversion"
---

Convert a local spreadsheet/Excel table to a json file with the Aspose.Cells Cloud Web API.

## **Convert Table to Json API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Request Parameters:**

| Parameter Name    | Type  | Path/Query String/HTTP Body | Description                                        |
|-------------------|-------|-----------------------------|----------------------------------------------------|
| Spreadsheet       | File  | FormData                    | Upload the spreadsheet file.                       |
| worksheet         | String| Query                       | Specify the worksheet name of the spreadsheet.     |
| tableName         | String| Query                       | Provide the name of the table to convert.          |
| outPath           | String| Query                       | (Optional) The folder path where the workbook is stored; defaults to null. |
| outStorageName    | String| Query                       | Specify the output file storage name.              |
| fontsLocation     | String| Query                       | Use custom fonts for conversion.                   |
| region            | String| Query                       | Define the region settings for the spreadsheet.    |
| password          | String| Query                       | The password required to open the spreadsheet file. |

## **Response**

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

## Why should you use the Convert Table to Json API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Table to Json API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel table to a json file for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:
