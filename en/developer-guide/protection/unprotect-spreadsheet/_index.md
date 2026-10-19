---
title: "Aspose.Cells Cloud Unprotect Spreadsheet API"
linktitle: "Unprotect Spreadsheet"
description: "Programmatically remove open and modify passwords from Excel files (.xlsx, .xls) using Aspose.Cells Cloud API. Supports OAuth2 authentication, batch processing, and secure cloud-based unprotection."
tags:
  [
    "unprotect",
    "excel",
    "password",
    "security",
    "rest-api",
    "oauth2",
    "batch-processing",
  ]
categories: ["aspose.cells.cloud", "api-reference"]
weight: 100
type: docs
---

# Aspose.Cells Cloud Unprotect Spreadsheet API

Remove both open and modify password protection from Excel workbooks programmatically with the Aspose.Cells Cloud Unprotect Spreadsheet API. This secure, server-side operation enables automated unlocking of protected files in data pipelines, document management systems, and migration workflows—without exposing sensitive passwords client-side.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

> **Note**: This API is part of Aspose.Cells Cloud v4.0. Verify compatibility if migrating from earlier versions. Aspose.Cells Cloud v5.0 may introduce breaking changes—see [API Versioning Guide](https://docs.aspose.cloud/total/getting-started/overview/api-versioning/) for details.

---

## Authentication

All requests require a valid JWT access token issued via OAuth2. For implementation guidance, see [Authentication Overview](https://docs.aspose.cloud/total/security/authenticating-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Request Parameters

| Parameter Name   | Type   | Location | Required | Description                                                                                                                                         |
| ---------------- | ------ | -------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Spreadsheet`    | File   | FormData | ✅ Yes   | The Excel file to unprotect. Supported formats: `.xlsx`, `.xls`, `.xlsm`, `.xlsb`.                                                                  |
| `password`       | String | Query    | ✅ Yes   | Password required to open the workbook. Omit only if no open password is set.                                                                       |
| `modifyPassword` | String | Query    | ✅ Yes   | Password required to modify the workbook (e.g., edit, format, insert rows).                                                                         |
| `outPath`        | String | Query    | ❌ No    | Full path (including filename) where the unprotected file will be saved (e.g., `/output/unprotected.xlsx`). Defaults to response stream if omitted. |
| `outStorageName` | String | Query    | ❌ No    | Name of the cloud storage (e.g., `First Aspose Cloud Storage`). Required if `outPath` is specified.                                                 |
| `region`         | String | Query    | ❌ No    | Locale setting (e.g., `en-US`, `fr-FR`). Affects date/number formatting. Default: `en-US`.                                                          |

> **Best Practice**: Always specify `outPath` and `outStorageName` for production workflows to avoid large response payloads. Store unprotected files directly in your cloud storage.

---

## Response

On success, returns the unprotected workbook as a file stream. The response payload contains the file content in binary format.

### Sample Response (Success: 200 OK)

```
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet
Content-Disposition: attachment; filename="unprotected.xlsx"
[Binary Excel content]
```

### HTTP Status Codes

| Code | Meaning               | Description                                                                     |
| ---- | --------------------- | ------------------------------------------------------------------------------- |
| 200  | OK                    | Unprotection successful. File returned in response body.                        |
| 400  | Bad Request           | Missing/invalid parameters (e.g., unsupported file format, malformed password). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token.                                         |
| 404  | Not Found             | Source file not found in storage (if referenced).                               |
| 413  | Payload Too Large     | Uploaded file exceeds 2 GB limit.                                               |
| 500  | Internal Server Error | Server error during processing (e.g., corrupted file, resource exhaustion).     |

---

## Key Features & Benefits

- **Dual-Layer Protection Removal**: Strip both open and modify passwords in a single API call.
- **Secure Processing**: Passwords are processed server-side and never exposed in logs or responses.
- **Batch Support**: Integrate with storage APIs to process hundreds of files via automation.
- **Flexible Output**: Retrieve files directly or save to cloud storage for downstream use.
- **Cross-Platform SDKs**: Pre-built wrappers for C#, Java, Python, Node.js, PHP, Ruby, Perl, and Go.

---

## Usage Examples

### cURL Command

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass&outPath=/output/unprotected.xlsx&outStorageName=First Aspose Cloud Storage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
```

> **Tip**: Replace `{access_token}` with your JWT token. Ensure `myfile.xlsx` contains both passwords set.

### Aspose.Cells Cloud SDK (C#)

```csharp
using Aspose.Cells.Cloud.Sdk;

var configuration = new Configuration
{
    AppSid = "your_app_sid",
    AppKey = "your_app_key"
};

var cellsApi = new CellsApi(configuration);

// Upload file to cloud storage first (if needed)
var fileStream = File.OpenRead("protected.xlsx");
cellsApi.UploadFile("protected.xlsx", fileStream);

// Unprotect and save
var response = cellsApi.CellsUnprotectSpreadsheet(
    name: "protected.xlsx",
    password: "OldPass",
    modifyPassword: "ModPass",
    outPath: "/output/unprotected.xlsx",
    storage: "First Aspose Cloud Storage"
);

Console.WriteLine($"Unprotected file saved to: {response.Path}");
```

> **SDK Support**: See [Aspose.Cells Cloud SDKs](https://github.com/aspose-cells-cloud) for language-specific implementations. All SDKs handle JWT token management and request/response serialization.

---

## Error Handling

### Common Scenarios & Fixes

| Error                   | Cause                                  | Resolution                                                              |
| ----------------------- | -------------------------------------- | ----------------------------------------------------------------------- |
| `400 Bad Request`       | Missing `password` or `modifyPassword` | Provide both passwords—even if one is empty, pass an empty string `""`. |
| `400 Bad Request`       | Unsupported file format                | Ensure input is `.xlsx`, `.xls`, `.xlsm`, or `.xlsb`.                   |
| `404 Not Found`         | Source file missing                    | Verify `name` matches an existing file in storage.                      |
| `413 Payload Too Large` | File > 2 GB                            | Split large files or use chunked upload + storage APIs first.           |
| `500 Server Error`      | Corrupted file                         | Validate file integrity before upload.                                  |
