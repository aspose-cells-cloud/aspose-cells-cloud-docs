---
title: "Working with Pivot Filters"
second_title: "Document"
linktitle: Filters
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells, Pivot Table, Filter, REST API, Cloud"
description: "Learn how to add, retrieve, and delete pivot table filters using the Aspose.Cells Cloud REST API. Includes request syntax, required parameters, cURL example, and SDK snippets for C# and Go."
weight: 50
ArticleTitle: "Working with Pivot Filters – Aspose.Cells Cloud Documentation"
---

This REST API adds a **pivot filter** to the pivot table at the specified index.

**Prerequisites**  
Before calling this endpoint you must:

- Generate a valid OAuth/JWT access token and include it in the `Authorization` header.  
- Ensure the target workbook is stored in a cloud folder that you have access to (specify `folder` and optionally `storageName`).  
- Use Aspose.Cells Cloud API version 3.0 or later.

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name      | Type    | Location | Description                                                                                     |
| ------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------- |
| **name**            | string  | path     | The name of the Excel file.                                                                     |
| **sheetName**       | string  | path     | The worksheet that contains the pivot table.                                                    |
| **pivotTableIndex** | integer | path     | Zero‑based index of the pivot table to which the filter will be applied.                        |
| **filter**          | object  | body     | JSON object that defines the filter settings. See the **filter schema** table below.            |
| **needReCalculate** | boolean | query    | When **true**, forces the workbook to recalculate after the filter is added. Default **false**. |
| **folder**          | string  | query    | Folder in cloud storage where the file is located.                                              |
| **storageName**     | string  | query     | Name of the cloud storage.                                                                      |

**filter schema**

| Property                     | Type    | Description                                                                                 |
| ---------------------------- | ------- | ------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Settings for an AutoFilter; can be omitted if not used.                                    |
| **EvaluationOrder**          | integer | Order in which the filter is evaluated.                                                     |
| **FieldIndex**               | integer | Zero‑based index of the field to which the filter applies.                                 |
| **FilterType**               | string  | Type of filter (e.g., `Value`, `Count`, `Label`).                                          |
| **MeasureFldIndex**          | integer | Index of the measure field, if applicable.                                                  |
| **MemberPropertyFieldIndex** | integer | Index of the member property field, if applicable.                                         |
| **Name**                     | string  | Optional name for the filter.                                                               |
| **Value1**                   | string  | First value used by the filter (e.g., lower bound for a range).                            |
| **Value2**                   | string  | Second value used by the filter (e.g., upper bound for a range).                           |
| **CustomFilters**            | array   | Collection of custom filter objects (each with `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Settings for a dynamic filter (e.g., Top10, Bottom10).                                      |
| **IconFilter**               | object  | Settings for an icon‑based filter.                                                          |
| **Top10Filter**              | object  | Settings for a Top10/Bottom10 filter.                                                       |
| **ColorFilter**              | object  | Settings for a color‑based filter.                                                          |
| **Visibledropdown**          | boolean | Indicates whether the filter dropdown is visible.                                          |

> **Note:** All parameters listed above are required unless explicitly marked as optional in the API reference.

### Response codes

| Code | Meaning                                      |
| ---- | -------------------------------------------- |
| 200  | Filter added successfully.                  |
| 400  | Bad request – invalid parameters.            |
| 401  | Unauthorized – missing or invalid token.     |
| 404  | Not found – workbook or pivot table missing. |
| 500  | Internal server error.                       |

**Best Practices**  
- Keep filter objects as small as possible; large filter definitions may increase request latency.  
- Calls are idempotent — adding the same filter twice will not create duplicates.  
- Respect the API rate‑limit of 100 requests per minute per account.  

*Additional notes:*  
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