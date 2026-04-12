---
title: "Working with Pivot Filters"
second_title: "Document"
linktitle: Filters
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells Cloud, pivot filter, REST API, Excel, add filter, pivot table"
description: "Learn how to add, retrieve, and delete pivot table filters using the Aspose.Cells Cloud REST API. Includes request syntax, required parameters, cURL example, and SDK snippets for C# and Go."
weight: 50
---

This REST API adds a **pivot filter** to the pivot table at the specified index.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### Request parameters

| Parameter Name      | Type    | Location | Description                                                                                     |
| ------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------- |
| **name**            | string  | path     | The name of the Excel file.                                                                     |
| **sheetName**       | string  | path     | The worksheet that contains the pivot table.                                                    |
| **pivotTableIndex** | integer | path     | Zero‑based index of the pivot table to which the filter will be applied.                        |
| **filter**          | object  | body     | JSON object that defines the filter settings (e.g., `AutoFilter`, `EvaluationOrder`, etc.).     |
| **needReCalculate** | boolean | query    | When **true**, forces the workbook to recalculate after the filter is added. Default **false**. |
| **folder**          | string  | query    | Folder in cloud storage where the file is located.                                              |
| **storageName**     | string  | query    | Name of the cloud storage.                                                                      |

> **Note:** All parameters listed above are required unless explicitly marked as optional in the API reference.

### Response codes

| Code | Meaning                                      |
| ---- | -------------------------------------------- |
| 200  | Filter added successfully.                   |
| 400  | Bad request – invalid parameters.            |
| 401  | Unauthorized – missing or invalid token.     |
| 404  | Not found – workbook or pivot table missing. |
| 500  | Internal server error.                       |

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
          "link": { "Href": "string", "Rel": "string", "Title": "string", "Type": "string" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "string",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ {} ]
              },
              "ColorFilter": {
                "FilterByFillColor": "string",
                "Pattern": "string",
                "Color": {
                  "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
                  "ColorIndex": 0,
                  "IsShapeColor": true,
                  "ThemeColor": { "ColorType": "string", "Tint": 0 },
                  "Type": "string"
                },
                "ForegroundColorColor": {
                  "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
                  "ColorIndex": 0,
                  "IsShapeColor": true,
                  "ThemeColor": { "ColorType": "string", "Tint": 0 },
                  "Type": "string"
                },
                "BackgroundColor": {
                  "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
                  "ColorIndex": 0,
                  "IsShapeColor": true,
                  "ThemeColor": { "ColorType": "string", "Tint": 0 },
                  "Type": "string"
                }
              },
              "CustomFilters": [ { "FilterOperatorType": "string" } ],
              "DynamicFilter": { "DynamicFilterType": "string" },
              "IconFilter": { "IconId": 0, "IconSetType": "string" },
              "Top10Filter": { "Criteria": "string", "IsPercent": true, "IsTop": true, "Items": 0 },
              "Visibledropdown": "string"
            }
          ],
          "Range": "string",
          "Sorter": {
            "CaseSensitive": true,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "string", "CustomList": "string" } ],
            "SortLeftToRight": true
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "string",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "string",
        "Value1": "string",
        "Value2": "string"
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
