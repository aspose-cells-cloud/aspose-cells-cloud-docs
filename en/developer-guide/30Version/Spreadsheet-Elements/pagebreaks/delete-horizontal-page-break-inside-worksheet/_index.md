---
title: "Delete horizontal page break"
ArticleTitle: "Aspose.Cells Cloud – Delete Horizontal Page Break (REST API)"
second_title: "Developer Guide"
linktitle: "Delete horizontal page break"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, Delete horizontal page break, Excel worksheet, REST API, SDK"
description: "Delete a horizontal page break from an Excel worksheet via Aspose.Cells Cloud REST API using cURL or SDKs."
weight: 50
---
The **DeleteHorizontalPageBreak** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}`) enables developers to remove a specific horizontal page break from a worksheet in Aspose.Cells Cloud by specifying the workbook name, worksheet name, and zero-based index of the break to delete, supporting precise control over print layout without modifying other worksheet elements.

## The Delete Horizontal Page Break Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The workbook name. |
| sheetName | String | Path | The worksheet name. |
| index | Integer | Path | Removes the horizontal page break element at a specified name. Element index, zero based. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Responses

| HTTP Code | Description                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| 401       | Unauthorized – missing or invalid token.                                       |
| 404       | Not Found – the specified file, worksheet, or page‑break index does not exist. |
| 400       | Bad Request – malformed request syntax or invalid parameters.                  |
| 500       | Internal Server Error – an unexpected condition was encountered.               |

**See also:**

- [Add Horizontal Page Break](/page-breaks/add-horizontal-page-break/)
- [Get Horizontal Page Breaks](/page-breaks/get-horizontal-page-breaks/)
- [Delete Vertical Page Break](/page-breaks/delete-vertical-page-break/)

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make the call with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**Response Schema**

| Field   | Type    | Description                                      |
| ------- | ------- | ------------------------------------------------ |
| Code    | integer | HTTP status code (e.g., 200).                    |
| Status  | string  | Textual status message (e.g., "OK").             |
| Message | string  | Optional additional information for error cases. |

{{< /tab >}}

{{< /tabs >}}

_All API calls must be made over **HTTPS**._

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d)._

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f)._

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152)._

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca)._

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0)._

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1)._

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca)._

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
_If the example fails to load, view it on the [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185)._

{{< /tab >}}

{{< /tabs >}}
