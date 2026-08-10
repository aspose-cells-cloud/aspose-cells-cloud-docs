---
title: "Delete Column from an Excel Worksheet using Aspose.Cells Cloud API"
description: "Learn how to delete one or more columns from an Excel worksheet via the Aspose.Cells Cloud REST API. Includes authentication, request syntax, parameters, responses, error handling, and SDK examples."
keywords: ["Aspose.Cells", "Delete Column", "Excel API", "REST", "Cloud", "Worksheet", "Columns"]
date: 2026-07-30
api_version: "v3.0"
---

# Delete Column from Excel Worksheet

**Endpoint**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

The operation removes a single column or a range of columns from a worksheet. Cell references (including formulas) can be updated automatically after the deletion.

---

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Authentication](#authentication)  
3. [Request URL & HTTP Method](#request-url--http-method)  
4. [Parameters](#parameters)  
   - [Path parameters](#path-parameters)  
   - [Query parameters](#query-parameters)  
5. [cURL Example](#curl-example)  
6. [Responses](#responses)  
7. [Error Codes](#error-codes)  
8. [SDK Samples](#sdk-samples)  
9. [Additional Notes](#additional-notes)  

---

## Prerequisites
- A valid **JWT access token** obtained via the Aspose Cloud authentication flow.  
- The workbook (`{name}`) must already be uploaded to Aspose Cloud storage (or accessible via the `folder`/`storageName` query parameters).  

---

## Authentication
All Aspose.Cells Cloud requests require **Bearer token** authentication.

```http
Authorization: Bearer <access_token>
```

Refer to the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details on obtaining a JWT token.

---

## Request URL & HTTP Method
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – workbook file name (e.g., `test.xlsx`).  
- **`{sheetName}`** – worksheet name (e.g., `Sheet1`).  
- **`{columnIndex}`** – zero‑based index of the first column to delete.

---

## Parameters

| Name            | Location | Type    | Required | Description |
|-----------------|----------|---------|----------|-------------|
| **name**        | path     | string  | ✅ Yes   | Workbook file name. |
| **sheetName**   | path     | string  | ✅ Yes   | Worksheet name. |
| **columnIndex** | path     | integer | ✅ Yes   | Zero‑based index of the first column to delete. |
| **startColumn** | query    | integer | ❌ No    | Zero‑based index where deletion starts. Defaults to `columnIndex` if omitted. |
| **totalColumns**| query    | integer | ❌ No    | Number of columns to delete. If omitted, only the column identified by `columnIndex` is removed. |
| **updateReference** | query | boolean | ❌ No | When `true`, updates cell references (including formulas) across the workbook after deletion. |
| **folder**      | query    | string  | ❌ No    | Path to the folder that contains the workbook. |
| **storageName** | query    | string  | ❌ No    | Name of the Aspose Cloud storage service. |

> **Note** – The `columns` parameter shown in the low‑level API spec has been superseded by the more expressive `startColumn` and `totalColumns` query parameters. Both approaches are accepted for backward compatibility.

---

## cURL Example

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Explanation
- Deletes column **B** (`columnIndex = 1`) from `Sheet1` of `test.xlsx`.  
- `startColumn=1` and `totalColumns=1` specify a single‑column deletion.  
- `updateReference=true` ensures formulas and other references are automatically adjusted.

---

## Responses

| HTTP Code | Description | Example |
|-----------|-------------|---------|
| **200** | Success – the column(s) were deleted. | `{ "Code": 200, "Status": "OK" }` |
| **400** | Bad request – missing or invalid parameters. | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401** | Unauthorized – missing or invalid JWT token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | Not found – workbook or worksheet does not exist. | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500** | Internal server error – unexpected condition on the server. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

The response body follows the generic **`CellsCloudResponse`** model.

---

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
---

## SDK Samples

Below are ready‑to‑run snippets for the most popular SDKs. Replace placeholder values (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>`, etc.) with your own data.

| Language | Sample |
|----------|--------|
| **C#** | <details><summary>Show code</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = \"<YOUR_ACCESS_TOKEN>\", BaseUrl = \"https://api.aspose.cloud\" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: \"test.xlsx\",\n                                         sheetName: \"Sheet1\",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($\"Status: {response.Status}\");\n```</details> |
| **Java** | <details><summary>Show code</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken(\"<YOUR_ACCESS_TOKEN>\");\nconfig.setBaseUrl(\"https://api.aspose.cloud\");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns(\"test.xlsx\", \"Sheet1\", 1, 1, 1, true, null, null);\nSystem.out.println(\"Status: \" + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Show code</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Show code</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Show code</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Show code</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>Show code</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Show code</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*All SDKs automatically add the required `Authorization` header when the `access_token` is configured.*

---

## Additional Notes

### Security Headers (recommended for production)
When serving the documentation page, include the following HTTP response headers to improve security:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Performance Tips
- Load third‑party analytics scripts (`gtag.js`, `containerize.js`) with the `async` attribute or defer them until after the page has rendered.  
- Minify any custom JavaScript/CSS bundles.  
- Preload small SVG icons if they are render‑blocking:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO Enhancements (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Delete Column from Excel Worksheet using Aspose.Cells Cloud API",
  "description": "Learn how to delete one or more columns from an Excel worksheet via Aspose.Cells Cloud REST API.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Delete Column", "Excel", "REST API"]
}
```

Place the snippet inside a `<script type="application/ld+json">` block in the HTML head.

### Accessibility
- All decorative images use `alt=""` or are hidden with `aria-hidden="true"`.  
- The Open Graph image now includes an `alt` attribute in the meta tag for completeness.  

---

## See Also
- [OpenAPI Specification for DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud)  

---