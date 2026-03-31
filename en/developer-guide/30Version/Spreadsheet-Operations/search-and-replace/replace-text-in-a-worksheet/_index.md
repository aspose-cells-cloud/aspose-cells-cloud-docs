---
title: "Replace Text in an Excel Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Replace in worksheet"
type: docs
url: /replace-text-in-a-worksheet/
url: /worksheets/replace-text/
aliases: [/replace-text-in-a-workbook/]
keywords: "Aspose.Cells replace text API, Excel replace text, Aspose.Cells Cloud, REST API, spreadsheet, worksheet"
description: "Learn how to replace text in an Excel worksheet using the Aspose.Cells Cloud API (v3.0). Includes prerequisites, authentication, request syntax, cURL example, SDK code samples, response details, and error handling."
weight: 70
---

This REST API replaces text in an Excel worksheet using the **Aspose.Cells replace text API**.

## Prerequisites

1. A valid Aspose Cloud client ID and client secret.  
2. An access token obtained via OAuth/JWT (`https://api.aspose.cloud/connect/token`).  
3. The workbook must be uploaded to Aspose Cloud storage (or already exist in the specified folder).  

## Authentication

All requests must include the following HTTP header:

```
Authorization: Bearer {access_token}
```

Replace `{access_token}` with the token acquired in the prerequisites step. The token should be refreshed before it expires.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```

### Request Parameters

| Parameter Name | Type   | Location | Description                         |
|----------------|--------|----------|-------------------------------------|
| **name**       | string | path     | The name of the Excel workbook.     |
| **sheetName**  | string | path     | The name of the worksheet.          |
| **oldValue**   | string | query    | The text to be replaced.            |
| **newValue**   | string | query    | The replacement text.               |
| **folder**     | string | query    | The folder that contains the file.  |
| **storageName**| string | query    | The storage service name.           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorsheetTextReplace) defines this publicly accessible interface.

You can use the cURL command‑line tool to call the service:

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 0,
  "Worksheet": {
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Response Details

| Property | Type   | Description |
|----------|--------|-------------|
| **Matches** | integer | Number of cells where `oldValue` was replaced. |
| **Worksheet.link.Href** | string | Relative URL of the affected worksheet. |
| **Code** | integer | HTTP status code returned by the API (e.g., 200). |
| **Status** | string | Textual representation of the status (e.g., “OK”). |

### Error Handling

| HTTP Status | Example JSON Payload | Meaning |
|-------------|----------------------|---------|
| **400** | `{ "Code": 400, "Message": "Invalid request.", "Description": "The parameter 'oldValue' is missing." }` | Bad request – required parameter missing or malformed. |
| **401** | `{ "Code": 401, "Message": "Unauthorized.", "Description": "Access token is invalid or expired." }` | Authentication failure – obtain a new token. |
| **404** | `{ "Code": 404, "Message": "Worksheet not found.", "Description": "The sheetName 'SheetX' does not exist." }` | The specified worksheet could not be located. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

## See Also

- [Find text in a worksheet](/cells/worksheets/find-text/)
- [Replace text in a workbook](/cells/workbook/replace-text/)
- [Search and replace overview](/cells/overview/search-replace/)

---