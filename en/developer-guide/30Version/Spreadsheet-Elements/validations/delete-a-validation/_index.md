---
title: "Delete a worksheet validation on an Excel worksheet"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /validations/delete/
keywords: "Delete worksheet validation, Aspose Cells Cloud, REST API, Excel, worksheet validation"
description: "Learn how to delete a worksheet validation from an Excel file using the Aspose.Cells Cloud REST API. Includes request details, cURL example, and SDK code snippets for multiple programming languages."
weight: 10
---

This REST API deletes a worksheet validation by its index on an Excel worksheet.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

**Request parameters**

| Parameter Name   | Type    | Location | Description                              |
|------------------|---------|----------|------------------------------------------|
| name             | string  | path     | The name of the Excel file.              |
| sheetName        | string  | path     | The name of the worksheet.               |
| validationIndex  | integer | path     | The zero‑based index of the validation to delete. |
| folder           | string  | query    | The folder that contains the document.   |
| storageName      | string  | query    | The name of the storage service.         |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to call the Aspose.Cells web service. The example below shows how to delete a validation with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
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

## Cloud SDK Family

Using an SDK is the fastest way to integrate this operation into your application. SDKs handle low‑level details so you can focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to delete a worksheet validation using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}