---
title: "Encrypt, Decrypt, and Digitally Sign Excel Files"
second_title: "Document"
linktitle: "Protect Excel"
type: docs
url: /protect/
aliases: [/workbook/password/]
keywords: "Excel, protect, encrypt, decrypt, digital signature, Aspose.Cells Cloud, REST API, password, security"
description: "Learn how to protect, encrypt, decrypt, and digitally sign Excel workbooks with Aspose.Cells Cloud REST API – code examples for Android, C#, Java, Python and more."
ArticleTitle: "Encrypt, Decrypt, Digitally Sign and Protect Excel Files using Aspose.Cells Cloud API"
weight: 36
---

## **Protecting and un‑protecting Excel files**

**What is “protect” in Aspose.Cells Cloud?**  
The **Protect** operation secures an Excel workbook by applying a password that restricts opening, editing, or modifying the file’s structure. The API also supports encrypting the workbook, decrypting it, and adding a digital signature for tamper‑proof verification.

**API reference**  

| HTTP Method | Endpoint | Required query / body parameters | Sample request body | Typical responses |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (path), `password` (query) | `{ "password": "MySecret123" }` | `200 OK` – protection applied, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (path), `password` (query) | N/A | `200 OK` – protection removed, error codes as above |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (path), `password` (query) | N/A | `200 OK` – file encrypted |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (path), `password` (query) | N/A | `200 OK` – file decrypted |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (path) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – digital signature added |

**Code example (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initialise the API client
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Protect the workbook
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**Prerequisites**  
- An active Aspose.Cells Cloud subscription.  
- `AppSid` and `AppKey` for authentication.  

**Authentication**  
All requests must include the `Authorization` header with a valid JWT token obtained from the Aspose Cloud authentication endpoint.

**Error handling**  
Check the HTTP status code and the `Error` object returned in the response body. Common errors include invalid password (`400`), missing file (`404`), and authentication failures (`401`).

**Notes**  
- The same endpoint can be used to **encrypt** or **decrypt** by changing the action segment (`/encrypt`, `/decrypt`).  
- Digital signatures require a valid certificate file accessible to the API.

- [Encrypt an Excel file with Aspose.Cells Cloud API](/cells/excel-file-encrypt/)
- [Protect an Excel file with Aspose.Cells Cloud API](/cells/protect-excel-file/)
- [Add a digital signature to an Excel file](/cells/excel-digital-signature/)
- [Protect Excel files – detailed guide](/cells/protect-excel-files/)
- [Set a password for an Excel file](/cells/workbook/password/modify/)
- [Decrypt an Excel file](/cells/excel-file-decrypt/)
- [Unprotect an Excel file](/cells/excel-file-unprotect/)
- [Unlock Excel files](/cells/unlock-excel-files/)
- [Clear the password of an Excel file](/cells/clear-excel-files-password/)