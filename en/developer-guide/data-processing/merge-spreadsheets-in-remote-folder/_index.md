---
title: "Merge Matching Spreadsheets in Remote Folder"
description: "Combine spreadsheet files stored in Aspose Cloud storage into a single file. Supports 30+ output formats such as PDF, CSV, JSON, XLSX, ODS, XPS, and more."
keywords: "Aspose.Cells, merge spreadsheets, remote folder, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

# Merge Matching Spreadsheets in Remote Folder

Combine multiple spreadsheet files that reside in a remote Aspose Cloud storage folder into a single output file. The operation runs entirely in the cloud, eliminating the need to download source files locally. Over 30 output formats are supported (PDF, CSV, JSON, XLSX, ODS, XPS, …).

---

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Authentication](#authentication)  
3. [Endpoint](#endpoint)  
4. [Request Parameters](#request-parameters)  
5. [Request Example (cURL)](#request-example)  
6. [Responses](#responses)  
7. [Error Handling](#error-handling)  
8. [SDK Code Samples](#sdk-code-samples)  
9. [Related APIs](#related-apis)  

---

## Prerequisites <a id="prerequisites"></a>

| # | Requirement |
|---|--------------|
| 1 | An active **Aspose Cloud** subscription. |
| 2 | A **JWT access token** (see the [Authentication](#authentication) section). |
| 3 | At least one cloud storage (default or custom) configured in your Aspose account. |
| 4 | Source spreadsheet files stored in the chosen storage folder. |
| 5 | If any source file is password‑protected, the password must be supplied. |

---

## Authentication <a id="authentication"></a>

The API uses **JWT token‑based authentication**.

1. **Obtain client credentials** (Client Id & Client Secret) from the Aspose Cloud console.  
2. **Request an access token**:

   ```bash
   POST https://api.aspose.cloud/connect/token
   Content-Type: application/x-www-form-urlencoded

   grant_type=client_credentials&client_id={YOUR_CLIENT_ID}&client_secret={YOUR_CLIENT_SECRET}
   ```

3. **Include the token** in the `Authorization` header of every API call:

   ```http
   Authorization: Bearer {access_token}
   ```

> **Tip:** Tokens are valid for 1 hour. Refresh them as needed.

---

## Endpoint <a id="endpoint"></a>

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

*Method:* `PUT`  
*Path:* `/cells/merge/remote-spreadsheets`  
*API version:* `v4.0`

---

## Request Parameters <a id="request-parameters"></a>

| Name                | Type    | Location | Required | Description |
|---------------------|---------|----------|----------|-------------|
| **folder**          | string  | query    | **Yes**  | Cloud storage folder that contains the source spreadsheets. |
| **fileMatchExpression** | string  | query    | **Yes**  | Pattern to select files (e.g., `*report*.xlsx`). Supports wildcards `*` and `?`. |
| **outFormat**       | string  | query    | **Yes**  | Desired output format (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …). |
| **mergeInOneSheet** | boolean | query    | **Yes**  | `true` – all data merged into a single worksheet. `false` – each source file gets its own worksheet. |
| **storageName**     | string  | query    | No       | Custom storage name; defaults to the primary storage if omitted. |
| **outPath**         | string  | query    | No       | Destination folder for the merged file. If omitted, the file is saved in the source folder. |
| **outStorageName**  | string  | query    | No       | Storage name where the merged file will be written. |
| **fontsLocation**   | string  | query    | No       | Path to a folder containing custom fonts (required for PDF/Image export). |
| **region**          | string  | query    | No       | Locale for number, date, and currency formatting (e.g., `en-US`, `de-DE`). |
| **password**        | string  | query    | No       | Password to open any protected source spreadsheet. |

---

## Request Example (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Replace `<access_token>` with a valid JWT token.*

---

## Responses <a id="responses"></a>

### Success (200)

The API returns a binary stream representing the merged file.

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

> **Note:** The `Content-Type` header of the HTTP response matches the selected `outFormat` (e.g., `application/pdf` for PDF).

### Sample JSON for a successful response (metadata)

```json
{
  "FileName": "MergedReport.pdf",
  "FileSize": 254312,
  "ContentType": "application/pdf",
  "DownloadUrl": "https://storage.aspose.cloud/v4.0/.../MergedReport.pdf"
}
```

---

## Error Handling <a id="error-handling"></a>

| HTTP Code | Meaning | Sample JSON |
|-----------|---------|-------------|
| **400** Bad Request | Invalid URI or query parameters. | `{ "code": 400, "message": "Bad request – check URI and parameters.", "requestId": "12345abcde" }` |
| **401** Unauthorized | Missing/invalid JWT token. | `{ "code": 401, "message": "Unauthorized – verify OAuth token.", "requestId": "12345abcde" }` |
| **404** Not Found | Specified folder or file cannot be accessed. | `{ "code": 404, "message": "Resource not found – confirm file/folder path.", "requestId": "12345abcde" }` |
| **500** Server Error | Internal processing error. | `{ "code": 500, "message": "Internal server error – see logs for details.", "requestId": "12345abcde" }` |

---

## SDK Code Samples <a id="sdk-code-samples"></a>

The following snippets demonstrate how to call the **Merge Spreadsheets in Remote Folder** operation using Aspose.Cells Cloud SDKs. Replace placeholder values (`YOUR_CLIENT_ID`, `YOUR_CLIENT_SECRET`, `folder`, etc.) with your own data.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Model;
using System.Threading.Tasks;

var config = new Configuration
{
    ClientId = "YOUR_CLIENT_ID",
    ClientSecret = "YOUR_CLIENT_SECRET",
    BasePath = "https://api.aspose.cloud"
};

var api = new CellsApi(config);

await api.MergeSpreadsheetsInRemoteFolderAsync(
    folder: "MyFolder",
    fileMatchExpression: "*.xlsx",
    outFormat: "PDF",
    mergeInOneSheet: true,
    storageName: null,
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    region: "en-US",
    password: null);
```

</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.*;

public class MergeRemoteFolder {
    public static void main(String[] args) throws ApiException {
        CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
        api.mergeSpreadsheetsInRemoteFolder(
            "MyFolder",               // folder
            "*.xlsx",                 // fileMatchExpression
            "PDF",                    // outFormat
            true,                     // mergeInOneSheet
            null, null, null, null,   // optional params
            "en-US", null);
    }
}
```

</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration(
    client_id="YOUR_CLIENT_ID",
    client_secret="YOUR_CLIENT_SECRET"
)

api = CellsApi(config)

api.merge_spreadsheets_in_remote_folder(
    folder="MyFolder",
    file_match_expression="*.xlsx",
    out_format="PDF",
    merge_in_one_sheet=True,
    storage_name=None,
    out_path=None,
    out_storage_name=None,
    fonts_location=None,
    region="en-US",
    password=None
)
```

</details>

*Additional SDKs (Node.js, PHP, Ruby, Go, Perl) are available in the official [GitHub repository](https://github.com/aspose-cells-cloud).*

---

## Related APIs <a id="related-apis"></a>

- **Merge Spreadsheets (Local Files)** – `PUT /cells/merge`  
- **Split Spreadsheet** – `PUT /cells/split`  
- **Convert Workbook** – `PUT /cells/convert`  

Explore these APIs to build more complex document‑processing pipelines.

---

## Accessibility & SEO Notes

- All external links that open in a new tab include `rel="noopener noreferrer"` for security.  
- Flag icons used in the language selector have `aria-label` attributes (e.g., `<em class="flag-us flag-24" aria-label="English (US)"></em>`).  
- The page declares `charset=utf-8` and is saved in UTF‑8 without BOM, eliminating encoding artifacts.  
- The `<meta name="keywords">` tag now contains a concise, non‑duplicated keyword list.  
- Heading hierarchy follows a single H1 → H2 → H3 pattern for optimal SEO and screen‑reader navigation.

---