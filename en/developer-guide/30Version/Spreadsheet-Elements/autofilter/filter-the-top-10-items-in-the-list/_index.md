---
title: "Add Top 10 Filter to an Excel Worksheet (Aspose.Cells Cloud)"
ArticleTitle: "Add Top 10 Filter to an Excel Worksheet – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Add top 10 filter"
type: docs
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, Top 10 filter, Excel API"
description: "Learn how to apply a Top 10 AutoFilter to an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint, parameters, HTTPS cURL example, authentication details, error handling, and SDK snippets for C#, Java, Python, and more."
weight: 65
---

## REST API

This REST API filters the **Top 10** items in a list.

> **Prerequisites**  
> • Obtain a valid JWT token using Aspose.Cells Cloud authentication.  
> • Upload the Excel workbook to your Aspose Cloud storage (or specify the storage/folder where it resides).  
> • Know the worksheet name and the cell range that you want to filter.

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name  | Type    | Location | Required | Default | Description                                                                 |
| --------------- | ------- | -------- | -------- | ------- | --------------------------------------------------------------------------- |
| **name**        | string  | path     | Yes      | —       | The name of the Excel file.                                                 |
| **sheetName**   | string  | path     | Yes      | —       | The name of the worksheet that contains the data.                           |
| **range**       | string  | query    | Yes      | —       | The cell range to which the filter is applied (e.g., `A1:B10`).             |
| **fieldIndex**  | integer | query    | Yes      | —       | Zero‑based index of the column on which the filter is applied.              |
| **isTop**       | boolean | query    | Yes      | `true`  | `true` to filter the top items; `false` for bottom items.                   |
| **isPercent**   | boolean | query    | No       | `false` | `true` to treat `itemCount` as a percentage; `false` for an absolute count. |
| **itemCount**   | integer | query    | No       | `10`    | Number of items to include in the filter.                                   |
| **matchBlanks** | boolean | query    | No       | `false` | `true` to include blank cells in the filter results.                        |
| **refresh**     | boolean | query    | No       | `false` | `true` to refresh the filter after applying it.                             |
| **folder**      | string  | query    | No       | —       | The folder in storage where the Excel file is located.                      |
| **storageName** | string  | query    | No       | —       | The name of the Aspose Cloud storage.                                       |

### **Response**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Typical error responses**

```json
{
    "Code":400,
    "Message":"Bad Request – missing or invalid parameters."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – invalid or missing JWT token."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – uploaded file exceeds the allowed size."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – unexpected server condition."
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

## How to Use the PutWorksheetFilterTop10 API with SDKs

### PutWorksheetFilterTop10 API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}