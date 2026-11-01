---
url: /replace-content-in-remote-range/
title: "Replace Text in Remote Range"
linktitle: "Replace Remote Range Content"
type: docs
description: "Replace text in a specific Excel range via Aspose.Cells Cloud API with cloud storage integration"
keywords: "replace text remote excel range, Aspose.Cells Cloud API, find and replace Excel, cloud spreadsheet edit, remote Excel file update"
weight: 100
ArticleTitle: "Replace Text in Remote Excel Range via Aspose.Cells Cloud API"
---
The **ReplaceContentInRemoteRange** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content`) in Aspose.Cells Cloud v4.0 enables precise, bulk text replacement within a specified cell range of a remote Excel file stored in cloud storage—such as AWS S3, Azure Blob, or Google Cloud Storage—without requiring the file to be downloaded locally.

---

## The Replace Content in Remote Range Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### Authentication

All requests require a valid [JWT access token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
curl -X PUT \
  'https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/Sheet1/ranges/A1:D20/replace/content?searchText=OldValue&replaceText=NewValue' \
  -H 'Authorization: Bearer <access_token>'
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The name of the workbook file to be replace. |
| searchText | String | Query | The searched text. |
| replaceText | String | Query | The replaced text. |
| worksheet | String | Path | The worksheet name. |
| cellArea | String | Path | The cell area for the replace. |
| folder | String | Query | The folder path where the workbook is stored. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

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

A successful request returns a `200 OK` status with the following JSON body:


The `CellsCloudResponse` object confirms successful execution. The API does **not** return the count or locations of replacements—only success confirmation.

### Error Codes

| Code | Message      | Cause                                                                         |
| ---- | ------------ | ----------------------------------------------------------------------------- |
| 400  | Bad Request  | Invalid URL, malformed parameters, or unsupported file format.                |
| 401  | Unauthorized | Missing, expired, or invalid access token.                                    |
| 404  | Not Found    | Workbook, worksheet, or specified range does not exist.                       |
| 500  | Server Error | Internal failure during processing (e.g., file corruption, permission error). |

---

### HTTP Request

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
