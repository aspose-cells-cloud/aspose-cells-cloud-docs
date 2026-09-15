---
title: "Set Row Height for a Range in Excel – Aspose.Cells Cloud API (v3.0)"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Row height"
type: docs
url: /ranges/update/row-height/
description: "Learn how to programmatically set row height for a range in Excel worksheets using Aspose.Cells Cloud REST API v3.0, with full cURL and SDK examples for multiple languages."
keywords:
  - "row height"
  - "Excel range"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "SDK"
date: 2024-06-15
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
canonical: "https://docs.aspose.cloud/cells/ranges/update/row-height/"
---

# Set Row Height for a Range in Excel

This operation updates the row height of a specified range on a worksheet stored in Aspose Cloud storage.

## Prerequisites / Authentication

You must obtain a JWT access token from the Aspose Cloud OAuth service with the **Cells.ReadWrite** scope.

Include the token in the `Authorization` header of every request:

```http
Authorization: Bearer YOUR_JWT_TOKEN_HERE
```

> **Note**: Replace `YOUR_JWT_TOKEN_HERE` with your actual JWT access token. If you do not have a token, follow the [authentication guide](/authentication/) to request one.

## HTTP Request

| Method   | URI                                                                                  |
| -------- | ------------------------------------------------------------------------------------ |
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Path Parameters

| Name        | Type     | Description                                                   |
| ----------- | -------- | ------------------------------------------------------------- |
| `name`      | `string` | **Required.** The name of the Excel file stored in the cloud. |
| `sheetName` | `string` | **Required.** The worksheet that contains the target range.   |

### Query Parameters

| Name          | Type     | Required | Description                                                        |
| ------------- | -------- | -------- | ------------------------------------------------------------------ |
| `value`       | `number` | **Yes**  | Desired row height (in points) to apply to the range.              |
| `folder`      | `string` | No       | Folder path in storage where the file is located.                  |
| `storageName` | `string` | No       | Name of the storage service (if multiple storages are configured). |

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

| Property      | Type    | Required | Description                                                          |
| ------------- | ------- | -------- | -------------------------------------------------------------------- |
| `FirstRow`    | integer | **Yes**  | Zero-based index of the first row in the range.                      |
| `RowCount`    | integer | **Yes**  | Number of rows to which the height will be applied.                  |
| `FirstColumn` | integer | No       | Zero-based index of the first column (optional for row-height only). |
| `ColumnCount` | integer | No       | Number of columns the range spans (optional).                        |

Only the properties listed above are used for the row-height operation; any extra fields are ignored.

## Sample Request

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN_HERE" \
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

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Row height updated successfully.                                  |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

All responses contain a numeric `Code` and a human-readable `Status` (or `Message` for errors). Additional `ErrorDetails` may be provided when an error occurs.

## SDK Examples

The following snippets demonstrate how to call **Set Row Height for a Range** using the official Aspose.Cells Cloud SDKs.

| Language    | Example                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **C#**      | <details><summary>Show code</summary><code>using Aspose.Cells.Cloud.SDK.Api;<br>using Aspose.Cells.Cloud.SDK.Model;<br><br>var api = new RangesApi(configuration);<br>var range = new Range { FirstRow = 9, RowCount = 1 };<br>await api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);</code></details>                                                                                                                                                                                    |
| **Java**    | <details><summary>Show code</summary><code>import com.aspose.cloud.cells.api.RangesApi;<br>import com.aspose.cloud.cells.model.Range;<br><br>RangesApi api = new RangesApi(config);<br>Range range = new Range().firstRow(9).rowCount(1);<br>api.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);</code></details>                                                                                                                                                                     |
| **Python**  | <details><summary>Show code</summary><code>from asposecellscloud import RangesApi, ApiClient, Configuration<br><br>config = Configuration()<br>config.access_token = 'YOUR_JWT_TOKEN_HERE'<br>api = RangesApi(ApiClient(config))<br>range = {'FirstRow': 9, 'RowCount': 1}<br>api.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)</code></details>                                                                                                                                                    |
| **Node.js** | <details><summary>Show code</summary><code>const { RangesApi, Configuration } = require('asposecellscloud');<br>const config = new Configuration();<br>config.accessToken = 'YOUR_JWT_TOKEN_HERE';<br>const api = new RangesApi(config);<br>const range = { FirstRow: 9, RowCount: 1 };<br>api.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)<br>  .then(() => console.log('Row height set'))<br>  .catch(err => console.error(err));</code></details>                                                        |
| **PHP**     | <details><summary>Show code</summary><code>use Aspose\Cells\Configuration;<br>use Aspose\Cells\Api\RangesApi;<br><br>$config = new Configuration();<br>$config->setAccessToken('YOUR_JWT_TOKEN_HERE');<br>$api = new RangesApi($config);<br>$range = ['FirstRow' => 9, 'RowCount' => 1];<br>$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);</code></details>                                                                                                                                                  |
| **Ruby**    | <details><summary>Show code</summary><code>require 'aspose_cells_cloud'<br>config = AsposeCellsCloud::Configuration.new<br>config.access_token = 'YOUR_JWT_TOKEN_HERE'<br>api = AsposeCellsCloud::RangesApi.new<br>range = { 'FirstRow' => 9, 'RowCount' => 1 }<br>api.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)</code></details>                                                                                                                                                              |
| **Go**      | <details><summary>Show code</summary><code>import (<br>    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"<br>    "context"<br>)<br><br>cfg := asposecellscloud.NewConfiguration()<br>cfg.AccessToken = "YOUR_JWT_TOKEN_HERE"<br>api := asposecellscloud.NewRangesApi(cfg)<br>rangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }<br>_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)<br>if err != nil { panic(err) }</code></details> |
| **Perl**    | <details><summary>Show code</summary><code>use AsposeCellsCloud::Api::RangesApi;<br>my $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => 'YOUR_JWT_TOKEN_HERE' });<br>my $range = { FirstRow => 9, RowCount => 1 };<br>$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);</code></details>                                                                                                                                                                                            |

> **Note**: All SDKs automatically add the required `Authorization: Bearer` header when the access token is configured.

## See Also

- [Set Column Width for a Range](/ranges/update/column-width/)
- [Batch Update Worksheet Ranges](/ranges/batch-update/)
- **OpenAPI Specification** – Detailed contract for this operation: [PostWorksheetCellsRangeRowHeight](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight)
- **Aspose.Cells Cloud SDK Repository** – Source code and additional language bindings: [GitHub](https://github.com/aspose-cells-cloud)
- **Authentication Guide** – How to obtain a JWT token: [Authentication Guide](/authentication/)

> **Updated for Aspose.Cells Cloud v3.0 (released 2024-06)**