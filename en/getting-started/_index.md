---
title: "Getting Started with Aspose.Cells Cloud API – Process Excel Files in 3 Simple Steps"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Getting Started"
linktitle: "Getting Started"
type: docs
url: /getting-started/
description: "Learn how to upload, convert, and download Excel files using Aspose.Cells Cloud REST API in three simple steps. Includes cURL code samples."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, spreadsheet conversion, Excel to PDF, cloud spreadsheet, Aspose.Cells Cloud API"
---

- [Overview](/cells/overview/)
- [Quickstart](/cells/quickstart/)
- [Available SDKs](/cells/available-sdks/)
- [Supported Platforms](/cells/supported-platforms/)
- [Supported File Formats](/cells/supported-file-formats/)
- [Evaluate Aspose.Cells Cloud](/cells/evaluate-aspose-cells/)
- [Pricing Plan](/cells/pricing-plan/)
- [Technical Support](/cells/technical-support/)
- [How to Run Docker Container](/cells/how-to-run-docker-container/)

**Getting Started Guide**

Before you begin, make sure you have a valid **Aspose Cloud API key** and **storage name**. These credentials are required for all subsequent API calls.

**Step 1: Upload an Excel file**  
Upload your source workbook to Aspose Cloud storage.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*Request body*: The file is sent as a binary stream (`application/octet‑stream`).  
*Required parameters*:

- `path` – storage path where the file will be saved (e.g., `folder/sample.xlsx`).

**Step 2: Convert the workbook to PDF**  
Send a conversion request after the file is stored.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Required parameters*:

- `name` – name of the uploaded workbook (e.g., `sample.xlsx`).
- `format` – target format (`pdf`).
- `outputPath` – storage path for the converted file (e.g., `folder/result.pdf`).

*Sample response payload* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**Step 3: Download the converted PDF**  
Retrieve the resulting PDF from storage.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Required parameters*:

- `outputPath` – path of the PDF generated in the previous step.

**Sample Request / Response Summary**

| Operation | HTTP Method | Endpoint (example) | Parameters | Success Status |
|-----------|-------------|--------------------|------------|----------------|
| Upload    | PUT         | /cells/storage/file/{path} | `path` (storage location) | 200 OK |
| Convert   | POST        | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Download  | GET         | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Common Error Codes**

- **400 Bad Request** – Missing or invalid parameters.  
- **401 Unauthorized** – Invalid or missing access token.  
- **404 Not Found** – Specified file or path does not exist.  
- **500 Internal Server Error** – Unexpected server error; retry or contact support.