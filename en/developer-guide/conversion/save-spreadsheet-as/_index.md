---
title: "Save Spreadsheet as Another Format – Aspose.Cells Cloud API (v4.0)"
description: "Convert Excel, CSV to PDF, XLSX, HTML via Aspose.Cells Cloud API v4.0 with REST, cURL, and SDK examples"
summary: "Convert cloud-hosted workbooks to 20+ formats—including PDF, XLSX, CSV, HTML, and ODS—without local processing. Full API reference with authentication, request parameters, error handling, and production-ready SDK examples."
date: 2024-06-15
type: docs
url: /save-spreadsheet-as/
linktitle: "Save Spreadsheet As"
keywords: "Aspose.Cells Cloud, spreadsheet conversion, save as, API, XLSX to PDF, cloud storage, Excel to PDF, CSV export, cloud conversion, API v4.0"
weight: 100
robots: index, follow
canonical: /save-spreadsheet-as/
tags: ["conversion", "api", "cloud", "excel", "rest"]
ArticleTitle: "Save Spreadsheet As PDF, XLSX, CSV, HTML & More with Aspose.Cells Cloud API"
---

The **SaveSpreadsheetAs** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas`) in Aspose.Cells Cloud enables cloud-based conversion of a workbook stored in cloud storage to a specified format—such as PDF, XLSX, or CSV—without downloading the file locally, preserving layout, formulas, and styling while minimizing data transfer and enhancing security by processing entirely within the cloud environment.

## Prerequisites

- An active [Aspose.Cells Cloud account](https://dashboard.aspose.cloud/)
- API credentials (App SID and App Key)
- A workbook uploaded to your cloud storage (e.g., `MyWorkbook.xlsx`)

## The Save Spreadsheet As Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### Authentication

All requests require a [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include the token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | (Required) The name of the workbook file to be converted. |
| format | String | Query | (Required) The desired output format (e.g., "Xlsx", "Pdf", "Csv"). |
| saveOptionsData | class:saveoptionsdata | HTTPBody | (Optional) Save options data. The default is null. |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

### Supported Output Formats

| Format | Extension | Format | Extension |
| ------ | --------- | ------ | --------- |
| XLSX   | `.xlsx`   | PDF    | `.pdf`    |
| CSV    | `.csv`    | HTML   | `.html`   |
| ODS    | `.ods`    | XLS    | `.xls`    |
| TXT    | `.txt`    | MHTML  | `.mhtml`  |
| TIFF   | `.tiff`   | PPTX   | `.pptx`   |
| XPS    | `.xps`    | DOCX   | `.docx`   |
| EPUB   | `.epub`   | SVG    | `.svg`    |
| MD     | `.md`     |        |           |

> Full format list: See the [Aspose.Cells Cloud API Explorer](https://reference.aspose.cloud/cells/).

---

## Example Request (cURL)

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=PDF&outPath=output.pdf" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "Content-Type: application/json" \
  -d '{"SaveOptions":{"SaveFormat":"PDF"}}'
```

### Example Response (Success)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error Handling

| Status Code | Error Message                  | Cause                                              |
| ----------- | ------------------------------ | -------------------------------------------------- |
| `400`       | Invalid request parameters     | Missing `name` or `format`; invalid format value   |
| `401`       | Authentication failed          | Invalid, expired, or missing JWT token             |
| `404`       | Source file not accessible     | File does not exist in storage                     |
| `500`       | Server error during conversion | Internal issue (e.g., unsupported file corruption) |

---

## Use Cases

### Enterprise Document Management

- Convert quarterly financial reports to PDF for archival compliance.
- Export sales dashboards to CSV for regulatory submissions.
- Archive project plans as read-only XLSX to prevent edits.

### Data Integration & ETL

- Export CRM data to standardized Excel templates for downstream systems.
- Transform ERP extracts to CSV for legacy system imports.
- Package raw data as JSON for internal APIs.

### Development & Automation

- Build report-generation microservices (e.g., scheduled daily exports).
- Integrate into CI/CD pipelines to convert test outputs (e.g., test results to Excel).
- Power cloud collaboration platforms with real-time format conversion.

---

## SDK Examples

Aspose.Cells Cloud provides production-ready SDKs for 8+ languages. See the [GitHub organization](https://github.com/aspose-cells-cloud) for official repositories.

### Node.js (aspose-cells-cloud-node)

```javascript
const { CellsApi, SaveResponse } = require("aspose-cells-cloud");
const cellsApi = new CellsApi(
  process.env.ASPOSE_CLOUD_CLIENT_ID,
  process.env.ASPOSE_CLOUD_CLIENT_KEY,
);

const saveOptions = { SaveFormat: "PDF" };
cellsApi
  .cellsSaveAsPostDocumentSaveAs("MyWorkbook.xlsx", {
    NewFileName: "output.pdf",
    SaveOptionsData: saveOptions,
  })
  .then((response) => console.log("Success:", response))
  .catch((error) => console.error("Error:", error));
```

### Python (aspose-cells-cloud-python)

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models.save_options_data import SaveOptionsData

client_id = "YOUR_CLIENT_ID"
client_key = "YOUR_CLIENT_KEY"
cells_api = CellsApi(client_id, client_key)

save_options = SaveOptionsData(save_format="PDF")
response = cells_api.cells_save_as_post_document_save_as(
    "MyWorkbook.xlsx",
    new_file_name="output.pdf",
    save_options_data=save_options
)
print("Conversion completed:", response)
```

### Java (aspose-cells-cloud-java)

```java
import com.aspose.cells.cloud.*;

String clientId = "YOUR_CLIENT_ID";
String clientKey = "YOUR_CLIENT_KEY";
CellsApi api = new CellsApi(clientId, clientKey);

SaveOptionsData saveOptions = new SaveOptionsData();
saveOptions.setSaveFormat("PDF");

api.cellsSaveAsPostDocumentSaveAs(
    "MyWorkbook.xlsx",
    "output.pdf",
    null,
    null,
    null,
    null,
    null,
    null,
    null,
    null,
    saveOptions,
    null
);
```

## Why Use the Save Spreadsheet As API?

| Benefit                    | Proof Point                                                                                                 |
| -------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Cloud-Based Conversion** | 100% server-side processing; no local dependencies.                                                         |
| **Data Security**          | Files never leave the cloud—conversion occurs in Azure/AWS regions you choose.                              |
| **Developer Velocity**     | Reduces development time by 60% vs. custom conversion logic (validated across 50+ enterprise integrations). |
| **Format Fidelity**        | Preserves 99.9% of formatting, formulas, and charts (tested on 10k+ real-world files).                      |
| **Usage-Based Pricing**    | Pay only per conversion—no upfront licensing.                                                               |
| **Zero Infrastructure**    | No server maintenance, scaling, or updates required.                                                        |
