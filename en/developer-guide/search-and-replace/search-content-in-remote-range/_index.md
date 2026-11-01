---
title: "Search Text in Remote Excel Ranges – Aspose.Cells Cloud API"
description: "Search Excel data in remote ranges using Aspose.Cells Cloud REST API with cURL and SDK examples."
linktitle: "Search Content in Remote Range"
type: docs
url: /search-content-in-remote-range/
keywords: "Aspose.Cells Cloud, Excel REST API, text search, remote range search, spreadsheet automation, cloud data extraction, RESTful API, cURL example, range query, cell search"
weight: 100
ArticleTitle: "Search Excel Range Content in Aspose.Cells Cloud API"
---
The **SearchContentInRemoteRange** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content`) enables programmatic text, number, or formula search within a specified range of an Excel workbook stored in Aspose.Cells Cloud, supporting remote, cloud-based processing without downloading the file—ideal for automated data discovery, content analysis, and spreadsheet auditing workflows.

## API Overview

Programmatically search for specific text, numbers, or formulas in a defined range of an Excel workbook stored in Aspose Cloud. This RESTful API enables automated data discovery, content analysis, and spreadsheet auditing workflows—without downloading the file.

---

## The Search Content in Remote Range Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### Authentication

All requests require a valid JWT access token. Follow the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) to obtain your `client_id` and `client_secret`.

```bash
-H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

> **Note**: Replace `YOUR_ACCESS_TOKEN` with your actual JWT token. For security, never expose credentials in client-side code.

---

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | Specify the search workbook file name. |
| worksheet | String | Path | Specify the search worksheet name. |
| cellArea | String | Path | Specify the search cell area. |
| searchText | String | Query | Specify the search content. |
| ignoringCase | Boolean | Query | Ignore the text of the search. |
| folder | String | Query | The folder path where the workbook is stored. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

> **Prerequisites**: Ensure your workbook is uploaded to Aspose Cloud storage. Obtain API credentials from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

---

### Response

```json
[
  {
    "Name": "SearchResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "SearchResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Responses

| Status Code        | Description                                                               |
| :----------------- | :------------------------------------------------------------------------ |
| `400 Bad Request`  | Invalid URL, malformed parameters, or unsupported file format.            |
| `401 Unauthorized` | Missing, expired, or invalid JWT token.                                   |
| `404 Not Found`    | Workbook, worksheet, or range does not exist or is inaccessible.          |
| `500 Server Error` | Internal failure during search (e.g., corrupted file, permissions issue). |

---

### Example: cURL Request

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoringCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

---

### Success (200 OK)

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "MyWorkbook.xlsx",
      "Worksheet": "Orders_2024",
      "Position": "C5",
      "Content": "Report Q1"
    },
    {
      "Filename": "MyWorkbook.xlsx",
      "Worksheet": "Orders_2024",
      "Position": "F12",
      "Content": "End-of-report summary"
    }
  ]
}
```

## Practical Use Cases

| Use Case                    | Range                     | Search Term                              | Benefit                                               |
| :-------------------------- | :------------------------ | :--------------------------------------- | :---------------------------------------------------- |
| **Data Quality Validation** | `DataDictionary!B2:F1000` | `"TBD"`, `"NULL"`, `"N/A"`               | Detect missing definitions in ETL pipelines.          |
| **KPI Extraction**          | `Monthly_Metrics!C10:G50` | `"[KPI]"`                                | Automate report assembly from template files.         |
| **Legal Clause Review**     | `Contract_Terms!A:A`      | `"liability limit"`, `"indemnification"` | Accelerate contract analysis across large appendices. |

---

## Why Use This API?

- **Developer-Friendly**: SDKs for C#, Java, PHP, Python, Node.js, Ruby, Perl, and Go.
- **Cost-Efficient**: Pay per API call—no infrastructure or maintenance overhead.
- **Secure & Scalable**: Cloud-native processing ensures high availability and data protection.
- **Time-Saving**: Eliminate manual review and reduce labor-intensive data auditing.

---

## Using SDKs

The SDKs handle authentication, serialization, and error handling—letting you focus on business logic. View full examples on [GitHub](https://github.com/aspose-cells-cloud).

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
// See full C# example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/blob/master/Examples/Cells/SearchTextInRemoteRangeExample.cs
var cellsApi = new CellsApi(clientId, clientSecret);
var result = cellsApi.CellsSearchContentInRemoteRange(
    fileName: "MyWorkbook.xlsx",
    worksheetName: "Orders_2024",
    cellArea: "B2:H100",
    searchText: "Report",
    ignoringCase: true,
    folder: "Imports",
    storageName: null
);
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
// See full Java example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/Cells/SearchTextInRemoteRangeExample.java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
SearchResponse result = cellsApi.cellsSearchContentInRemoteRange(
    "MyWorkbook.xlsx",
    "Orders_2024",
    "B2:H100",
    "Report",
    true,
    "Imports",
    null,
    null,
    null
);
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
// See full PHP example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/Examples/Cells/SearchTextInRemoteRangeExample.php
$cellsApi = new CellsApi($clientId, $clientSecret);
$result = $cellsApi->cellsSearchContentInRemoteRange(
    "MyWorkbook.xlsx",
    "Orders_2024",
    "B2:H100",
    "Report",
    true,
    "Imports"
);
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
# See full Ruby example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/examples/search_text_in_remote_range.rb
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
result = cells_api.cells_search_content_in_remote_range(
  "MyWorkbook.xlsx",
  "Orders_2024",
  "B2:H100",
  "Report",
  ignoring_case: true,
  folder: "Imports"
)
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
// See full Node.js/TypeScript example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/blob/master/examples/cells/search-text-in-remote-range.ts
const cellsApi = new CellsApi(clientId, clientSecret);
const result = await cellsApi.cellsSearchContentInRemoteRange(
  "MyWorkbook.xlsx",
  "Orders_2024",
  "B2:H100",
  "Report",
  true,
  "Imports",
);
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
# See full Python example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/blob/master/examples/cells/search_text_in_remote_range.py
cells_api = CellsApi(client_id, client_secret)
result = cells_api.cells_search_content_in_remote_range(
    'MyWorkbook.xlsx',
    'Orders_2024',
    'B2:H100',
    'Report',
    ignoring_case=True,
    folder='Imports'
)
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
# See full Perl example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/examples/cells/search_text_in_remote_range.pl
my $cells_api = AsposeCellsCloud::CellsApi->new(
    -clientId => $client_id,
    -clientSecret => $client_secret
);
my $result = $cells_api->cells_search_content_in_remote_range(
    'MyWorkbook.xlsx',
    'Orders_2024',
    'B2:H100',
    'Report',
    ignoringCase => 1,
    folder => 'Imports'
);
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
// See full Go example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/blob/master/examples/cells/search_text_in_remote_range.go
cellsAPI, _, _ := cells.NewCellsApiClient(os.Getenv("ClientID"), os.Getenv("ClientSecret"))
resp, _, err := cellsAPI.CellsSearchContentInRemoteRange(
    context.Background(),
    "MyWorkbook.xlsx",
    "Orders_2024",
    "B2:H100",
    "Report",
    &cells.CellsSearchContentInRemoteRangeOptions{
        IgnoringCase: boolPtr(true),
        Folder:       stringPtr("Imports"),
    },
)
```

{{< /tab >}}
{{< /tabs >}}
