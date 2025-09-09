---
title: "Aspose.Cells Cloud Web API - Sum, Count, Average Value, etc by color in Spreadsheet/Excel"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Sum, Count, Average Value, etc by color in Spreadsheet/Excel"
LinkTitle: "Aggregate Cells by Color"
type: docs
url: /aggregate-cells-by-color/
keywords: "Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud API"
description: "The Aspose.Cells Cloud Web API(Excel Cloud API) can perform data calculations, summation, and averaging, and can also find the maximum and minimum values in an Excel spreadsheet based on the fill or font color of the cells."
weight: 100
kwords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud API
---

The API can perform data calculations, summation, and averaging, and can also find the maximum and minimum values in an Excel spreadsheet based on the fill or font color of the cells.

| Calculate Operation | Description |
| :- | :- |
| Count | Determine the number of cells with the same color. |
| Sum | Calculate the total value of cells with the same color. |
| Max Value | Identify the highest value among cells with the same color. |
| Min Value | Find the lowest value among cells with the same color. |
| Average Value | Compute the mean value of cells with the same color. |

## **Aggregating Cells by Color API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| Worksheet | String | Query | Specifies the worksheet. |
| Range | String | Query | Specifies the range. |
| Operation | String | Query | Specify calculation operation methods, including Sum, Count, Average, Min, and Max. |
| ColorPosition | String | Query | Indicates the content to sum and count based on background color and/or font color. |
| Region | String | Query | The spreadsheet region setting. |
| Password | String | Query | The password for opening the spreadsheet file. |

### **Response**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Aggregate by Color API?

In a spreadsheet, data from different categories is displayed in different colors, allowing operations such as summing, counting, calculating averages, and finding maximum and minimum values based on color.

## Why should you use the Aggregate by Color API?

- Provide methods for color data analysis.
- Classify and calculate data based on color to provide foundational data for data analysis.
- Development can be quickly completed through the existing SDK.

## How to Use the Aggregate by Color API with SDKs

### Aggregate by Color API Specification

The [Aggregate by Color API Specification](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to aggregate calculations by cell color with just a short piece of code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}
