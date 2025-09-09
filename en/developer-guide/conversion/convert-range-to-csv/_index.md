---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet Range data to a CSV file."
second_title: "Aspose.Cells Cloud"
ArticleTitle: Convert a Spreadsheet Range data to a CSV file.
linktitle: "Convert Range to CSV"
type: docs
url: /convert-range-to-csv/
keywords: "Convert range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to csv"
description: "Convert a specified range from a local spreadsheet file to a CSV format using the Excel API, ensuring seamless cloud execution."
weight: 100
kwords: range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to csv
---

Convert a range data from a local spreadsheet/Excel file to a [CSV](https://docs.fileformat.com/spreadsheet/csv/) file.

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

### **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream",
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Why should you use the Convert Chart to Csv API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Chart to Csv API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) outlines a publicly accessible API, enabling REST interactions directly from a web browser.

## Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a range data to a csv file with short code.
Explore the complete list of Aspose.Cells Cloud SDKs in our [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}
