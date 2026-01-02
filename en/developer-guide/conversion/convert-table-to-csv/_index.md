---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet Table data to a CSV file."
second_title: "Document"
ArticleTitle: "Convert a Spreadsheet Table data to a CSV file."
linktitle: "Convert Table to CSV"
type: docs
url: /convert-table-to-csv/
keywords: "convert table to CSV, convert spreadsheet to CSV, Excel to CSV conversion, cloud conversion"
description: "Efficiently converts a table from a spreadsheet on your local drive to a CSV file using our API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown,Table to CSV, Local to Cloud Conversion"
---

Convert a local spreadsheet/Excel table to a CSV file.

## **Convert Table to CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Request Parameters:**

| Parameter Name   | Type  | Path/Query String/HTTP Body | Description                                     |
|-------------------|-------|------------------------------|-------------------------------------------------|
| Spreadsheet       | File  | FormData                     | Upload the spreadsheet file.                    |
| worksheet         | String| Query                        | Name of the worksheet in the spreadsheet.       |
| tableName         | String| Query                        | Name of the table to be converted.              |
| outPath           | String| Query                        | (Optional) Folder path where the workbook is stored; defaults to null. |
| outStorageName    | String| Query                        | Name of the output file storage.                |
| fontsLocation     | String| Query                        | Path for using custom fonts.                     |
| region            | String| Query                        | Defines the spreadsheet region setting.         |
| password          | String| Query                        | Password for opening the spreadsheet file.      |

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

## Why should you use the Convert Table to CSV API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Table to CSV API with SDKs?

### Convert Table to CSV API Specification

The [Convert Table to CSV API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCSV) provides a publicly accessible programming interface, allowing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a spreadsheet table data to a CSV file with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}
