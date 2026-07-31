---
title: "Aspose.Cells Cloud Web API – Sum and Count by Color in Excel"
second_title: "Document"
ArticleTitle: "Sum, Count, Average, Max, Min Values by Color in Spreadsheet/Excel"
LinkTitle: "Aggregate Cells by Color"
type: docs
url: /aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "Aggregate Excel cells by background or font color (sum, count, average, min, max) using Aspose.Cells Cloud API. Learn the endpoint, parameters, authentication, and SDK examples."
weight: 100
---

## Overview

The API can perform data calculations based on cell **color**. It can sum, count, average, and also find the maximum and minimum values in an Excel spreadsheet according to the fill or font color of the cells.

| Calculate Operation | Description                                                  |
| :------------------ | :----------------------------------------------------------- |
| Count               | Determine the number of cells with the same colour.          |
| Sum                 | Calculate the total value of cells with the same colour.     |
| Max Value           | Identify the highest value among cells with the same colour. |
| Min Value           | Find the lowest value among cells with the same colour.      |
| Average Value       | Compute the mean value of cells with the same colour.        |

## Authentication

**Prerequisites** – Ensure you have a registered Aspose Cloud application and that you are using a supported SDK version for your platform (e.g., .NET 6+, Java 11+, Python 3.8+). The API requires an OAuth 2.0 access token.

1. **Register an application** in the Aspose Cloud Dashboard to receive a **Client Id** and **Client Secret**.
2. **Request a token**

   ```http
   POST https://api.aspose.cloud/connect/token
   Content-Type: application/x-www-form-urlencoded

   grant_type=client_credentials&client_id=<YOUR_CLIENT_ID>&client_secret=<YOUR_CLIENT_SECRET>
   ```

   The response contains an `access_token`.

3. **Include the token** in every API request

   ```http
   Authorization: Bearer <access_token>
   ```

The token is valid for one hour; refresh it by repeating step 2.

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### Request Parameters

| Parameter Name | Type   | Location | Description                                                      |
| :------------- | :----- | :------- | :--------------------------------------------------------------- |
| Spreadsheet    | File   | FormData | The Excel workbook to process.                                   |
| Worksheet      | String | Query    | Name of the worksheet that contains the range.                   |
| Range          | String | Query    | A‑1 style range (e.g., `A1:B10`).                                |
| Operation      | String | Query    | Calculation method – `Sum`, `Count`, `Average`, `Min`, or `Max`. |
| ColorPosition  | String | Query    | Determines which colour to evaluate – `Background`, `Font`.      |
| Region         | String | Query    | The spreadsheet region setting (e.g., `us-east-1`).              |
| Password       | String | Query    | Password for opening a protected workbook (optional).            |

#### Enumerations

- **ColorPosition**

  | Value      | Meaning                     |
  | :--------- | :-------------------------- |
  | Background | Use the cell’s fill colour. |
  | Font       | Use the cell’s font colour. |

**Example multipart/form‑data request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Response

The schema below describes the response object. A concrete example follows the schema.

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
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Example response (real‑world values)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

### Error Codes

- **200 OK** – Successful aggregation operation returns the `AggregateResults` payload.  
- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid or missing access token, or incorrect client credentials.  
- **404 Not Found** – The specified spreadsheet cannot be accessed.  
- **500 Server Error** – The service encountered an unexpected condition while processing the request.

## Where should we use the Aggregate by Color API?

In a spreadsheet, data from different categories is often color‑coded. This API enables you to sum, count, average, or find the minimum and maximum values for each color group, simplifying color‑based data analysis.

## Why should you use the Aggregate by Color API?

The API provides a fast, reliable way to perform color‑based calculations without writing custom parsing logic. It integrates seamlessly with Aspose.Cells Cloud SDKs, allowing developers to implement color aggregation with just a few lines of code.

## How to Use the Aggregate by Color API with SDKs

### Aggregate by Color API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">Aggregate by Color API Specification</a> defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to aggregate calculations by cell color with just a short piece of code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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

**Notes:**  
- When working with protected workbooks, include the optional `Password` query parameter; otherwise the request will fail with a 401 error.  
- The maximum request size for the `Spreadsheet` file is 100 MB. If you need to process larger files, consider uploading the workbook to Aspose Cloud storage first and referencing it via the `Path` parameter (not shown here).