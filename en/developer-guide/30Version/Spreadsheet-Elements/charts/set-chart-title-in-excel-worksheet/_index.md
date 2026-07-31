---
title: "Set Chart Title in an Excel Worksheet – Aspose.Cells Cloud API"
description: "Add or update a chart title in an Excel worksheet using the Aspose.Cells Cloud REST API (v3.0). Includes HTTPS cURL, SDK samples, required parameters, authentication, response headers, and error handling."
keywords:
  - Aspose.Cells Cloud
  - chart title API
  - Excel chart title
  - REST API
  - SDK examples
version: "v3.0"
badge: "[![API version](https://img.shields.io/badge/API%20v3.0-blue)](https://api.aspose.cloud/cells/v3.0)"
---

# Set Chart Title in an Excel Worksheet

> **Version:** `v3.0`  `{{< badge >}}`  
> **Summary:** Use the **PUT** operation to add a new chart title or make an existing title visible in a worksheet chart.

---

## Prerequisites

Before calling the API you must:

1. **Create an Aspose Cloud account** and subscribe to the **Aspose.Cells Cloud** service.  
2. **Obtain a JWT access token** (OAuth 2.0). The token must be included in the `Authorization` header as `Bearer <jwt token>`.  
3. **Upload the workbook** to Aspose Cloud Storage (or reference a file already stored).  
4. Ensure the target **storage** (default is `Default`) is accessible and the workbook path (`folder`) is correct.  

*All API calls must be made over **HTTPS** (TLS 1.2+).*

---

## HTTP Request

```
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Path Parameters

| Parameter   | Type   | Description                |
|-------------|--------|----------------------------|
| `name`      | string | The workbook file name.    |
| `sheetName` | string | The worksheet name.        |
| `chartIndex`| integer| Zero‑based index of the chart. |

### Query Parameters *(optional)*

| Parameter   | Type   | Description                                   |
|-------------|--------|-----------------------------------------------|
| `folder`    | string | Folder that contains the workbook.            |
| `storageName`| string| Name of the storage (e.g., `Default`).        |

### Body Parameter *(optional)*

```json
{
  "Text": "Your chart title"
}
```

*The body must be a JSON representation of the **Title** model. Only the `Text` property is required to set the title string.*

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title?folder=Docs&storageName=Default" \
  -X PUT \
  -H "Authorization: Bearer <jwt-token>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{"Text":"Sales Chart"}'
```

> **Note:** The example uses `https://` to guarantee encrypted transport. Replace `<jwt-token>` with a valid JWT.

---

## Successful Response

| Element | Type   | Description |
|---------|--------|-------------|
| `Code`  | string | HTTP‑style status code (`200`). |
| `Status`| string | Human‑readable status (`OK`). |

**Example JSON payload**

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Example response headers**

```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Sun, 30 Jul 2026 08:15:42 GMT
Connection: keep-alive
```

---

## Error Responses

| HTTP Code | Example Payload | Description |
|-----------|----------------|-------------|
| **400**   | `{ "Code": "400", "Message": "Invalid request payload." }` | Malformed JSON or missing required fields. |
| **401**   | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | Missing, invalid, or expired JWT. |
| **404**   | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }` | The specified resource does not exist. |
| **500**   | `{ "Code": "500", "Message": "Internal server error." }` | Unexpected server‑side failure. |

---

## SDK Sample Code

The following snippets demonstrate how to call the **PutWorksheetChartTitle** operation using Aspose.Cells Cloud SDKs. Replace placeholder values (`<fileName>`, `<sheet>`, etc.) with your own data.

| Language | Example |
|----------|---------|
| **C# (.NET)** | ```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new ChartsApi();\nvar title = new Title { Text = \"Sales Chart\" };\nawait api.PutWorksheetChartTitleAsync(name: \"Sample_Test_Book.xls\", sheetName: \"Sheet5\", chartIndex: 0, title: title, folder: \"Docs\", storageName: \"Default\");\n``` |
| **Java** | ```java\nChartsApi chartsApi = new ChartsApi();\nTitle title = new Title();\ntitle.setText(\"Sales Chart\");\nchartsApi.putWorksheetChartTitle(\"Sample_Test_Book.xls\", \"Sheet5\", 0, title, \"Docs\", \"Default\");\n``` |
| **Python** | ```python\nfrom asposecellscloud import ChartsApi, Title\napi = ChartsApi()\ntitle = Title(text='Sales Chart')\napi.put_worksheet_chart_title(name='Sample_Test_Book.xls', sheet_name='Sheet5', chart_index=0, title=title, folder='Docs', storage_name='Default')\n``` |
| **Node.js** | ```javascript\nconst { ChartsApi, Title } = require('asposecellscloud');\nconst api = new ChartsApi();\nconst title = new Title({ text: 'Sales Chart' });\napi.putWorksheetChartTitle('Sample_Test_Book.xls', 'Sheet5', 0, title, 'Docs', 'Default')\n  .then(() => console.log('Title set'))\n  .catch(err => console.error(err));\n``` |
| **PHP** | ```php\nuse Aspose\\Cells\\Cloud\\Api\\ChartsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Title;\n\n$api = new ChartsApi();\n$title = new Title();\n$title->setText('Sales Chart');\n$api->putWorksheetChartTitle('Sample_Test_Book.xls', 'Sheet5', 0, $title, 'Docs', 'Default');\n``` |
| **Go** | ```go\nimport (\n    \"github.com/aspose-cells-cloud/go-sdk/api\"\n    \"github.com/aspose-cells-cloud/go-sdk/model\"\n)\n\nclient := api.NewChartsApi()\ntitle := model.Title{Text: \"Sales Chart\"}\n_, err := client.PutWorksheetChartTitle(\"Sample_Test_Book.xls\", \"Sheet5\", 0, &title, \"Docs\", \"Default\")\nif err != nil { panic(err) }\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ChartsApi.new\ntitle = AsposeCellsCloud::Title.new(text: 'Sales Chart')\napi.put_worksheet_chart_title('Sample_Test_Book.xls', 'Sheet5', 0, title, folder: 'Docs', storage_name: 'Default')\n``` |
| **Perl** | ```perl\nuse Aspose::Cells::Cloud::Api::ChartsApi;\nuse Aspose::Cells::Cloud::Model::Title;\nmy $api   = Aspose::Cells::Cloud::Api::ChartsApi->new();\nmy $title = Aspose::Cells::Cloud::Model::Title->new(text => 'Sales Chart');\n$api->put_worksheet_chart_title(name => 'Sample_Test_Book.xls', sheet_name => 'Sheet5', chart_index => 0, title => $title, folder => 'Docs', storage_name => 'Default');\n``` |

> **Tip:** All SDKs automatically prepend the `https://` base URL and inject the `Authorization` header when you configure the `ApiClient` with your JWT token.

---

## See Also

- **[Get Chart Title](https://docs.aspose.cloud/cells/chart/title/get/)** – Retrieve the current chart title.  
- **[Delete Chart Title](https://docs.aspose.cloud/cells/chart/title/delete/)** – Remove a chart title.  
- **[Update Chart Title](https://docs.aspose.cloud/cells/chart/title/patch/)** – Partially modify an existing title.  
- **[Charts Overview](https://docs.aspose.cloud/cells/charts/)** – General information about chart operations.  

---

## Additional References

- **OpenAPI Specification** – Detailed contract for the operation: <https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle>  
- **Aspose.Cells Cloud SDK Repository** – Source code and further examples: <https://github.com/aspose-cells-cloud>  

--- 

*Document last updated: 2026‑07‑30*