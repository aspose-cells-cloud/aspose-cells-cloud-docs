---
title: "Add a color filter in an Excel worksheet"
second_title: "Developer Guide"
linktitle: "Add color filter"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/, /autofilter/add-a-color-filter/]
keywords: "Excel, color filter, Aspose.Cells Cloud, REST API, auto filter, JWT authentication"
description: "Learn how to apply a color filter to an Excel worksheet with Aspose.Cells Cloud API. Includes endpoint, parameters, cURL example, error handling, and SDK samples."
weight: 65
ArticleTitle: "Add a Color Filter in an Excel Worksheet using Aspose.Cells Cloud API"
---
The **PutWorksheetColorFilter** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter`) enables developers to apply a color filter to a specified field within an Excel worksheet’s AutoFilter, allowing conditional highlighting or hiding of rows based on cell background or font color; it requires the workbook name, worksheet name, target range, field index, and a color filter request body, with optional parameters to match blank cells and refresh the filter.

This REST API adds a **color filter** to an Excel worksheet.

## The Put Worksheet Color Filter Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters:

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The workbook name. |
| sheetName | String | Path | The worksheet name. |
| range | String | Query | Represents the range to which the specified AutoFilter applies. |
| fieldIndex | Integer | Query | The integer offset of the field on which you want to base the filter (from the left of the list; the leftmost field is field 0). |
| colorFilter | class:colorfilterrequest | HTTPBody | color filter request. |
| matchBlanks | Boolean | Query | Match all blank cell in the list. |
| refresh | Boolean | Query | Refresh auto filters to hide or unhide the rows. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**`colorFilter` JSON schema**

| Property        | Type   | Description                                                                                                                    | Required |
| --------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------ | -------- |
| Pattern         | string | Filter pattern (e.g., `"Solid"`).                                                                                              | Yes      |
| ForegroundColor | object | Defines the foreground color. Contains sub‑properties such as `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor`, and `Type`. | No       |
| BackgroundColor | object | Defines the background color. Same sub‑properties as `ForegroundColor`.                                                        | No       |

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
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the PutWorksheetColorFilter API with SDKs

### PutWorksheetColorFilter API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**See also:** [Add a custom filter](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Add a date filter](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Remove an auto filter](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).
