---
title: "Get a worksheet validation by index from an Excel worksheet"
second_title: "Document"
linktitle: "Get"
type: docs
url: /validations/get/
aliases: [/get-validation-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, worksheet validation API, get validation by index, Excel REST API, Aspose.Cells SDK"
description: "Retrieve a worksheet validation by its zero‑based index from an Excel workbook using Aspose.Cells Cloud API (v3.0). Includes cURL example, response schema, error codes, and SDK snippets for C#, Java, Python, and more."
weight: 10
---

This REST API retrieves a worksheet validation by its index on an Excel worksheet.  
Before calling the endpoint, obtain a JWT token via the `/connect/token` endpoint and include it in the `Authorization` header as `Bearer <jwt token>`.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

**Request parameters**

| Parameter Name   | Type    | Location | Description                                    |
|------------------|---------|----------|------------------------------------------------|
| name             | string  | path     | The name of the workbook file.                 |
| sheetName        | string  | path     | The name of the worksheet.                     |
| validationIndex  | integer | path     | Zero‑based index of the validation to retrieve.|
| folder           | string  | query    | Folder that contains the workbook.             |
| storageName      | string  | query    | Name of the storage service.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Response schema**

| Field          | Type    | Description                                                                 |
|----------------|---------|-----------------------------------------------------------------------------|
| AlertStyle     | string  | The style of the alert shown to the user (Stop, Warning, Information).   |
| AreaList       | array   | Collection of cell ranges that the validation applies to.                  |
| IgnoreBlank    | boolean | If `true`, blank cells are ignored during validation.                      |
| InCellDropDown | boolean | If `true`, a drop‑down list is displayed in the cell.                      |
| Operator       | string  | Comparison operator used for the validation (e.g., `None`, `Between`).    |
| ShowError      | boolean | Determines whether an error message is shown when validation fails.       |
| ShowInput      | boolean | Determines whether an input message is shown when the cell is selected.   |
| Type           | string  | Type of validation (e.g., `AnyValue`, `WholeNumber`, `Decimal`, etc.).     |
| link.Href      | string  | Self‑reference URL to the validation resource.                              |
| link.Rel       | string  | Relation type (always `self`).                                              |

**Possible error codes**

| HTTP Status | Meaning                              |
|-------------|--------------------------------------|
| 200         | Validation retrieved successfully.   |
| 400         | Bad request – missing or invalid parameters. |
| 401         | Unauthorized – invalid or missing JWT token. |
| 404         | Not found – workbook, worksheet, or validation index does not exist. |
| 500         | Internal server error – unexpected condition. |

**Frequently asked questions**

- **How do I authenticate to call this API?**  
  Obtain a JWT token from the `/connect/token` endpoint using your client ID and secret, then include it in the `Authorization` header as `Bearer <jwt token>`.

- **What does the `AlertStyle` property represent?**  
  It indicates the type of alert presented to the user when validation fails. Allowed values are `Stop`, `Warning`, and `Information`.

- **Is this request idempotent?**  
  Yes. A `GET` request does not modify server state and can be safely retried.

## Cloud SDK Family

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details so you can focus on your business logic. Check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}