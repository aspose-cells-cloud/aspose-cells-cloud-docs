---
title: "Add a pivot table in an Excel worksheet"
second_title: "Developer Guide"
linktitle: Add
type: docs
url: /pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Add pivot table, Excel worksheet, Aspose.Cells Cloud, REST API, SDK, Excel pivot table"
description: "Add a pivot table to an Excel worksheet using Aspose.Cells Cloud REST API with cURL or SDKs for C#, Java, Python."
weight: 30
ArticleTitle: "How to Add a Pivot Table in an Excel Worksheet using Aspose.Cells Cloud"
---
The **PutWorksheetPivotTable** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables`) in Aspose.Cells Cloud adds a PivotTable to a specified worksheet, supporting parameters such as `sourceData`, `destCellName`, and `tableName` to define the PivotTable’s data source, position, and name; this enables programmatic creation of complex summary reports without manual Excel interaction.

## The Put Worksheet Pivot Table Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| folder | String | Query | The folder where the file is situated. |
| sourceData | String | Query | The data for the new PivotTable cache. |
| destCellName | String | Query | The cell in the upper-left corner of the destination range for the PivotTable report. |
| tableName | String | Query | The name of the new PivotTable. |
| useSameSource | Boolean | Query | Indicates whether using same data source when another existing PivotTable has used this data source. If the property is true, it will save memory. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

**Security Note:** Always use `https://` when calling the API and keep your JWT token confidential; transmitting it over plain HTTP can expose the token to interception.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Put Worksheet Pivot Table API with SDKs?

### Put Worksheet Pivot Table API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable" rel="noopener noreferrer">Put Worksheet Pivot Table API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

For more operations, see the related API pages: **[Get a pivot table](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Delete a pivot table](https://docs.aspose.cloud/cells/pivot-tables/delete/)**, and **[Update a pivot table](https://docs.aspose.cloud/cells/pivot-tables/update/)**.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetPivotTable.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetPivotTable.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetPivotTable.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetPivotTable.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetPivotTable.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetPivotTable.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetPivotTable.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetPivotTable.go" >}}
{{</tab>}}
{{< /tabs >}}
