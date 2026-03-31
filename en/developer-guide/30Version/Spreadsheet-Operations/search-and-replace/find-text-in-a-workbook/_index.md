---
title: "Find text in an Excel workbook"
second_title: "Document"
linktitle: "Find in workbook"
type: docs
url: /workbook/find-text/
aliases: [/find-text-in-a-workbook/]
weight: 30
keywords: "Find text, Excel workbook, Aspose.Cells Cloud, REST API, SDK, search text in workbook, Aspose.Cells findText, Excel API"
description: "Learn how to use Aspose.Cells Cloud API to **find text** in Excel workbooks (XLS‑X, ODS). Includes cURL example, SDK snippets, and response schema. Get started now."
---

This REST API searches for text in an Excel workbook.

## REST API

**Prerequisites** – You need a valid Aspose.Cells Cloud account, the API version **v3.0**, and an OAuth 2.0 bearer token for authentication. The API works with Excel formats such as XLS, XLSX, XLSM, XLSB, and ODS.

**Authentication** – Include the following header in every request:  

```
Authorization: Bearer <your_access_token>
```

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

The request accepts the following parameters:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| name           | string | path     | Name of the Excel workbook. |
| text           | string | query    | Text string to search for. |
| folder         | string | query    | Folder that contains the workbook (optional). |
| storageName    | string | query    | Name of the storage where the workbook resides (optional). |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Error handling** – The API may return standard HTTP status codes such as **401 Unauthorized** (invalid or missing token), **404 Not Found** (workbook does not exist), and **500 Internal Server Error** (unexpected server condition). The response body for errors follows the common Aspose.Cells error format.

**Quick FAQ**

- **How do I search for a specific string in an Excel workbook using Aspose.Cells Cloud?**  
  Send a **POST** request to `https://api.aspose.cloud/v3.0/cells/{workbookName}/findText` with the query parameter `text=<searchString>` and include the `Authorization: Bearer <token>` header. The response contains a `TextItems` collection with each match.

- **What parameters are required for the Find Text API?**  
  - `name` (path) – workbook name (required)  
  - `text` (query) – string to locate (required)  
  - `folder` (query) – workbook folder (optional)  
  - `storageName` (query) – storage name (optional)

- **What does the API response look like when a match is found?**  
  The JSON response includes a `Status` field and a `TextItems` object. `TextItems.TextItemList` is an array; each entry provides a `link` object (Href, Rel, Title, Type) and a `Text` field with the matched string.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}