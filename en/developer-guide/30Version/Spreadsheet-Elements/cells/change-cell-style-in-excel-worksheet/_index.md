---
title: "Change Cell Style in Excel Worksheet – Aspose.Cells Cloud API Guide"
type: docs
url: /change-cell-style-in-excel-worksheet/
weight: 30
api_version: "v3.0"
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - Excel
  - Cell Style
  - REST API
  - Cloud SDK
  - cURL
  - cell style update
  - Excel API
description: "Change Excel cell style using Aspose.Cells Cloud API with cURL or SDKs (C#, Java, Python) and authentication examples"
tags:
  - cell-style
  - excel-api
  - rest
  - cloud
  - aspose.cells
categories:
  - cells
  - api-reference
article_title: "Change Cell Style in Excel Worksheet – Aspose.Cells Cloud API Guide"
linktitle: "Update Cell Style"
ArticleTitle: "Update Excel Cell Style with Aspose.Cells Cloud REST API"
---
The **PostUpdateWorksheetCellStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style`) enables developers to update the style of a specific cell in an Excel worksheet by specifying the workbook name, worksheet name, and cell name, with the style configuration sent in the request body; Aspose.Cells Cloud supports this operation via REST API and SDKs for .NET, Java, Python, Node.js, Go, and other languages, allowing precise, programmatic control over cell formatting without altering other worksheet content.

## The Post Update Worksheet Cell Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### Authentication

First, obtain a JWT access token:

```bash
JWT_TOKEN=$(curl -s "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
  | jq -r '.access_token')
```

> Replace `YOUR_CLIENT_ID` and `YOUR_CLIENT_SECRET` with your credentials from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| cellName | String | Path | The cell name. |
| style | class:style | HTTPBody | Style with update style settings. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### Example Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

The `PostUpdateWorksheetCellStyle` API endpoint allows you to update the style of a single cell. Here’s how to use it with `cURL`.

### Example Request: Apply Background Theme Color

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer ${JWT_TOKEN}" \
  -d '{
    "BackgroundThemeColor": {
      "ColorType": "Text2",
      "Tint": 0.2
    }
  }'
```

### HTTP Status Codes

| Code  | Meaning               | Description                                                  |
| ----- | --------------------- | ------------------------------------------------------------ |
| `200` | OK                    | Style updated successfully.                                  |
| `400` | Bad Request           | Invalid cell name, malformed JSON, or unsupported file type. |
| `401` | Unauthorized          | Invalid or missing JWT token.                                |
| `413` | Payload Too Large     | Request body exceeds 50 MB limit.                            |
| `500` | Internal Server Error | Unexpected server error.                                     |

> **Note**: The `Style` object in the response reflects the _current_ state after applying the update.

## Use Aspose.Cells Cloud SDKs

SDKs abstract low-level HTTP details and simplify integration. All official SDKs are open-source on [GitHub](https://github.com/aspose-cells-cloud).

### Available SDKs

- [C# (.NET)](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java)
- [PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php)
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)
- [Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby)
- [Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl)
- [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go)

### Code Examples

#### C# (.NET)

```csharp
// Install-Package Aspose.Cells.Cloud -Version 23.11.0

var config = new Configuration
{
    ClientId = "YOUR_CLIENT_ID",
    ClientSecret = "YOUR_CLIENT_SECRET"
};
var cellsApi = new CellsApi(config);
var style = new Style
{
    BackgroundThemeColor = new ThemeColor
    {
        ColorType = "Text2",
        Tint = 0.2
    }
};
var response = cellsApi.PostUpdateWorksheetCellStyle(
    "test_cells.xlsx", "Sheet3", "A1", style);
Console.WriteLine(response.Status);
```

#### Java

```java
// implementation, please see:
// https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/src/main/java/com/aspose/cells/examples/styles/UpdateCellStyle.java
```

#### Python

```python
# pip install asposecellscloud

from asposecellscloud.configuration import Configuration
from asposecellscloud.api.cells_api import CellsApi
from asposecellscloud.models.style import Style
from asposecellscloud.models.theme_color import ThemeColor

config = Configuration(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
api = CellsApi(config)

style = Style()
style.background_theme_color = ThemeColor(color_type="Text2", tint=0.2)

response = api.post_update_worksheet_cell_style(
    "test_cells.xlsx", "Sheet3", "A1", style)
print(response.status)
```

> 🔗 Explore full SDK examples, changelogs, and issue reporting on [GitHub](https://github.com/aspose-cells-cloud).
