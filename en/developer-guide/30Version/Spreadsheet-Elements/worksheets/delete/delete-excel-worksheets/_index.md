---
title: "Delete Multiple Excel Worksheets"
second_title: "Document"
linktitle: "Multiple worksheets"
type: docs
url: /worksheets/delete-multiple/
aliases: [/delete-excel-worksheets/]
keywords: "Aspose.Cells Cloud, delete multiple worksheets, Excel workbook, REST API, v3.0"
description: "Learn how to delete several worksheets from an Excel workbook using the Aspose.Cells Cloud REST API (v3.0). Includes a secure HTTPS endpoint, required parameters, a corrected cURL example, and SDK snippets for multiple programming languages."
weight: 20
---

This REST API deletes multiple worksheets from a workbook.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Request parameters**

| Parameter Name | Type   | Location | Description                                                                 |
| -------------- | ------ | -------- | --------------------------------------------------------------------------- |
| name           | string | path     | The name of the Excel file.                                                 |
| matchCondition | object | body     | A `MatchConditionRequest` object that specifies which worksheets to delete. |
| folder         | string | query    | Folder path in storage where the file is located.                           |
| storageName    | string | query    | Name of the storage service.                                                |

**MatchConditionRequest Properties**

| Name                | Type     | Description                                  | Notes    |
| ------------------- | -------- | -------------------------------------------- | -------- |
| RegexPattern        | string   | Regular expression to match worksheet names. | optional |
| FullMatchConditions | string[] | Exact worksheet names to be deleted.         | optional |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL. **A valid JWT token is required in the `Authorization` header.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

The request can also return common error responses, for example:

| HTTP Status | Meaning                                      | Sample Payload                                           |
| ----------- | -------------------------------------------- | -------------------------------------------------------- |
| 400         | Bad request – invalid JSON or parameters     | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401         | Unauthorized – missing or invalid JWT token  | `{"Code":401,"Message":"Authentication failed."}`        |
| 403         | Forbidden – insufficient permissions         | `{"Code":403,"Message":"Access denied."}`                |
| 404         | Not found – file or worksheet does not exist | `{"Code":404,"Message":"Resource not found."}`           |
| 500         | Internal server error                        | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}
