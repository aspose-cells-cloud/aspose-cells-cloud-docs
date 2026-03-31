---
title: "Copy columns in an Excel worksheet"
second_title: "Document"
linktitle: "Copy"
type: docs
url: /columns/copy/
aliases: [/copy-columns-in-excel-worksheet/,/copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, copy columns, Excel API, REST, Cloud SDK, cURL, Java, Python"
description: "Learn how to copy one or more columns in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes request syntax, required parameters, authentication, error handling, and SDK examples in C#, Java, Python, and more."
weight: 30
---

This REST API copies **columns** in an Excel worksheet.

## Overview
The **Copy Columns** operation lets you duplicate a single column or a range of columns and insert the copy at a specified location within the same worksheet.

## Prerequisites
- An Aspose Cloud account.  
- A valid **client ID** and **client secret** to obtain an OAuth 2.0 access token.  
- The workbook you want to modify must be stored in Aspose Cloud storage (or provided via the `folder` parameter).  
- cURL installed locally, or any HTTP client capable of sending `POST` requests.

## Authentication
All Aspose.Cells Cloud requests require an **Authorization** header containing a Bearer token.

1. **Obtain an access token**  
   Send a `POST` request to `https://api.aspose.cloud/connect/token` with your client credentials. The response includes `access_token`.

2. **Include the token in every API call**  

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/<workbook>.xlsx/worksheets/<sheet>/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
        -H "Authorization: Bearer <access_token>" \
        -H "accept: application/json"
   ```

> **Tip:** Store the token in an environment variable (e.g., `ASPOSE_TOKEN`) and reference it with `$ASPOSE_TOKEN` to avoid exposing credentials in scripts.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Request Parameters

| Parameter Name          | Type    | Location | Description                                                                 |
|-------------------------|---------|----------|-----------------------------------------------------------------------------|
| **name**                | string  | path     | The workbook name.                                                          |
| **sheetName**           | string  | path     | The worksheet name.                                                         |
| **sourceColumnIndex**   | integer | query    | 0‑based index of the column to copy.                                        |
| **destinationColumnIndex** | integer | query | 0‑based index where the copied column(s) will be inserted.                  |
| **columnNumber**        | integer | query    | Number of consecutive columns to copy.                                      |
| **worksheet**           | string  | query    | *(Optional)* Worksheet identifier used when the worksheet name differs from the path. |
| **folder**              | string  | query    | Path to the folder containing the workbook in Aspose Cloud storage.        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) defines the full contract for this operation.

### cURL Example

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Error Handling
The API returns standard HTTP status codes with a JSON payload describing the error.

| Status Code | Meaning                     | Example JSON Body                              |
|-------------|----------------------------|-----------------------------------------------|
| **400**     | Bad request – invalid parameters | `{ "Code": 400, "Message": "Invalid column index." }` |
| **401**     | Unauthorized – missing or invalid token | `{ "Code": 401, "Message": "Access token is invalid or expired." }` |
| **404**     | Not found – workbook or worksheet does not exist | `{ "Code": 404, "Message": "Workbook not found." }` |
| **500**     | Internal server error – unexpected condition | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

> **How to troubleshoot:** Verify that the access token is current, the workbook and worksheet names are correct, and that `sourceColumnIndex`, `destinationColumnIndex`, and `columnNumber` are within the worksheet’s column range.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How do I authenticate when calling the Copy Columns API?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Obtain an OAuth2 access token from Aspose Cloud using your client ID and secret, then include it in the request header as `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "What is the difference between `sourceColumnIndex` and `destinationColumnIndex`?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` is the 0‑based index of the column you want to copy. `destinationColumnIndex` is the 0‑based index where the copied column(s) will be inserted."
      }
    },
    {
      "@type": "Question",
      "name": "What response do I receive if the copy operation fails?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The API returns a non‑200 status code (e.g., 400 for a bad request, 401 for unauthorized). The response body contains a JSON object with fields `Code` and `Message` describing the error."
      }
    }
  ]
}
</script>