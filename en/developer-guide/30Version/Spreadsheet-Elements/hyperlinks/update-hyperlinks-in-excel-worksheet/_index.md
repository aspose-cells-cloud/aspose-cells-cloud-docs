---
title: "Update a Hyperlink in an Excel Worksheet"
type: docs
url: /hyperlinks/update/
aliases: [/update-hyperlinks-in-excel-worksheet/]
keywords: "Aspose.Cells Cloud, update hyperlink API, Excel hyperlink REST, v3.0, SDK example"
description: "Learn how to update a hyperlink in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, request‑body schema, cURL sample, and SDK code snippets for C#, Java, Python, and more."
weight: 30
---

This REST API updates a hyperlink in an Excel worksheet identified by its zero‑based index.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Request parameters

| Parameter Name | Type    | Location | Description                                                          |
| -------------- | ------- | -------- | -------------------------------------------------------------------- |
| name           | string  | path     | Name of the Excel file.                                              |
| sheetName      | string  | path     | Name of the worksheet.                                               |
| hyperlinkIndex | integer | path     | Zero‑based index of the hyperlink to be updated.                     |
| hyperlink      | object  | body     | **Hyperlink** object that contains the new values for the hyperlink. |
| folder         | string  | query    | Folder path where the workbook is stored.                            |
| storageName    | string  | query    | Name of the storage service.                                         |

**Request body schema** – The `hyperlink` object may contain the following fields:

| Field         | Type   | Required | Description                                                                                              |
| ------------- | ------ | -------- | -------------------------------------------------------------------------------------------------------- |
| Address       | string | yes      | Target URL of the hyperlink.                                                                             |
| Area          | object | yes      | Defines the cell range where the hyperlink is placed (`StartRow`, `StartColumn`, `EndRow`, `EndColumn`). |
| ScreenTip     | string | no       | Text displayed when the mouse hovers over the hyperlink.                                                 |
| TextToDisplay | string | no       | Text shown in the cell for the hyperlink.                                                                |
| link          | object | no       | Hypermedia links (`Href`, `Rel`, `Title`, `Type`).                                                       |

### Error Responses

| HTTP Code | Reason                                             | Example Body                                                        |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – missing or invalid parameters.       | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – missing or invalid JWT token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist.  | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": null,
          "TextToDisplay": "https://www.msnbc.com/",
          "link": {
            "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/4",
            "Rel": "self",
            "Title": null,
            "Type": null
          }
        },
        "Code": 200,
        "Status": "OK"
      }'
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

Using an SDK is the fastest way to develop. An SDK handles low‑level details, letting you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
