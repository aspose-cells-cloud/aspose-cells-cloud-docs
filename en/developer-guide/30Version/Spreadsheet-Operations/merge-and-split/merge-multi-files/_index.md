---
title: "Merge Multiple Excel Files into a Single Workbook"
second_title: "Document"
linktitle: "Merge Multiple Excel Files"
type: docs
url: /merge-multi-files-into-excel/
aliases: [ /merge/multi-files/]
keywords: "Aspose.Cells Cloud, merge multiple Excel files, REST API, spreadsheet merge, cloud SDK"
description: "Learn how to merge multiple Excel workbooks into one file using the Aspose.Cells Cloud REST API (v3.0). Includes HTTPS endpoint, cURL command, SDK samples, required parameters, and error‑handling details."
weight: 32
---

This REST API merges multiple Excel files into a single Excel workbook.

## Prerequisites

* An **Aspose Cloud** account with a valid **Client Id** and **Client Secret**.  
* A **JWT Bearer token** obtained from the OAuth endpoint  
  `POST https://api.aspose.cloud/connect/token`. (See the *Authentication* page for a full example.)  
* API version **v3.0** (the endpoint used in this document).  
* `curl` (or any HTTP client) installed on your machine.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### Request parameters

| Parameter Name | Type   | Location   | Description                                                                    | Required |
|----------------|--------|------------|--------------------------------------------------------------------------------|----------|
| files[]        | file   | formData   | One or more Excel workbooks to be merged. Use `file1`, `file2`, … in the request. | Yes      |
| format         | string | query      | Desired output format (e.g., `xlsx`).                                         | Yes      |
| mergeToOneSheet| boolean| query      | Set to `true` to combine all worksheets into a single sheet; default is `false`. | No       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

*Explanation*:  
- The request uses **HTTPS** to ensure secure transmission.  
- The `Authorization` header carries the JWT token obtained in the *Prerequisites* step.  
- `-F` automatically sets the `Content-Type` to **multipart/form-data**, which matches the payload of file uploads.  
- Replace `<jwt token>` with your actual token and `file1.xlsx`, `file2.xlsx` with the files you want to merge.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

*Explanation*:  
- The response returns a JSON object containing the merged workbook(s) encoded in **Base64**.  
- Each entry in the `Files` array provides the original filename, its size, and the merged file content.

{{< /tab >}}

{{< /tabs >}}

### Error handling

| HTTP Status | Meaning                              | Sample error body |
|-------------|--------------------------------------|-------------------|
| 400         | Bad request – missing required files or parameters. | `{ "ErrorMessage": "File list cannot be empty.", "ErrorCode": "BadRequest" }` |
| 401         | Unauthorized – invalid or expired JWT token. | `{ "ErrorMessage": "Access token is invalid.", "ErrorCode": "Unauthorized" }` |
| 415         | Unsupported Media Type – file format not supported. | `{ "ErrorMessage": "Only Excel formats are allowed.", "ErrorCode": "UnsupportedMediaType" }` |
| 500         | Internal server error – unexpected failure on the server side. | `{ "ErrorMessage": "An unexpected error occurred.", "ErrorCode": "InternalError" }` |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

*Last Updated: 2024‑03‑28*