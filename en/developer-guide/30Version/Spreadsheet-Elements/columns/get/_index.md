---
title: "Get Column Details – Aspose.Cells Cloud API Reference (v4.0)"
second_title: "Document"
linktitle: "Get"
type: docs
url: /columns/get/
aliases:
  - /get-columns-from-an-excel-worksheet/
  - /get-columns-from-a-worksheet/
  - /get-column-from-a-worksheet/
keywords: "Aspose.Cells Cloud, Get Column API, Excel column API, retrieve column data, Aspose.Cells SDK"
description: "Retrieve detailed information about a worksheet column (index, width, style, hidden state) using Aspose.Cells Cloud REST API. Includes cURL example, SDK snippets, authentication steps, and error handling."
weight: 10
---

This REST API reads worksheet column data by the column’s index.

### Prerequisites

- A valid Aspose Cloud account.  
- An OAuth 2.0 access token (Bearer token).  
- The workbook must be stored in Aspose Cloud storage or a location you specify with `folder`/`storageName`.

## REST API

```bash
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

> **Note:** All Aspose.Cloud endpoints require **HTTPS**.

### Authentication

To call the API you must include an `Authorization` header containing a valid Bearer token:

```bash
-H "Authorization: Bearer <access_token>"
```

You can obtain an access token by following the [OAuth 2.0 token‑generation guide](https://docs.aspose.cloud/authentication/).

### Parameters

| Parameter Name | Type    | Location | Description                                                                 | Required |
|----------------|---------|----------|-----------------------------------------------------------------------------|----------|
| **name**       | string  | path     | The name of the workbook file.                                              | Yes      |
| **sheetName**  | string  | path     | The name of the worksheet that contains the column.                         | Yes      |
| **columnIndex**| integer | path     | Zero‑based index of the column to retrieve.                                 | Yes      |
| **folder**     | string  | query    | The folder path in storage where the workbook is located. *(optional)*    | No       |
| **storageName**| string  | query    | The name of the storage service (e.g., Aspose Cloud Storage). *(optional)*| No       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

### cURL Request

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### cURL Response

```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 10,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

### Possible Errors

| HTTP Status | Code | Message                              | When it occurs                                    |
|-------------|------|--------------------------------------|---------------------------------------------------|
| 400         | 400  | Bad Request                          | Required parameter is missing or malformed.      |
| 401         | 401  | Unauthorized                         | Missing or invalid `Authorization` header.       |
| 404         | 404  | Not Found                            | The specified workbook, worksheet, or column does not exist. |
| 500         | 500  | Internal Server Error                | Unexpected server‑side problem.                   |

**Example – 404 Not Found**

```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

## Cloud SDK Family

Using an SDK is the fastest way to develop against the API. SDKs handle low‑level details, allowing you to focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}