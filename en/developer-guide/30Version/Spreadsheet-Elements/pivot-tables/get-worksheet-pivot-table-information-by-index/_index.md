---
title: "Get a Pivot Table in an Excel Worksheet"
second_title: "Developer Guide"
linktitle: Get
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, pivot table, Excel, REST API, get worksheet pivot table"
description: "Retrieve worksheet pivot table info by index via Aspose.Cells Cloud REST API, including cURL and SDK examples."
weight: 100
ArticleTitle: "Get a Pivot Table in an Excel Worksheet"
---
The **GetWorksheetPivotTable** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}`) retrieves detailed information about a specific PivotTable in a worksheet by its zero-based index, enabling developers to programmatically access PivotTable metadata such as cache, data fields, and layout without parsing the entire workbook; Aspose.Cells Cloud supports this operation via a RESTful endpoint and provides SDKs for multiple programming languages including .NET, Java, Go, Node.js, and Python.

## The Get Worksheet Pivot Table Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name  | Type    | Path/Query String/HTTPBody | Description                                  |
| --------------- | ------- | -------------------------- | -------------------------------------------- |
| name            | String  | Path                       | The file name.                               |
| sheetName       | String  | Path                       | The worksheet name.                          |
| pivottableIndex | Integer | Path                       | Gets the PivotTable report by index.         |
| folder          | String  | Query                      | The folder where the file is situated.       |
| storageName     | String  | Query                      | The storage name where the file is situated. |

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
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
    }
  ]
}
```

**Response Schema**

| Field                                                                            | Type   | Description                                      |
| -------------------------------------------------------------------------------- | ------ | ------------------------------------------------ |
| Status                                                                           | string | Operation status text (e.g., “OK”).              |
| PivotFilters                                                                     | array  | Collection of pivot filter definitions.          |
| └─ AutoFilter                                                                    | object | Details of automatic filtering applied to pivot. |
|     └─ link                                                                      | object | Hyperlink information for the filter.            |
|     └─ FilterColumns                                                             | array  | Individual column filter settings.               |
|     └─ Range                                                                     | string | Cell range the filter applies to.                |
|     └─ Sorter                                                                    | object | Sorting configuration for the filtered data.     |
| (additional nested fields follow the same structure as shown in the sample JSON) |

{{< /tab >}}

{{< /tabs >}}

### Response

```json
[
  {
    "Name": "PivotTableResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "PivotTableResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error handling

The API follows standard HTTP status codes. Typical responses include:

| Status Code | Meaning                                                          | Example JSON (error)                              |
| ----------- | ---------------------------------------------------------------- | ------------------------------------------------- |
| 200         | Success – the pivot table is returned                            | —                                                 |
| 401         | Unauthorized – invalid or missing token                          | `{"code":401,"message":"Invalid access token."}`  |
| 404         | Not found – file, worksheet, or pivot‑table index does not exist | `{"code":404,"message":"Pivot table not found."}` |
| 500         | Server error – unexpected condition                              | `{"code":500,"message":"Internal server error."}` |

**Notes:** The API supports Excel files up to 150 MB and works with Excel 2007‑2021 formats. Ensure the worksheet name is case‑sensitive.

## How to Use the Get Worksheet Pivot Table API with SDKs?

### Get Worksheet Pivot Table API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTable" rel="noopener noreferrer">Get Worksheet Pivot Table API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPivotTable.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPivotTable.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPivotTable.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPivotTable.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPivotTable.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPivotTable.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPivotTable.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPivotTable.go" >}}
{{</tab>}}
{{< /tabs >}}
