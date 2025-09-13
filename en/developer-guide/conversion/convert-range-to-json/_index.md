---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet Range data to a Json file."
second_title: "Aspose.Cells Cloud Document"
ArticleTitle: "Convert a Spreadsheet Range data to a Json file."
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

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Why should you use the Convert Range to Json API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Range to Json API with SDKs?

### Convert Range to Json API Specification

The [Convert Range to Json API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToJson) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a range data to a json file with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}
