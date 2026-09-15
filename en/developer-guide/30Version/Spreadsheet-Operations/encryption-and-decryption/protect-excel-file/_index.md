---
title: "Protect an Excel Workbook Using Aspose.Cells Cloud API"
description: "Secure your Excel workbook with Aspose.Cells Cloud REST API v3.0. Learn to apply password protection and restrict editing (structure, windows, contents) via cURL or SDKs (C#, Java, Python, etc.). Includes full request/response examples."
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-22T14:30:00Z
draft: false
tags: ["excel-protection", "rest-api", "aspose.cells", "security", "v3.0"]
categories: ["cloud-api", "workbook"]
weight: 30
ArticleTitle: "Protect an Excel Workbook Using Aspose.Cells Cloud API"
linktitle: "Protect an Excel File"
type: docs
url: /protect-excel-file/
aliases: [/protect-excel-workbooks/, /workbook/protect/]
---

This REST API **protects** an Excel workbook, enabling you to securely protect an Excel workbook with password and protection options using Aspose.Cells Cloud.

### Security Notice
**⚠️ Security Note**: Replace `test.xlsx`, `MyFolder`, `MyStorage`, and `aspose` with your actual file path, storage name, and a *strong, unique password*.

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Query Parameters

| Parameter Name | Type   | Description                                                     |
| -------------- | ------ | --------------------------------------------------------------- |
| folder         | string | Folder that contains the source workbook. _(optional)_          |
| storageName    | string | Name of the storage location. _(optional; default = "Default")_ |

### Request Body Parameters

| Parameter Name | Type                      | Description                                                   |
| -------------- | ------------------------- | ------------------------------------------------------------- |
| protection     | WorkbookProtectionRequest | Object that defines the protection settings for the workbook. |

#### WorkbookProtectionRequest

| Parameter Name | Type   | Description                                                                                                                                              |
| -------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType | string | Type of protection to apply. Allowed values (case‑insensitive): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password       | string | Optional password to set for the protection.                                                                                                             |

### Response

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Protection applied successfully.                |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

## How to Use the PostProtectDocument API with SDKs

### Prerequisites

Before calling the API, ensure you have completed the following steps:

- **Obtain a JWT access token** using the <a href="/rest-api/auth/" rel="noopener noreferrer">authentication flow</a>.  
- **Upload the workbook** to your Aspose Cloud storage or confirm it already exists in the target folder.  
- **Know the storage name** (default is `"Default"` if not specified) and the exact file name you wish to protect.

### PostProtectDocument API Specification

The <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Example: Protect a Workbook with cURL

1. Obtain an access token as described in **Prerequisites / Authentication**.  
2. Execute the request:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   The response will include a status object confirming the protection succeeded.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the most efficient way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details, allowing you to focus on your business logic. See the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud SDKs repository on GitHub</a> for a complete list of supported SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Sample Full Response

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```