---
title: "Working with Pivot Filters"
second_title: "Developer Guide"
linktitle: Filters
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells, Pivot Table, Filter, REST API, Cloud"
description: "Add pivot table filters to Excel workbooks via Aspose.Cells Cloud REST API with cURL and SDK examples."
weight: 50
ArticleTitle: "Working with Pivot Filters – Aspose.Cells Cloud Documentation"
---
The **PutWorksheetPivotTableFilter** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters`) adds a pivot filter to the specified PivotTable in a worksheet using Aspose.Cells Cloud, enabling developers to programmatically apply filtering criteria to pivot table data without manual intervention.

## The Put Worksheet Pivot Table Filter Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| pivotTableIndex | Integer | Path | Gets the PivotTable report by index. |
| filter | class:pivotfilter | HTTPBody | PivotFilter Pivot filter description. |
| needReCalculate | Boolean | Query | Whether the specific PivotTable calculate(true/false). |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**filter schema**

| Property                     | Type    | Description                                                                               |
| ---------------------------- | ------- | ----------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Settings for an AutoFilter; can be omitted if not used.                                   |
| **EvaluationOrder**          | integer | Order in which the filter is evaluated.                                                   |
| **FieldIndex**               | integer | Zero‑based index of the field to which the filter applies.                                |
| **FilterType**               | string  | Type of filter (e.g., `Value`, `Count`, `Label`).                                         |
| **MeasureFldIndex**          | integer | Index of the measure field, if applicable.                                                |
| **MemberPropertyFieldIndex** | integer | Index of the member property field, if applicable.                                        |
| **Name**                     | string  | Optional name for the filter.                                                             |
| **Value1**                   | string  | First value used by the filter (e.g., lower bound for a range).                           |
| **Value2**                   | string  | Second value used by the filter (e.g., upper bound for a range).                          |
| **CustomFilters**            | array   | Collection of custom filter objects (each with `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Settings for a dynamic filter (e.g., Top10, Bottom10).                                    |
| **IconFilter**               | object  | Settings for an icon‑based filter.                                                        |
| **Top10Filter**              | object  | Settings for a Top10/Bottom10 filter.                                                     |
| **ColorFilter**              | object  | Settings for a color‑based filter.                                                        |
| **Visibledropdown**          | boolean | Indicates whether the filter dropdown is visible.                                         |

> **Note:** All parameters listed above are required unless explicitly marked as optional in the API reference.

### Response codes

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
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Best Practices**

- Keep filter objects as small as possible; large filter definitions may increase request latency.
- Calls are idempotent — adding the same filter twice will not create duplicates.
- Respect the API rate‑limit of 100 requests per minute per account.

_Additional notes:_

- The maximum size of a filter definition is 1 MB; larger payloads will be rejected with a 400 error.
- When using `needReCalculate=true`, the recalculation may increase response time for large workbooks.

You can explore the full OpenAPI definition here:  
[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Example cURL request

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
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

## Cloud SDK Family

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. SDKs handle low‑level details, letting you focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Initialise the API client (replace with your credentials)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // Build the filter object
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Prepare the request
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Execute the request
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

For additional operations related to pivot tables, see the **Add**, **Delete**, and **Clear** filter documentation.
