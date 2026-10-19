---
url: /replace-content-in-remote-range/
title: "Replace Text in Remote Range"
linktitle: "Replace Remote Range Content"
type: docs
description: "Use Aspose.Cells Cloud API to find and replace text within a specified range of a remote Excel file stored in cloud storage. Supports authentication, error handling, and multi-language SDK integration."
keywords: "replace text remote excel range, Aspose.Cells Cloud API, find and replace Excel, cloud spreadsheet edit, remote Excel file update"
weight: 100
---

Perform bulk text replacement across remote Excel files stored in cloud storage such as AWS S3, Azure Blob Storage, or Google Cloud Storage. This API enables precise find-and-replace operations within a defined cell range of a worksheet without downloading the file.

---

## Replace Text in Remote Range API

### HTTP Request

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### Request Parameters

| Parameter Name | Type   | Location | Required | Description                                                                                  |
| -------------- | ------ | -------- | -------- | -------------------------------------------------------------------------------------------- |
| `name`         | string | Path     | Yes      | The name of the workbook file stored in cloud storage (e.g., `"report.xlsx"`).               |
| `worksheet`    | string | Path     | Yes      | The name of the worksheet where the replacement will occur.                                  |
| `cellArea`     | string | Path     | Yes      | The cell range (e.g., `"A1:D20"`) in which text will be searched and replaced.               |
| `searchText`   | string | Query    | Yes      | The exact text string to search for within the specified range.                              |
| `replaceText`  | string | Query    | Yes      | The text string that replaces all occurrences of `searchText`.                               |
| `folder`       | string | Query    | No       | The cloud storage folder path where the workbook resides.                                    |
| `storageName`  | string | Query    | No       | _(Optional)_ The name of a custom cloud storage. If omitted, the default storage is used.    |
| `region`       | string | Query    | No       | _(Optional)_ Locale identifier (e.g., `"en-US"`, `"fr-FR"`) affecting text comparison rules. |
| `password`     | string | Query    | No       | _(Optional)_ Password to open a password-protected workbook.                                 |

### Authentication

All requests require a valid [JWT access token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
curl -X PUT \
  'https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/Sheet1/ranges/A1:D20/replace/content?searchText=OldValue&replaceText=NewValue' \
  -H 'Authorization: Bearer <access_token>'
```

### Response

A successful request returns a `200 OK` status with the following JSON body:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

The `CellsCloudResponse` object confirms successful execution. The API does **not** return the count or locations of replacements—only success confirmation.

### Error Codes

| Code | Message      | Cause                                                                         |
| ---- | ------------ | ----------------------------------------------------------------------------- |
| 400  | Bad Request  | Invalid URL, malformed parameters, or unsupported file format.                |
| 401  | Unauthorized | Missing, expired, or invalid access token.                                    |
| 404  | Not Found    | Workbook, worksheet, or specified range does not exist.                       |
| 500  | Server Error | Internal failure during processing (e.g., file corruption, permission error). |

---

## Use Cases

- **Template Content Updates**: Dynamically replace placeholder text in cloud-hosted Excel templates (e.g., quarterly reports, invoices).
- **Batch Data Standardization**: Standardize text across multiple Excel files in cloud storage (e.g., region-specific currency or unit labels).
- **Cross-Region Deployment**: Synchronize content consistency for Excel files deployed across regions while respecting locale settings.
- **Automated Reporting Pipelines**: Integrate into CI/CD workflows to inject runtime values into Excel reports stored in object storage.

---

## Implementation Examples

### OpenAPI Specification

A stable, versioned OpenAPI specification for this operation is available at:  
[https://docs.aspose.cloud/cells/specification/22.12/](https://docs.aspose.cloud/cells/specification/22.12/)  
_(Note: Replace `22.12` with the latest stable version as needed.)_

### SDK Examples

Aspose.Cells Cloud provides SDKs for major programming languages. The SDKs handle authentication, serialization, and request routing—minimizing boilerplate.

#### C#

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var cellsApi = new CellsApi("client_id", "client_secret");

var name = "report.xlsx";
var worksheet = "Sheet1";
var cellArea = "A1:D20";
var searchText = "Q1";
var replaceText = "Q2";
var folder = "input";
var storage = null;

var response = cellsApi.CellsRangesPutReplaceContent(
    name, worksheet, cellArea, searchText, replaceText, folder: folder, storage: storage);

Console.WriteLine($"Status: {response.Code}, Message: {response.Status}");
```

#### Java

```java
import com.aspose.cells.cloud.*;

ApiClient apiClient = new ApiClient("client_id", "client_secret", null);
CellsApi cellsApi = new CellsApi(apiClient);

String name = "report.xlsx";
String worksheet = "Sheet1";
String cellArea = "A1:D20";
String searchText = "Q1";
String replaceText = "Q2";
String folder = "input";

CellsRangesPutReplaceContentResponse response = cellsApi.cellsRangesPutReplaceContent(
    name, worksheet, cellArea, searchText, replaceText, folder, null, null, null);

System.out.println("Status: " + response.getCode() + " - " + response.getStatus());
```

#### Python

```python
from asposecellscloud.api import CellsApi
from asposecellscloud.configuration import Configuration

config = Configuration(client_id="client_id", client_secret="client_secret")
api = CellsApi(config)

name = "report.xlsx"
worksheet = "Sheet1"
cell_area = "A1:D20"
search_text = "Q1"
replace_text = "Q2"
folder = "input"

response = api.cells_ranges_put_replace_content(
    name, worksheet, cell_area, search_text, replace_text, folder=folder)

print(f"Status: {response.code} - {response.status}")
```
