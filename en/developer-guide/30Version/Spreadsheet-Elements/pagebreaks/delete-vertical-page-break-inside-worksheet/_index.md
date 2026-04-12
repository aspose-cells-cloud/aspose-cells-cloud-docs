---
title: "Delete Vertical Page Break"
second_title: "Document"
linktitle: "Delete vertical page break"
type: docs
url: /page-breaks/delete-vertical-page-break/
aliases: [/delete-vertical-page-break-inside-worksheet/]
keywords: "delete vertical page break, Aspose.Cells Cloud, REST API"
description: "Remove a vertical page break from an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes cURL example, SDK code snippets, parameters, and error handling."
weight: 60
---

## REST API

This REST API deletes a **vertical** page break.

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

### Request Parameters

| Parameter Name | Type    | Location | Required? | Description                                            |
| -------------- | ------- | -------- | --------- | ------------------------------------------------------ |
| name           | string  | path     | Yes       | The name of the Excel file.                            |
| sheetName      | string  | path     | Yes       | The name of the worksheet containing the break.        |
| index          | integer | path     | Yes       | Zero‑based index of the vertical page break to delete. |
| folder         | string  | query    | No        | Folder path where the file is stored.                  |
| storageName    | string  | query    | No        | Name of the storage service.                           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Error Responses

| HTTP Code | Description                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| 401       | Unauthorized – missing or invalid token.                                       |
| 404       | Not Found – the specified file, worksheet, or page‑break index does not exist. |
| 400       | Bad Request – malformed request syntax or invalid parameters.                  |
| 500       | Internal Server Error – an unexpected condition was encountered.               |

## Cloud SDK Family

Using an SDK can speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
