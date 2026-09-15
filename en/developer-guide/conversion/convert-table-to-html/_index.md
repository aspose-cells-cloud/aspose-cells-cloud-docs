---
title: "Convert Excel Table to HTML | Aspose.Cells Cloud"
description: "Aspose.Cells Cloud API v3: Convert Excel tables to HTML via REST. Secure, format-preserving, and SDK-ready. No upload required."
keywords: "Aspose.Cells Cloud, Excel table to HTML, convert table to HTML, cloud API, spreadsheet conversion"
weight: 100
date: 2024-05-10
last_updated: 2024-05-10
version: "v3.0"
url: /convert-table-to-html/
type: docs
aliases: ["/api/convert-table-to-html", "/docs/cells/convert/table/html"]
---

**Quick summary** – This endpoint reads a local Excel workbook, extracts the specified **table**, converts it to an **HTML** file, and returns the result as a downloadable stream. No intermediate upload to Aspose Cloud storage is required.

## ConvertTableToHTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/authentication/" rel="noopener noreferrer">JWT token-based authentication</a>.  
*Replace `{YOUR_ACCESS_TOKEN}` in examples with a valid JWT token obtained from the Aspose Cloud dashboard.*

### Request Parameters

| Name               | Location  | Type      | Required | Description                                                                       |
| ------------------ | --------- | --------- | -------- | --------------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data | `File`    | **Yes**  | The Excel workbook containing the table to convert.                               |
| **worksheet**      | Query     | `String`  | **Yes**  | Name of the worksheet that holds the table.                                       |
| **tableName**      | Query     | `String`  | **Yes**  | Exact name of the table to be converted.                                          |
| **outPath**        | Query     | `String`  | No       | Folder path in Aspose Cloud storage where the HTML file will be saved (optional). |
| **outStorageName** | Query     | `String`  | No       | Storage name for the output file (optional).                                      |
| **fontsLocation**  | Query     | `String`  | No       | Path to a folder containing custom fonts required for the conversion.             |
| **region**         | Query     | `String`  | No       | Locale identifier (e.g., `en-US`, `fr-FR`). Affects number/date formatting.       |
| **password**       | Query     | `String`  | No       | Password to open a protected workbook.                                            |
| **AutoRowsFit**    | Query     | `Boolean` | No       | Auto‑fit all rows in the worksheet (`true`/`false`).                              |
| **AutoColumnsFit** | Query     | `Boolean` | No       | Auto‑fit all columns in the worksheet (`true`/`false`).                           |

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

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

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

> **Note**: For full workbook conversion (not just tables), see [Convert Workbook to HTML](/convert-workbook-to-html/).  
> For a comparison of table vs. range conversion, refer to [Table vs. Range Conversion](/docs/comparison/table-vs-range).