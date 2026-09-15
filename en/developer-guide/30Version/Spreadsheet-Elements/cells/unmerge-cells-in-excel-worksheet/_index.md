---
title: "Unmerge Cells in Excel Worksheet"
type: docs
url: /unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, unmerge cells, REST API, cloud, C#, Python, Java, SDK"
description: "Unmerge merged cells in Excel worksheets via Aspose.Cells Cloud REST API. Includes cURL and SDK examples (C#, Java, Python, Ruby, Node.js, PHP, Perl, Go), authentication details, and parameter guidance."
ArticleTitle: "Unmerge Cells in Excel Worksheet"
date: 2024-03-15T00:00:00Z
lastmod: 2024-03-15T00:00:00Z
tags:
  - cells
  - unmerge
  - rest-api
  - excel
  - cloud
related:
  - url: /merge-cells-in-excel-worksheet/
    title: Merge Cells in Excel Worksheet
---

This REST API endpoint unmerges previously merged cells in an Excel worksheet using Aspose.Cells Cloud. The operation supports specifying a rectangular cell range to unmerge and returns a confirmation response. SDKs for .NET, Java, Python, Ruby, Node.js, PHP, Perl, and Go are available to accelerate development.

> **API Version**: Aspose.Cells Cloud v24.3  
> **Supported Formats**: `.xlsx`, `.xlsb`, `.xlsm`, `.xls`

## REST API

### Endpoint

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

### Security and Authentication

The API uses JWT token-based authentication. Before making requests, ensure you have obtained a valid access token with the `user` scope. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for detailed instructions.

> **Note**: Include the header `x-aspose-client: DeveloperTool` in all requests to help us improve service reliability.

## Request Parameters

| Parameter Name | Type    | Location | Required | Description |
|----------------|---------|----------|----------|-------------|
| `name`         | string  | path     | Yes      | Name of the workbook file. |
| `sheetName`    | string  | path     | Yes      | Name of the worksheet containing the merged cells. |
| `startRow`     | integer | query    | Yes      | Zero-based index of the first row in the range to unmerge. |
| `startColumn`  | integer | query    | Yes      | Zero-based index of the first column in the range to unmerge. |
| `totalRows`    | integer | query    | Yes      | Number of rows to include in the unmerge operation. |
| `totalColumns` | integer | query    | Yes      | Number of columns to include in the unmerge operation. |
| `folder`       | string  | query    | No       | Folder path where the workbook is stored (e.g., `"docs/input"`). |
| `storageName`  | string  | query    | No       | Name of the storage service (e.g., `"First Aspose Storage"`). |

> **Tip**: Omitting `folder` and `storageName` defaults to the root folder and default storage configured for your account.

## Response

The API returns a `CellsCloudResponse` object with the following fields:

| Field    | Type   | Description |
|----------|--------|-------------|
| `Status` | string | `"OK"` on success; `"Error"` on failure. |
| `Code`   | integer| HTTP status code (e.g., `200`, `400`, `401`, `500`). |

### Example Response

```json
{
  "Status": "OK",
  "Code": 200
}
```

### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Unmerge operation completed successfully. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., non-numeric `startRow`, unsupported file extension). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 404  | Not Found             | Workbook or worksheet not found. |
| 413  | Payload Too Large     | Workbook exceeds maximum file size limit (1 GB). |
| 500  | Internal Server Error | Unexpected server error. Contact support with request ID. |

## How to Use the API

### Using cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=5&totalColumns=3" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <your_jwt_token>" \
-H "x-aspose-client: DeveloperTool"
```

**Response:**

```json
{
  "Status": "OK",
  "Code": 200
}
```

### Using Aspose.Cells Cloud SDKs

SDKs handle low-level HTTP communication, authentication, and serialization. Below are concise examples for major languages.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" title="C#" >}}

```csharp
// Replace 'MyApp.SID' and 'MyApp.Key' with your credentials
var cellsApi = new CellsApi("MyApp.SID", "MyApp.Key");
var response = cellsApi.PostWorksheetUnmerge(
    name: "test.xlsx",
    sheetName: "Sheet1",
    startRow: 10,
    startColumn: 10,
    totalRows: 5,
    totalColumns: 3
);
Console.WriteLine($"Status: {response.Status}, Code: {response.Code}");
```
{{< /tab >}}

{{< tab tabNum="2" title="Java" >}}

```java
// Replace 'clientId' and 'clientSecret' with your credentials
CellsApi cellsApi = new CellsApi("MyApp.SID", "MyApp.Key");
CellsCloudResponse response = cellsApi.postWorksheetUnmerge(
    "test.xlsx", "Sheet1", 10, 10, 5, 3, null, null
);
System.out.println("Status: " + response.getStatus() + ", Code: " + response.getCode());
```
{{< /tab >}}

{{< tab tabNum="3" title="PHP" >}}

```php
// Replace with your credentials
$cellsApi = new CellsApi("MyApp.SID", "MyApp.Key");
$response = $cellsApi->postWorksheetUnmerge(
    "test.xlsx", "Sheet1", 10, 10, 5, 3, null, null
);
echo "Status: " . $response->getStatus() . ", Code: " . $response->getCode();
```
{{< /tab >}}

{{< tab tabNum="4" title="Ruby" >}}

```ruby
# Replace with your credentials
cells_api = AsposeCellsCloud::CellsApi.new("MyApp.SID", "MyApp.Key")
response = cells_api.post_worksheet_unmerge(
  'test.xlsx', 'Sheet1', 10, 10, 5, 3, nil, nil
)
puts "Status: #{response.status}, Code: #{response.code}"
```
{{< /tab >}}

{{< tab tabNum="5" title="Node.js" >}}

```typescript
// Replace with your credentials
const cellsApi = new CellsApi("MyApp.SID", "MyApp.Key");
const response = await cellsApi.postWorksheetUnmerge(
  'test.xlsx', 'Sheet1', 10, 10, 5, 3, undefined, undefined
);
console.log(`Status: ${response.body.status}, Code: ${response.body.code}`);
```
{{< /tab >}}

{{< tab tabNum="6" title="Python" >}}

```python
# Replace with your credentials
cells_api = CellsApi("MyApp.SID", "MyApp.Key")
response = cells_api.post_worksheet_unmerge(
    'test.xlsx', 'Sheet1', 10, 10, 5, 3, folder=None, storage_name=None
)
print(f"Status: {response.status}, Code: {response.code}")
```
{{< /tab >}}

{{< tab tabNum="7" title="Perl" >}}

```perl
# Replace with your credentials
my $cells_api = AsposeCellsCloud::API->new(
    client_id => "MyApp.SID",
    client_secret => "MyApp.Key"
);
my $response = $cells_api->post_worksheet_unmerge(
    'test.xlsx', 'Sheet1', 10, 10, 5, 3, { folder => undef, storage_name => undef }
);
print "Status: $response->{status}, Code: $response->{code}\n";
```
{{< /tab >}}

{{< tab tabNum="8" title="Go" >}}

```go
// Replace with your credentials
cfg := cells.NewConfiguration("MyApp.SID", "MyApp.Key")
client := cells.NewClient(cfg)
resp, err := client.CellsPostWorksheetUnmerge(
    context.Background(),
    "test.xlsx", "Sheet1", 10, 10, 5, 3,
    nil, nil,
)
if err != nil {
    log.Fatal(err)
}
fmt.Printf("Status: %s, Code: %d\n", *resp.Status, resp.Code)
```
{{< /tab >}}

{{< /tabs >}}

> **Tip**: All SDK examples assume credentials are configured via environment variables or explicit initialization. Never hard-code secrets in production code.

## Related Operations

- [Merge Cells in Excel Worksheet](/merge-cells-in-excel-worksheet/) — Merge adjacent cells into a single range.
- [Get Worksheet Cells](/get-worksheet-cells/) — Retrieve cell data, including merged regions.
- [Clear Cells](/clear-cells-in-excel-worksheet/) — Clear contents, formatting, or comments from a range.

## Support

For issues or questions, contact [Aspose.Cells Cloud Support](https://helpdesk.aspose.cloud/) or post to our [community forum](https://forum.aspose.cloud/).