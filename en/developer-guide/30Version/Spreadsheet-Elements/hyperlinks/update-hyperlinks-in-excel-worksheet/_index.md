---
title: "Update a Hyperlink in an Excel Worksheet – Aspose.Cells Cloud API Guide"
description: "Learn how to update a hyperlink in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, request‑body schema, cURL sample, SDK snippets, error handling, rate‑limiting and prerequisites."
keywords:
  - "Aspose.Cells"
  - "hyperlink update"
  - "Excel API"
  - "REST API"
  - "cloud spreadsheet"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Update a Hyperlink in an Excel Worksheet  

**API version:** v3.0  

The **PostWorksheetHyperlink** operation updates an existing hyperlink in a worksheet identified by its zero‑based index.

---

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Rate Limiting](#rate-limiting)  
3. [Endpoint](#endpoint)  
4. [Parameters](#parameters)  
   - [Path parameters](#path-parameters)  
   - [Query parameters](#query-parameters)  
   - [Request body schema](#request-body-schema)  
5. [Responses](#responses)  
   - [Success](#success-response)  
   - [Error responses](#error-responses)  
6. [cURL Example](#curl-example)  
7. [SDK Code Samples](#sdk-code-samples)  
8. [See Also](#see-also)  

---

## Prerequisites <a name="prerequisites"></a>

| Requirement | Description |
|-------------|-------------|
| **Authentication** | JWT token‑based authentication. Obtain a token as described in the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Storage** | The workbook must be stored in a supported Aspose Cloud storage (default is **Default**). |
| **Permissions** | The JWT token must have permission to read and write the target workbook. |
| **Headers** | `Content-Type: application/json` and `Accept: application/json` are required for all requests. |

---

## Rate Limiting <a name="rate-limiting"></a>

Aspose.Cells Cloud enforces a **maximum of 60 requests per minute per access token**. Exceeding this limit returns HTTP **429 Too Many Requests**. Implement exponential back‑off or respect the `Retry-After` header when throttling occurs.

---

## Endpoint <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Updates the hyperlink identified by `hyperlinkIndex` in the worksheet `sheetName` of the file `name`.*

---

## Parameters <a name="parameters"></a>

### Path parameters <a name="path-parameters"></a>

| Name            | Type   | Required | Description |
|-----------------|--------|----------|-------------|
| `name`          | string | ✅ | Name of the Excel file (including extension). |
| `sheetName`     | string | ✅ | Name of the worksheet that contains the hyperlink. |
| `hyperlinkIndex`| integer| ✅ | Zero‑based index of the hyperlink to be updated. |

### Query parameters <a name="query-parameters"></a>

| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `folder`    | string | ❌ | Folder path in the storage where the workbook resides. |
| `storageName`| string| ❌ | Name of the storage service (e.g., `Default`). |

### Request body schema <a name="request-body-schema"></a>

The request body must contain a **`hyperlink`** object. Only the fields you wish to change need to be supplied; omitted optional fields retain their existing values.

| Field         | Type   | Required | Description |
|---------------|--------|----------|-------------|
| `Address`     | string | ✅ | Target URL of the hyperlink. |
| `Area`        | object | ✅ | Cell range where the hyperlink is placed. Must contain `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (all integers, zero‑based). |
| `ScreenTip`   | string | ❌ | Tooltip displayed on mouse‑over. |
| `TextToDisplay`| string| ❌ | Text shown inside the cell. |
| `link`        | object| ❌ | Hypermedia links (`Href`, `Rel`, `Title`, `Type`). Generally omitted in request payloads. |

**`Area` object definition**

| Sub‑field   | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `StartRow`  | integer| ✅ | Zero‑based start row index. |
| `StartColumn`| integer| ✅ | Zero‑based start column index. |
| `EndRow`    | integer| ✅ | Zero‑based end row index. |
| `EndColumn` | integer| ✅ | Zero‑based end column index. |

---

## Responses <a name="responses"></a>

### Success response <a name="success-response"></a>

| Field | Type   | Description |
|-------|--------|-------------|
| `Code`| integer| HTTP status code (200 for success). |
| `Status`| string| Textual status (`OK`). |
| `Hyperlink`| object (optional) | The updated hyperlink object, returned when the `link` sub‑object is requested. |

**Example JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error responses <a name="error-responses"></a>

| HTTP Code | Reason | Example Body |
|-----------|--------|--------------|
| **400** | Bad Request – missing or invalid parameters. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Unauthorized – missing or invalid JWT token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Not Found – workbook, worksheet, or hyperlink does not exist. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | Too Many Requests – rate limit exceeded. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## cURL Example <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Response**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Tip:* Save the JSON payload to a file (e.g., `payload.json`) and reference it with `--data @payload.json` for cleaner copy‑pasting.

---

## SDK Code Samples <a name="sdk-code-samples"></a>

The following snippets demonstrate how to call **PostWorksheetHyperlink** using the official Aspose.Cells Cloud SDKs. Replace placeholder values (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>`, etc.) with real data.

| Language | Sample |
|----------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*All SDKs are open‑source and can be found in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).*

---

## See Also <a name="see-also"></a>

- **Authentication** – [Getting started with JWT tokens](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Storage operations** – [Upload a file](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Other hyperlink operations** – [Add a hyperlink](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Delete a hyperlink](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI Specification** – Full definition of the endpoint: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Document last updated: 2026‑07‑30*