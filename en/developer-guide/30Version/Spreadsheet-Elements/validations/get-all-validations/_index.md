---
title: "Get All Worksheet Validations from an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Get All"
type: docs
url: /validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, worksheet validations, REST API, Get all validations, SDKs"
description: "Get all Excel worksheet validations using Aspose.Cells Cloud REST API with cURL or SDKs for C#, Java, Python."
weight: 100
ArticleTitle: "Get All Worksheet Validations via Aspose.Cells Cloud REST API"
---
The **GetWorksheetValidations** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations`) retrieves descriptions of all data validation rules defined in a specific worksheet, enabling developers to inspect enforced constraints such as list dropdowns, date ranges, or numeric limits. Aspose.Cells Cloud supports this operation via a RESTful endpoint requiring the workbook name (`name`) and worksheet name (`sheetName`) as path parameters, with optional `folder` and `storageName` query parameters for file location context. This allows accurate, programmatic retrieval of validation metadata to support data integrity auditing or migration workflows.

This REST API retrieves all worksheet validations on an Excel worksheet.

## The Get Worksheet Validations Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The workbook name. |
| sheetName | String | Path | The worksheet name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Response status codes**


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells Cloud web services easily. **Prerequisite:** you must include a valid JWT token in the `Authorization` header.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "Value must be between 1 and 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "Select a value from the list."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Response**

```json
[
  {
    "Name": "ValidationsResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "ValidationsResponse"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}
