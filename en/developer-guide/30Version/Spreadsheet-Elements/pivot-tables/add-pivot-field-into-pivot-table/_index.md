---
title: "Add a Pivot Field to a Pivot Table"
second_title: "Developer Guide"
linktitle: "Add Pivot Field"
type: docs
url: /pivot-tables/add-pivot-field/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, pivot table, add pivot field, REST API, SDK"
description: "Add a pivot field to an existing pivot table via Aspose.Cells Cloud REST API, including cURL and SDK examples."
weight: 40
ArticleTitle: "Add a Pivot Field to a Pivot Table – Aspose.Cells Cloud Documentation"
---
The **PutPivotTableField** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField`) adds a pivot field to an existing pivot table in Aspose.Cells Cloud, supporting row, column, data, or filter field types via the required `pivotFieldType` query parameter and `pivotTableFieldRequest` body. This operation enables developers to programmatically extend pivot table structure without manual reconfiguration, leveraging Aspose.Cells Cloud’s REST API to automate complex spreadsheet analysis workflows across supported SDKs for .NET, Java, Python, and other languages.

## The Put Pivot Table Field Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request parameters

| Parameter Name         | Type                         | Path/Query String/HTTPBody | Description                                            |
| ---------------------- | ---------------------------- | -------------------------- | ------------------------------------------------------ |
| name                   | String                       | Path                       | The file name.                                         |
| sheetName              | String                       | Path                       | The worksheet name.                                    |
| pivotTableIndex        | Integer                      | Path                       | The PivotTable index.                                  |
| pivotFieldType         | String                       | Query                      | The fields area type.                                  |
| pivotTableFieldRequest | class:pivottablefieldrequest | HTTPBody                   | PivotTableFieldRequest The PivotTable field request.   |
| needReCalculate        | Boolean                      | Query                      | Whether the specific PivotTable calculate(true/false). |
| folder                 | String                       | Query                      | The folder where the file is situated.                 |
| storageName            | String                       | Query                      | The storage name where the file is situated.           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The example below demonstrates how to add a pivot field using cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

The successful response returns a JSON object with `Code` and `Status` fields. Example schema:

```json
{
  "Code": 0, // integer indicating the HTTP status code
  "Status": "OK" // string message
}
```

Possible error responses include **400 Bad Request** for missing parameters, **401 Unauthorized** if the token is invalid, and **500 Internal Server Error** for server‑side issues.

### **Response**

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

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Put Pivot Table Field API with SDKs?

### Put Pivot Table Field API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/PutPivotTableField" rel="noopener noreferrer">Put Pivot Table Field API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**See also:**

- [Add a Pivot Table](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)
- [Delete Pivot Field](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutPivotTableField.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutPivotTableField.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutPivotTableField.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutPivotTableField.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutPivotTableField.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutPivotTableField.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutPivotTableField.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutPivotTableField.go" >}}
{{</tab>}}
{{< /tabs >}}
