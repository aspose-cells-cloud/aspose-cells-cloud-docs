---
title: "Encrypt, Decrypt, and Digitally Sign Excel Files"
second_title: "Developer Guide"
linktitle: "Protect Excel"
type: docs
url: /protect/
aliases: [/workbook/password/]
keywords: "Excel, protect, encrypt, decrypt, digital signature, Aspose.Cells Cloud, REST API, password, security"
description: "Encrypt, decrypt, protect, and sign Excel files with Aspose.Cells Cloud API using passwords or certificates"
ArticleTitle: "Encrypt, Decrypt, Digitally Sign and Protect Excel Files using Aspose.Cells Cloud API"
weight: 36
---

## **Protecting and un‑protecting Excel files**

**What is “protect” in Aspose.Cells Cloud?**  
The **Protect** operation secures an Excel workbook by applying a password that restricts opening, editing, or modifying the file’s structure. The API also supports encrypting the workbook, decrypting it, and adding a digital signature for tamper‑proof verification.

- [Encrypt an Excel file with Aspose.Cells Cloud API](/cells/excel-file-encrypt/)
- [Protect an Excel file with Aspose.Cells Cloud API](/cells/protect-excel-file/)
- [Add a digital signature to an Excel file](/cells/excel-digital-signature/)
- [Protect Excel files – detailed guide](/cells/protect-excel-files/)
- [Set a password for an Excel file](/cells/workbook/password/modify/)
- [Decrypt an Excel file](/cells/excel-file-decrypt/)
- [Unprotect an Excel file](/cells/excel-file-unprotect/)
- [Unlock Excel files](/cells/unlock-excel-files/)
- [Clear the password of an Excel file](/cells/clear-excel-files-password/)
 
**API reference**

| HTTP Method | Endpoint                                                   | Required query / body parameters      | Sample request body                                                             | Typical responses                                                                                 |
| ----------- | ---------------------------------------------------------- | ------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| POST        | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect`   | `fileName` (path), `password` (query) | `{ "password": "MySecret123" }`                                                 | `200 OK` – protection applied, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST        | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (path), `password` (query) | N/A                                                                             | `200 OK` – protection removed, error codes as above                                               |
| POST        | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt`   | `fileName` (path), `password` (query) | N/A                                                                             | `200 OK` – file encrypted                                                                         |
| POST        | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt`   | `fileName` (path), `password` (query) | N/A                                                                             | `200 OK` – file decrypted                                                                         |
| POST        | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign`      | `fileName` (path)                     | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – digital signature added                                                                |
