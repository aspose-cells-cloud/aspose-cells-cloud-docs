---
title: "Aspose.Cells Cloud Web API – Set / Modify Open Password for Excel Files"
second_title: "Comprehensive Developer Guide"
ArticleTitle: "Spreadsheet Protection – Set Open Password and Modify Password"
linktitle: "Protection"
type: docs
url: /protection/
keywords: "Aspose.Cells Cloud API, spreadsheet protection, open password, read‑write password, Excel security"
description: "Learn how to protect an Excel workbook with an open or read‑write password using Aspose.Cells Cloud REST API. Includes request syntax, code samples, and error handling."
weight: 60
---

In this guide, you will learn how to set, modify, and remove both the open password and the read‑write password for spreadsheets using the Aspose.Cells Cloud Web API. These features protect sensitive data in the document.

**API reference**  
- **Endpoint:** `PUT https://api.aspose.cloud/v3.0/cells/{fileName}/protection`  
- **Method:** `PUT` (or `POST` depending on your SDK)  
- **Path parameters:**  
  - `fileName` – Name of the workbook (including extension).  
  - `folder` – (optional) Path to the folder in storage.  
  - `storage` – (optional) Storage name.  
- **Query parameters:**  
  - `password` – Current open password (required when modifying or removing).  
  - `newPassword` – New open password to set.  
  - `newReadOnlyPassword` – New read‑write password to set.  
- **Request body (JSON):**  

```json
{
  "Password": "currentOpenPassword",
  "NewPassword": "newOpenPassword",
  "NewReadOnlyPassword": "newReadWritePassword"
}
```

- **Successful response (JSON):**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Protection": {
    "IsProtected": true,
    "Password": "newOpenPassword",
    "ReadOnlyPassword": "newReadWritePassword"
  }
}
```

- **Common status codes:**  
  - `200` – Password applied or updated successfully.  
  - `400` – Invalid request parameters.  
  - `401` – Authentication failed.  
  - `404` – Specified workbook not found.  
  - `500` – Server error.

**Prerequisites**  
- Valid Aspose Cloud authentication token (JWT or OAuth2) must be included in the `Authorization` header.  
- The workbook must be stored in Aspose Cloud storage or provided as a multipart upload.

- **[Protect the Spreadsheet with password](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Unprotect the Spreadsheet with password](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  