---
title: "Aspose.Cells Cloud Web API - Converting Spreadsheet Range to HTML"
second_title: "Aspose.Cells Cloud Document"
ArticleTitle: "Converting Spreadsheet Range to Html"
linktitle: "Convert Range to HTML"
type: docs
url: /convert-range-to-html/
keywords: "Convert a spreadsheet range data to a html file, Spreadsheet Conversion, Excel Conversion"
description: "Convert a range from a local spreadsheet/Excel file to an html file with the Aspose.Cells Cloud Web API."
weight: 100
kwords: "Convert range to html, Spreadsheet, Excel"
---

Convert a range data from a local spreadsheet/Excel file to a html file.

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

## Why should you use the Convert Range to Html API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Range to Html API with SDKs?

### Convert Range to Html API Specification

The [Convert Range to Html API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) provides a publicly accessible programming interface, enabling you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a range data to a html file with short code.
Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}
