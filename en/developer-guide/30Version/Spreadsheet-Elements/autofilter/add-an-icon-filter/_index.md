---
title: "Add an Icon Filter to an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Add icon filter"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/, /autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, Icon Filter, AutoFilter, REST API"
description: "Apply icon filters to Excel worksheets via Aspose.Cells Cloud REST API with icon set types and field index."
weight: 65
ArticleTitle: "Add an Icon Filter to an Excel Worksheet – Aspose.Cells Cloud Documentation"
---
The **PutWorksheetIconFilter** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter`) enables developers to add an icon filter to a specified range in an Excel worksheet via the Aspose.Cells Cloud REST API, allowing conditional formatting based on icon sets such as traffic lights or arrows by specifying the icon set type and icon ID along with the field index and range.

## The Put Worksheet Icon Filter Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters:

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| range | String | Query | Represents the range to which the specified AutoFilter applies. |
| fieldIndex | Integer | Query | The integer offset of the field on which you want to base the filter (from the left of the list; the leftmost field is field 0). |
| iconSetType | String | Query | The icon set type. |
| iconId | Integer | Query | The icon id. |
| matchBlanks | Boolean | Query | Match all blank cell in the list. |
| refresh | Boolean | Query | Refresh auto filters to hide or unhide the rows. |
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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

This REST API adds an **icon filter** to an Excel worksheet using the **Aspose.Cells Cloud REST API**.

**Background:** An icon filter applies a visual icon set to cells based on their values, allowing quick visual analysis of data trends. Common use‑cases include highlighting performance metrics, status indicators, or categorizing values with traffic‑light icons directly within Excel worksheets.

## How to Use the PutWorksheetIconFilter API with SDKs

### PutWorksheetIconFilter API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
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

Possible response status codes:

| Code | Description                                             |
| ---- | ------------------------------------------------------- |
| 200  | Filter applied successfully.                            |
| 400  | Bad request – missing or invalid parameters.            |
| 401  | Unauthorized – invalid or missing authentication token. |
| 404  | Workbook, worksheet, or specified range not found.      |
| 500  | Internal server error.                                  |

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

For other AutoFilter capabilities, see the documentation on **[Add Color Filter](/autofilter/add-color-filter/)**, **[Add Date Filter](/autofilter/add-date-filter/)**, and **[Clear AutoFilter](/autofilter/clear-autofilter/)**.
