---
title: "Delete an OLE object in an Excel worksheet"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /oleobjects/delete/
aliases: [/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells Cloud Delete OLE Object, Excel worksheet, REST API, SDK"
description: "Learn how to delete an OLE object from an Excel worksheet using the Aspose.Cells Cloud REST API (v4.0). Includes HTTPS endpoint, authentication steps, cURL example, SDK snippets, error‑handling guidance, and next‑step links."
weight: 50
---

This page explains how to delete a specific OLE object from a worksheet in an Excel workbook using **Aspose.Cells Cloud**. An OLE object can be a linked image, chart, or any embedded object that Excel stores as a separate entity.

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Request Parameters

| Parameter name | Type    | Location | Description                                       |
| -------------- | ------- | -------- | ------------------------------------------------- |
| name           | string  | path     | The workbook name.                                |
| sheetName      | string  | path     | The worksheet name.                               |
| oleObjectIndex | integer | path     | Index of the OLE object to be deleted.            |
| folder         | string  | query    | The folder that contains the workbook. (optional) |
| storageName    | string  | query    | The name of the storage service. (optional)       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL command-line tool** to access Aspose.Cells web services easily. The following example shows how to make the call with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### Response details

| HTTP status          | Description                                                            | Sample JSON                                                         |
| -------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **200 OK**           | The OLE object was deleted successfully.                               | `{ "Code": 200, "Status": "OK" }`                                   |
| **401 Unauthorized** | Missing or invalid JWT token.                                          | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | The specified workbook, worksheet, or OLE object index does not exist. | `{ "Code": 404, "Message": "OLE object index out of range." }`      |
| **400 Bad Request**  | Required parameters are missing or malformed.                          | `{ "Code": 400, "Message": "Invalid request parameters." }`         |

Handle these responses in your application by checking the status code and displaying the accompanying message.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
