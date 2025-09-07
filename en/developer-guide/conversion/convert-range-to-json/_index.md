---
title: "Aspose.Cells Cloud Web API - Convert Spreadsheet Range to JSON"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Converting Spreadsheet Range to Json"
linktitle: "Convert Range to JSON"
type: docs
url: /convert-range-to-json/
keywords: "Convert range to pdf, JSON conversion, spreadsheet to JSON, Excel API, Aspose.Cells, cloud-based conversion"
description: "Efficiently converts a specified range of a spreadsheet on a local drive to a JSON file format."
weight: 100
kwords: Convert range to pdf, JSON conversion, spreadsheet to JSON, Excel API, Aspose.Cells, cloud-based conversion
---

Convert a range from a local spreadsheet/Excel file to a json file with the Aspose.Cells Cloud Web API.

## **Convert Range to Json API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **Request Parameters:**

| Parameter Name     | Type  | Path/Query String/HTTP Body | Description                                      |
| ------------------ | ----- | ---------------------------- | ------------------------------------------------ |
| Spreadsheet        | File  | FormData                     | Upload the spreadsheet file.                     |
| worksheet          | String| Query                       | Name of the worksheet in the spreadsheet.       |
| range              | String| Query                       | Cell area to convert, e.g., A1:C10.             |
| outPath            | String| Query                       | (Optional) Folder path where the workbook is stored; default is null. |
| outStorageName     | String| Query                       | Name of the output file storage.                 |
| fontsLocation      | String| Query                       | Custom fonts usage.                              |
| region             | String| Query                       | The spreadsheet region setting.                  |
| password           | String| Query                       | Password for opening the spreadsheet file.       |

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

## Why should you use the Convert Range to Json API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Range to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToJson) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel range to json for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
