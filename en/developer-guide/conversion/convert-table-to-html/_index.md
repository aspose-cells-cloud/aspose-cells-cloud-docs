---
title: "Convert Excel Table to HTML | Aspose.Cells Cloud"
description: "Convert Excel tables to HTML via Aspose.Cells Cloud REST API: secure, format-preserving, no upload needed."
keywords: "Aspose.Cells Cloud, Excel table to HTML, convert table to HTML, cloud API, spreadsheet conversion"
weight: 100
linktitle: "Convert Table To Html"
date: 2024-05-10
last_updated: 2024-05-10
version: "v3.0"
url: /convert-table-to-html/
type: docs
aliases: ["/api/convert-table-to-html", "/docs/cells/convert/table/html"]
ArticleTitle: "Aspose.Cells Cloud API: Convert Excel Table to HTML via REST"
---
The **ConvertTableToHtml** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/table/html`) in Aspose.Cells Cloud enables direct conversion of a specified table from a local Excel workbook to HTML format without requiring intermediate cloud storage upload. The API accepts the spreadsheet file via form-data, along with the worksheet and table name as query parameters, processes the conversion entirely on the cloud server, and returns the resulting HTML as a downloadable stream.

## The Convert Table to HTML Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/authentication/" rel="noopener noreferrer">JWT token-based authentication</a>.  
_Replace `{YOUR_ACCESS_TOKEN}` in examples with a valid JWT token obtained from the Aspose Cloud dashboard._

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| tableName | String | Query | table name |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

## When to Use the Convert Table to HTML API?

- **Dynamic web content** – Embed pricing tables, schedules, or product lists directly into web pages or CMSes.
- **Email templates** – Generate HTML snippets for order summaries or reports that render consistently across email clients.
- **Dashboards & reporting tools** – Show live spreadsheet data without loading the full workbook or using heavy grid components.
- **Document previews** – Provide quick, format‑preserving previews of specific spreadsheet sections.
- **Avoid using for large workbooks (>10k rows)** — consider pagination or streaming endpoints to ensure reliability and performance.

## How to Use the Convert Table to HTML API with SDKs?

### Convert Table to HTML API Specification

The [Convert Table to HTML API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) provides a publicly accessible programming interface, allowing REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert spreadsheet table data to HTML with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

#### C# Example

```csharp
var config = new Configuration { ClientId = "xxx", ClientSecret = "yyy" };
var cellsApi = new CellsApi(config);
var response = cellsApi.CellsTablePostTableToHtml(
    worksheet: "Sheet1",
    tableName: "Table1",
    filename: "myWorkbook.xlsx"
);
```

#### Python Example

```python
from asposecellscloud.configuration import Configuration
from asposecellscloud.apis.cells_api import CellsApi

config = Configuration()
config.client_id = "xxx"
config.client_secret = "yyy"
cells_api = CellsApi(config)

response = cells_api.cells_table_post_table_to_html(
    worksheet="Sheet1",
    table_name="Table1",
    filename="myWorkbook.xlsx"
)
```
