---
title: "Import Data Using Storage"
description: "Import structured data (JSON, CSV, IntArray, etc.) into Excel worksheets via Aspose.Cells Cloud REST API. Includes authentication, request examples, HTTP status codes, and SDK usage."
date: 2024-02-28T10:30:00Z
lastmod: 2024-04-27T14:15:00Z
draft: false
tags:
  - excel
  - cloud
  - import
  - rest-api
  - json
  - csv
  - data-import
categories:
  - cells
  - api
weight: 10
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
linktitle: "Import data with storage"
---

# Import Data into Excel Using Cloud Storage

Aspose.Cells Cloud REST API enables you to import structured data from various sources (e.g., JSON, CSV, arrays) directly into Excel worksheets. This functionality supports cloud-based workflows, eliminating the need for local file handling.

## API Overview

### Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### Request Parameters

| Parameter     | Type   | Location | Required | Description |
|---------------|--------|----------|----------|-------------|
| `name`        | string | path     | Yes      | The name of the target Excel file (must exist in storage). |
| `folder`      | string | query    | No       | The folder path in storage where the Excel file resides. |
| `storageName` | string | query    | No       | The name of the storage service (e.g., "default", "MyCloudStorage"). |
| `region`      | string | query    | No       | Regional settings for workbook formatting (e.g., "en-US"). |
| `FontsLocation` | string | query | No       | Custom font directory path (if applicable). |
| `importOption` | object | body    | No       | JSON object specifying import behavior (e.g., `ImportStringArrayOption`, `ImportPictureOption`). |

> **Note**: The `importOption` parameter defines the data format and import behavior. Supported options include:
> - `ImportCSVDataOption`
> - `ImportBatchDataOption`
> - `ImportStringArrayOption`
> - `Import2DimensionStringArrayOption`
> - `ImportPictureOption`
> - `ImportIntArrayOption`

### Security & Authentication

All requests require a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) in the `Authorization` header:

```http
Authorization: Bearer <your-jwt-token>
```

Ensure the target workbook exists in the specified storage location before importing data.

---

## Import Data Option Parameters

The `importOption` body parameter requires the following common fields (specific fields vary by option type):

| Field              | Type    | Required | Description |
|--------------------|---------|----------|-------------|
| `DestinationWorksheet` | string | Yes      | Target worksheet name (e.g., `"Sheet1"`). |
| `FirstRow`         | integer | Yes      | Starting row index (0-based or 1-based depending on option). |
| `FirstColumn`      | integer | Yes      | Starting column index (0-based or 1-based). |
| `IsVertical`       | boolean | No       | Direction of data insertion (`true` = column-wise, `false` = row-wise). |
| `IsInsert`         | boolean | No       | Whether to insert new rows/columns (`true`) or overwrite existing data (`false`). |
| `Data`             | array   | Yes      | Data to import (e.g., `[1, 2, 4]`, `[["A1","B1"], ["A2","B2"]]`). |

For detailed parameter definitions, see the [Import Data Option Reference](/cells/import/#import-data-option-parameter).

---

## Example: Import Integer Array

This example imports a 1D integer array into `Sheet1`, starting at cell `B2`, vertically:

### Request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata?folder=Temp&storageName=" \
     -X POST \
     -d '{
       "importOption": {
         "DestinationWorksheet": "Sheet1",
         "FirstRow": 1,
         "FirstColumn": 1,
         "IsVertical": true,
         "IsInsert": true,
         "Data": [1, 2, 4],
         "importDataType": "IntArray"
       }
     }' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <your-jwt-token>"
```

### Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## HTTP Status Codes

| Code | Meaning             | Description |
|------|---------------------|-------------|
| 200  | OK                  | Data imported successfully. |
| 400  | Bad Request         | Invalid `importOption` structure, missing required fields, or unsupported `importDataType`. |
| 401  | Unauthorized        | Invalid or expired JWT token. |
| 403  | Forbidden           | Insufficient permissions for the target storage or file. |
| 404  | Not Found           | Excel file or storage location not found. |
| 413  | Payload Too Large   | Request body exceeds size limits. |
| 500  | Internal Server Error | Unexpected server error. |

---

## SDK Integration

Using an SDK simplifies authentication, request formatting, and error handling. Aspose.Cells Cloud provides official SDKs for:

- [.NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java)
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)
- [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go)

### PHP SDK Example

```php
<?php
require_once("vendor/autoload.php");

use Aspose\Cells\CellsApi;
use Aspose\Cells\Models\ImportIntArrayOption;

$clientId = "your_client_id";
$clientSecret = "your_client_secret";
$apiKey = "your_api_key";

$cellsApi = new CellsApi($clientId, $clientSecret);

$request = new ImportIntArrayOption();
$request->setDestinationWorksheet("Sheet1");
$request->setFirstRow(1);
$request->setFirstColumn(1);
$request->setIsVertical(true);
$request->setIsInsert(true);
$request->setData([1, 2, 4]);

try {
    $result = $cellsApi->PostImportData("Book1.xlsx", $request, "Temp", "");
    echo "Import successful: " . $result->getStatus();
} catch (Exception $e) {
    echo "Error: " . $e->getMessage();
}
?>
```

> **Tip**: See the [Aspose.Cells Cloud SDKs GitHub Repository](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer"} for language-specific samples and documentation.

---

## Best Practices

1. **Validate Data Format**  
   Ensure the `Data` array matches the `importDataType` (e.g., use `ImportStringArrayOption` for `["A", "B", "C"]`).

2. **Handle Row/Column Indexing**  
   Confirm whether your SDK uses 0-based or 1-based indexing (most Aspose.Cells SDKs use 0-based for arrays).

3. **Test with `IsInsert=false` First**  
   Overwrite mode (`IsInsert=false`) avoids unintended worksheet expansion during initial testing.

4. **Use Storage Names Explicitly**  
   Specify `storageName` to avoid ambiguity in multi-storage environments.

5. **Check Region Settings**  
   For CSV or localized data, set `region` to match the data’s locale (e.g., `"de-DE"` for German number formats).

---

## Related Topics

- [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [Export Excel to PDF](/cells/export/)
- [Working with Cloud Storage](/storage/)

---

**Last Updated**: 2024-04-27