---
title: "Working with pivot filters"
second_title: "Document"
linktitle: Filters
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Pivot filters, Aspose.Cells Cloud, REST API, Excel, Pivot table, Add filter"
description: "Learn how to add and manage pivot table filters using the Aspose.Cells Cloud REST API. Includes request syntax, parameter details, cURL example, and SDK code snippets for multiple programming languages."
weight: 50
---

This REST API adds a **pivot filter** for a specified pivot table index.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### Request parameters

| Parameter Name   | Type    | Location                     | Description                                                                                     |
|------------------|---------|------------------------------|-------------------------------------------------------------------------------------------------|
| **name**         | string  | path                         | The name of the Excel file.                                                                      |
| **sheetName**    | string  | path                         | The worksheet that contains the pivot table.                                                    |
| **pivotTableIndex** | integer | path                     | Zero‑based index of the pivot table to which the filter will be applied.                       |
| **filter**       | object  | body                         | JSON object that defines the filter settings (e.g., `AutoFilter`, `EvaluationOrder`, etc.).    |
| **needReCalculate** | boolean | query                     | When **true**, forces the workbook to recalculate after the filter is added. Default **false**. |
| **folder**       | string  | query                        | Folder in cloud storage where the file is located.                                               |
| **storageName**  | string  | query                        | Name of the cloud storage.                                                                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

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
public void Run_PivotTable_PivotFilter()
{
    url = @"http://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }";   // Truncated for brevity
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";
    data = "{\"AutoFilter\":null,\"EvaluationOrder\":null,\"FieldIndex\":1,\"FilterType\":\"Count\",\"MeasureFldIndex\":null,\"MemberPropertyFieldIndex\":null,\"Name\":null,\"Value1\":null,\"Value2\":null}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Retrieve a specific filter
    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters/0?folder=Temp";
    using (HttpWebResponse response = _helper.CallGet(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Retrieve all filters
    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";
    using (HttpWebResponse response = _helper.CallGet(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Delete a specific filter
    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters/0?folder=Temp";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Delete all filters
    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}