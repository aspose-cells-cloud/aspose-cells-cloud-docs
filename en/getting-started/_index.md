---
title: "Getting Started with Aspose.Cells Cloud API – Process Excel Files in 3 Simple Steps"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Getting Started"
linktitle: "Getting Started"
type: docs
url: /getting-started/
description: "Learn how to upload, convert, and download Excel files using Aspose.Cells Cloud REST API in just three steps. Includes code samples for cURL, Python, .NET, and Java."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, spreadsheet conversion, Excel to PDF, cloud spreadsheet"
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
curl -X PUT "https://api.aspose.cloud/v3.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

**Step 2: Convert the workbook to PDF**  
Send a conversion request after the file is stored.

```curl
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/save?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

**Step 3: Download the converted PDF**  
Retrieve the resulting PDF from storage.

```curl
curl -X GET "https://api.aspose.cloud/v3.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

**Sample Request / Response Summary**

| Operation | HTTP Method | Endpoint (example) | Success Status |
|-----------|-------------|--------------------|----------------|
| Upload    | PUT         | /cells/storage/file/{path} | 200 OK |
| Convert   | POST        | /cells/{name}/save?format=pdf&outPath={outputPath} | 200 OK |
| Download  | GET         | /cells/storage/file/{outputPath} | 200 OK |

For more detailed code examples in **Python**, **.NET**, and **Java**, see the SDK documentation linked in the navigation above.  

If you encounter any issues, refer to the **Technical Support** page or the **FAQ** section of the documentation.