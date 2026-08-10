---
title: "Set Row Height for a Range in Excel – Aspose.Cells Cloud API (v3.0)"
description: "Change the height of rows within a specific range of an Excel worksheet using the Aspose.Cells Cloud REST API. Includes endpoint, parameters, cURL example, sample responses, and SDK snippets for multiple languages."
keywords: "Aspose.Cells, row height, range, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Set Row Height for a Range in Excel

This operation updates the row height of a specified range on a worksheet stored in Aspose Cloud storage.

## Prerequisites / Authentication

You must obtain a JWT access token from the Aspose Cloud OAuth service with the **Cells.ReadWrite** scope.

Include the token in the `Authorization` header of every request:

```http
Authorization: Bearer <jwt token>
```

If you do not have a token, follow the **Aspose Cloud authentication guide** to request one.

## HTTP Request

| Method | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Path Parameters

| Name | Type | Description |
|------|------|-------------|
| `name` | `string` | **Required.** The name of the Excel file stored in the cloud. |
| `sheetName` | `string` | **Required.** The worksheet that contains the target range. |

### Query Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `value` | `number` | **Yes** | Desired row height (in points) to apply to the range. |
| `folder` | `string` | No | Folder path in storage where the file is located. |
| `storageName` | `string` | No | Name of the storage service (if multiple storages are configured). |

### Request Body (JSON)

The body must contain a **Range** object that defines which rows are affected.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Range JSON Schema

| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `FirstRow` | integer | **Yes** | Zero‑based index of the first row in the range. |
| `RowCount` | integer | **Yes** | Number of rows to which the height will be applied. |
| `FirstColumn` | integer | No | Zero‑based index of the first column (optional for row‑height only). |
| `ColumnCount` | integer | No | Number of columns the range spans (optional). |

Only the properties listed above are used for the row‑height operation; any extra fields are ignored.

## Sample Request

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Sample Response (Success)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

All responses contain a numeric `Code` and a human‑readable `Status` (or `Message` for errors). Additional `ErrorDetails` may be provided when an error occurs.

## SDK Examples

The following snippets demonstrate how to call **Set Row Height for a Range** using the official Aspose.Cells Cloud SDKs.

| Language | Example |
|----------|---------|
| **C#** | <details><summary>Show code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync(\"test.xlsx\", \"Sheet1\", range, 15);\n```</details> |
| **Java** | <details><summary>Show code</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight(\"test.xlsx\", \"Sheet1\", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Show code</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Show code</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Show code</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Show code</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Show code</summary>```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"context\"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = \"<jwt token>\"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ \"FirstRow\": 9, \"RowCount\": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), \"test.xlsx\", \"Sheet1\", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Show code</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Note:** All SDKs automatically add the required `Authorization: Bearer` header when the access token is configured.

## See Also

- **OpenAPI Specification** – Detailed contract for this operation: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK Repository** – Source code and additional language bindings: <https://github.com/aspose-cells-cloud>
- **Authentication Guide** – How to obtain a JWT token: <https://docs.aspose.cloud/cells/authentication/>

---