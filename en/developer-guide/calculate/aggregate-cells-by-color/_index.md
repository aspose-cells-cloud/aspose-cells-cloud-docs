---
title: "Aggregate Cells by Color - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Aggregate Cells by Color"
type: docs
url: /aggregate-cells-by-color/
keywords: "Excel API, Aggregate Cells, Color-based Calculation, Data Analysis, REST API, Spreadsheet Operations, Aspose.Cells"
description: "The Aggregate by Color API enables efficient calculations on cells with matching fill or font colors in Excel spreadsheets. Support for aggregate operations like count, sum, max, min, and average allows for effective data analysis based on color distinctions."
weight: 100
kwords: Excel API, Aggregate by Color, Data Analysis, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Color-based Aggregation
---

# **Excel API: Aggregate Cells by Color**

## **Overview**

The Aggregate by Color API enables efficient calculations on cells with matching fill or font colors in Excel spreadsheets. This API supports various aggregate operations, including count, sum, maximum, minimum, and average, allowing for effective data analysis based on color distinctions.

## **Function Description**

The Aggregate by Color API is a powerful tool for data analysis, allowing you to perform color-based aggregations efficiently. Whether you need to count, sum, find the maximum or minimum value, or calculate the average, this API provides the flexibility to handle various aggregate operations based on cell colors.

- **Color-Based Aggregation**: Perform calculations on cells grouped by their fill or font color.
- **Aggregate Operations**:
  - **Count**: Determine the number of cells with the same color.
  - **Sum**: Calculate the total value of cells with the same color.
  - **Max Value**: Identify the highest value among cells with the same color.
  - **Min Value**: Find the lowest value among cells with the same color.
  - **Average Value**: Compute the mean value of cells with the same color.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

## **Request Parameters of the `aggregateCellsByColor` API:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| Worksheet | String | Query | Specifies the worksheet. |
| Range | String | Query | Specifies the range. |
| Operation | String | Query | Specify calculation operation methods, including Sum, Count, Average, Min, and Max. |
| ColorPosition | String | Query | Indicates the content to sum and count based on background color and/or font color. |
| Region | String | Query | The spreadsheet region setting. |
| Password | String | Query | The password for opening the spreadsheet file. |

## **Response Structure**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "AggregateResultByColor",
          "Name": "class:aggregateresultbycolor"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Code",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "Integer",
        "Name": "integer"
      }
    },
    {
      "Name": "Status",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Usage Scenarios

Suppose you have a spreadsheet where different categories of data are highlighted with different colors. You can use the Aggregate by Color API to quickly summarize the data for each color category. For instance, you can calculate the total sales for cells highlighted in green or the average cost for cells highlighted in red.

## Key Features and Benefits

- **Simplified Data Analysis**: Eliminates manual sorting or filtering of color-coded cells, reducing tedious manual operations and saving time.
- **Clear Color-Driven Insights**: Enables users to quickly summarize and understand data rules based on color distinctions (e.g., identifying the total sales value of cells marked with a specific fill color).
- **Strong Flexibility**: Adapts to multiple common analysis scenarios (quantity statistics, value summation, extremum search, average calculation) through its diversified aggregate operations, eliminating the need for additional custom development.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low-level details and allows you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
