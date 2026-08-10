---
title: "Get Named Ranges on an Excel Workbook"
second_title: "Document"
linktitle: "Name"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "named ranges, Excel, Aspose.Cells, Cloud API, worksheets"
description: "Retrieve named ranges from an Excel workbook using the Aspose.Cells Cloud REST API. Includes request details, sample cURL commands, and SDK examples for multiple programming languages."
ArticleTitle: "Get Named Ranges on an Excel Workbook – Aspose.Cells Cloud API"
weight: 10
---

This REST API returns information about named ranges defined within worksheets.

**Background** – A *named range* is a user‑defined identifier that refers to a specific cell or block of cells in a worksheet. Named ranges simplify formula creation, improve readability, and enable programmatic access to frequently used areas of a workbook.

**Prerequisites** – Access to the Aspose.Cells Cloud API requires a valid JWT access token. Obtain the token by authenticating with your Aspose Cloud client ID and client secret via the OAuth 2.0 token endpoint. Include the token in the `Authorization: Bearer <jwt token>` header of every request.

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type   | Location     | Description                                  |
| -------------- | ------ | ------------ | -------------------------------------------- |
| name           | string | Path         | The name of the Excel document.              |
| folder         | string | Query string | The folder that contains the document.       |
| storageName    | string | Query string | The storage name where the document resides. |

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to call Aspose.Cells web services. The example below demonstrates how to retrieve named ranges using cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Response Model**

| Field          | Type    | Description                                          |
|----------------|---------|------------------------------------------------------|
| `ColumnCount`  | integer | Number of columns in the range.                      |
| `ColumnWidth`  | number  | Width of each column (in points).                    |
| `FirstColumn`  | integer | Zero‑based index of the first column in the range.   |
| `FirstRow`     | integer | Zero‑based index of the first row in the range.      |
| `Name`         | string  | The user‑defined name of the range.                  |
| `RefersTo`     | string  | A formula that defines the cell reference (e.g., `=Sheet1!$B$10:$H$10`). |
| `RowCount`     | integer | Number of rows in the range.                         |
| `RowHeight`    | number  | Height of each row (in points).                      |
| `Worksheet`    | string  | Name of the worksheet that contains the range.       |

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality. SDKs handle low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}