---
title: "Compress and Repair Excel Files"
second_title: "Document"
type: docs
url: /compress-and-repair-excel-files/
linktitle: "Compress and Repair"
keywords: "Aspose.Cells, Excel compression, Excel repair, cloud API, reduce Excel file size, restore corrupted workbook, compress Excel file, repair Excel workbook"
description: "Learn how to compress large Excel workbooks and repair corrupted files using Aspose.Cells Cloud API. Step‑by‑step examples, supported languages, and best practices."
weight: 100
ArticleTitle: "Compress and Repair Excel Files – Aspose.Cells Cloud API"
---

Compressing an Excel workbook reduces its file size by removing unused styles, images, and shared strings, while repairing restores the integrity of corrupted workbooks. Aspose.Cells Cloud API provides dedicated endpoints for both operations.

- **[Compress the data in an Excel file](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Repair Excel Files](https://docs.aspose.cloud/cells/repair-excel-files/).**

**Compress Workbook API**  
The **Compress** operation uses a simple POST request. Below is a complete request/response specification:

| Method | Endpoint | Required Parameters | Request Body | Sample Response | Typical Status Codes |
|--------|----------|---------------------|--------------|-----------------|----------------------|
| POST   | `/cells/compress` | `file` (binary) – the workbook to compress; optional `outPath` (string) – destination path | *None* (file is sent as multipart/form‑data) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**Repair Workbook API**  
The **Repair** operation also uses a POST request. Its specification is:

| Method | Endpoint | Required Parameters | Request Body | Sample Response | Typical Status Codes |
|--------|----------|---------------------|--------------|-----------------|----------------------|
| POST   | `/cells/repair` | `file` (binary) – the corrupted workbook; optional `outPath` (string) – where to save the repaired file | *None* (file is sent as multipart/form‑data) | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

These tables provide developers with the essential details needed to call the APIs directly without navigating elsewhere.

**Additional Resources**  
- See the full **[Compress Excel Files](/compress-excel-files/)** guide for advanced options such as removing unused rows and columns.  
- Review the **[Repair Excel Files](/repair-excel-files/)** documentation for troubleshooting tips and error‑code explanations.  
- Explore related operations like **[Get File Info](/file-info/)** and **[Spreadsheet Operations](/spreadsheet-operations/)** for a broader understanding of the Aspose.Cells Cloud API.