---
title: "Clear Worksheet Comments"
type: docs
url: /comments/clear/
aliases: [/delete-all-comments-in-a-worksheet/]
keywords: "Aspose Cells clear comments API, delete worksheet comments, Aspose.Cells Cloud REST, Excel comment removal"
description: "Delete all comments from a specific worksheet in an Excel file using Aspose.Cells Cloud API. Learn the DELETE endpoint, required parameters, sample cURL request, and SDK examples (C#, Java, Python, …)."
weight: 50
---

This REST API deletes all comments from a worksheet.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

**Authentication** – Include an `Authorization: Bearer <jwt token>` header.  
A JWT token can be obtained from the Aspose Cloud authentication endpoint by supplying your client ID and client secret.

**Request parameters are listed below:**

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| name           | string | path     | Name of the Excel file (e.g., `test.xlsx`). |
| sheetName      | string | path     | Name of the worksheet (e.g., `Sheet1`). |
| folder         | string | query    | Path to the folder that contains the file. |
| storageName    | string | query    | Name of the storage where the file is located. |

**Response codes**

| Code | Meaning | Sample response |
|------|---------|-----------------|
| 200  | Success – all comments were deleted. | `{ "Code": 200, "Status": "OK" }` |
| 400  | Bad request – invalid parameters. | `{ "Code": 400, "Message": "Invalid request." }` |
| 401  | Unauthorized – missing or invalid JWT token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404  | Not found – file or worksheet does not exist. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500  | Internal server error. | `{ "Code": 500, "Message": "Server error." }` |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK can accelerate development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs (compatible with Aspose.Cells Cloud SDK version 3.13.0):

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}