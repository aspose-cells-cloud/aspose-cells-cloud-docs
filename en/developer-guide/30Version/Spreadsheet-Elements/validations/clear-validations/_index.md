---
title: "Delete All Worksheet Validations – Aspose.Cells Cloud API"
second_title: "Documentation"
linktitle: "Delete"
type: docs
url: /validations/clear/
keywords: "Aspose.Cells Cloud, Delete worksheet validations, Excel, REST API, Spreadsheet validation, API"
description: "Remove all data validation rules from a worksheet in an Excel file using Aspose.Cells Cloud REST API. Includes authentication steps, request details, cURL example, response schema, error handling, and SDK snippets."
weight: 10
---

**Prerequisites**  
- A valid Aspose Cloud account.  
- A JWT access token obtained via the Aspose Cloud authentication API (`/connect/token`).  
- The workbook must be stored in your Aspose Cloud storage (or the appropriate `folder`/`storageName` query parameters must be provided).

This REST API deletes all worksheet validations on an Excel worksheet.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

The request parameters are:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| name           | string | path     | The name of the Excel document. |
| sheetName      | string | path     | The name of the worksheet containing the validations. |
| folder         | string | query    | The folder where the document is stored. |
| storageName    | string | query    | The name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the API with cURL after obtaining a JWT token.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
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

### Error Handling

| HTTP Status | Meaning                              | Description |
|-------------|--------------------------------------|-------------|
| 400         | Bad Request                          | The request is malformed or missing required parameters. |
| 401         | Unauthorized                         | The JWT token is missing, invalid, or expired. |
| 404         | Not Found                            | The specified workbook or worksheet does not exist. |
| 500         | Internal Server Error                | An unexpected error occurred on the server side. |

The error payload follows the same JSON structure with `Code` and `Message` fields, for example:

```json
{
  "Code": 401,
  "Message": "Invalid or expired token."
}
```

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on business logic. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}