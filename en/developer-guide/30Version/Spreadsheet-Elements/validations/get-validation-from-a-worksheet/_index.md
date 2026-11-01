---
title: "Get a worksheet validation by index from an Excel worksheet"
second_title: "Developer Guide"
linktitle: "Get"
type: docs
url: /validations/get/
aliases: [/get-validation-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, worksheet validation API, get validation by index, Excel REST API, Aspose.Cells SDK"
description: "Get a validation by zero-based index from a worksheet in Excel via Aspose.Cells Cloud API with cURL or SDK examples"
weight: 100
ArticleTitle: "Get Worksheet Validation by Index in Aspose.Cells Cloud REST API"
---
The **GetWorksheetValidation** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}`) retrieves a specific data validation rule from an Excel worksheet by its zero-based index, enabling developers to inspect validation constraints such as formula, type, and error message. Aspose.Cells Cloud supports this operation as part of its REST API for spreadsheet automation, allowing programmatic access to worksheet-level validation metadata without requiring local Excel installation. Authentication requires a JWT token obtained via `/connect/token` and included in the `Authorization: Bearer <token>` header.

## The Get Worksheet Validation Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The workbook name. |
| sheetName | String | Path | The worksheet name. |
| validationIndex | Integer | Path | The validation index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

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

| Field          | Type    | Description                                                             |
| -------------- | ------- | ----------------------------------------------------------------------- |
| AlertStyle     | string  | The style of the alert shown to the user (Stop, Warning, Information).  |
| AreaList       | array   | Collection of cell ranges that the validation applies to.               |
| IgnoreBlank    | boolean | If `true`, blank cells are ignored during validation.                   |
| InCellDropDown | boolean | If `true`, a drop‑down list is displayed in the cell.                   |
| Operator       | string  | Comparison operator used for the validation (e.g., `None`, `Between`).  |
| ShowError      | boolean | Determines whether an error message is shown when validation fails.     |
| ShowInput      | boolean | Determines whether an input message is shown when the cell is selected. |
| Type           | string  | Type of validation (e.g., `AnyValue`, `WholeNumber`, `Decimal`, etc.).  |
| link.Href      | string  | Self‑reference URL to the validation resource.                          |
| link.Rel       | string  | Relation type (always `self`).                                          |

**Possible error codes**

| HTTP Status | Meaning                                                              |
| ----------- | -------------------------------------------------------------------- |
| 200         | Validation retrieved successfully.                                   |
| 400         | Bad request – missing or invalid parameters.                         |
| 401         | Unauthorized – invalid or missing JWT token.                         |
| 404         | Not found – workbook, worksheet, or validation index does not exist. |
| 500         | Internal server error – unexpected condition.                        |

### **Response**

```json
[
  {
    "Name": "ValidationResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "ValidationResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

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
