---
title: "File Info"
second_title: "Document"
linktitle: "File Info"
type: docs
url: /file-info/
keywords: "File Info, Excel file metadata, Base64 file content, Aspose.Cells Cloud API"
description: "Get Excel file name, size, and Base64 content via Aspose.Cells Cloud API. Learn request syntax, sample code, and error handling."
weight: 79
---

# FileInfo Properties

## Overview
The **FileInfo** endpoint returns metadata for a workbook stored in Aspose.Cells Cloud, including its name, size, and the entire file content encoded in Base64. Use this endpoint when you need to inspect a file or download its raw data without opening it in the cloud.

## Request
| Element | Value |
|---------|-------|
| **Method** | `GET` |
| **Endpoint** | `/cells/fileInfo/{path}` |
| **Path Parameter** | `path` – Full storage path of the target Excel file (e.g., `folder1/report.xlsx`). |
| **Authentication** | OAuth2 / JWT token supplied in the `Authorization` header. |

### Sample Requests
#### cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/fileInfo/folder1/report.xlsx" \
     -H "Authorization: Bearer {access_token}"
```

#### PowerShell
```powershell
Invoke-RestMethod -Method Get `
    -Uri "https://api.aspose.cloud/v3.0/cells/fileInfo/folder1/report.xlsx" `
    -Headers @{ Authorization = "Bearer $accessToken" }
```

#### .NET (Aspose.Cells Cloud SDK)
```csharp
var apiInstance = new CellsApi("client_id", "client_secret");
FileInfoResponse result = apiInstance.GetFileInfo("folder1/report.xlsx");
Console.WriteLine($"Name: {result.FileName}");
Console.WriteLine($"Size: {result.FileSize} bytes");
```

## Response
A successful call returns a JSON object containing the three properties listed below.

```json
{
  "FileName": "report.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQAAAAAAAAAAAAAAAAAJABwAd29ya2JvbG..."
}
```

*`FileContent` is a Base64‑encoded string that represents the raw Excel file. Decode it to obtain the binary workbook.*

## FileInfo Properties

| Name         | Type   | Description                                                                |
|--------------|--------|----------------------------------------------------------------------------|
| **FileName** | string | The name of the file, including its extension.                            |
| **FileSize** | long   | The size of the file in bytes.                                            |
| **FileContent** | string | Contains the raw Excel file data encoded in Base64.                       |

## Prerequisites
- A valid Aspose.Cells Cloud account with an active **OAuth2/JWT** access token.  
- The target Excel file must already exist in Aspose Cloud storage.  

## Errors
| HTTP Code | Meaning                     | When It Occurs |
|-----------|-----------------------------|----------------|
| 200       | OK – request succeeded.    | Normal response. |
| 401       | Unauthorized                | Missing or invalid authentication token. |
| 404       | Not Found                   | The specified file does not exist. |
| 500       | Internal Server Error       | Unexpected server‑side failure. |

## Version / Compatibility
The endpoint is supported in **Aspose.Cells Cloud v23.12** and later. Consult the [release notes](https://docs.aspose.cloud/cells/release-notes/) for any breaking changes.

## See Also
- [Get Workbook](https://docs.aspose.cloud/cells/get-workbook)  
- [Download File](https://docs.aspose.cloud/cells/download-file)  
- [Authentication Overview](https://docs.aspose.cloud/cells/authentication)  

---