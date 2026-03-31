---
title: "Add a color filter in an Excel worksheet"
second_title: "Document"
linktitle: "Add color filter"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: "Excel, color filter, Aspose.Cells Cloud, REST API, auto filter, JWT authentication"
description: "Learn how to apply a color filter to an Excel worksheet with Aspose.Cells Cloud API. Includes endpoint, parameters, cURL example, error handling, and SDK samples."
weight: 65
---

This REST API adds a **color filter** to an Excel worksheet.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

**Prerequisites** – The endpoint requires OAuth 2.0 authentication. Obtain a JWT token as described in the Aspose.Cells Cloud authentication guide and pass it in the request header as `Authorization: Bearer <jwt token>`. The API version is **v3.0**, and the workbook must be stored in Aspose Cloud Storage (or another supported storage) before the call.

The request parameters are:

| Parameter Name | Type    | Location | Description                                                                 |
|----------------|---------|----------|-----------------------------------------------------------------------------|
| name           | string  | path     | The name of the Excel file.                                                 |
| sheetName      | string  | path     | The name of the worksheet that contains the data to be filtered.           |
| range          | string  | query    | The cell range to which the filter is applied (e.g., `A1:B10`).            |
| fieldIndex     | integer | query    | Zero‑based index of the column on which the color filter is applied.       |
| colorFilter    | object  | body     | JSON object that defines the foreground and background colors to filter.   |
| matchBlanks    | boolean | query    | Whether rows with blank cells should be included in the filter results.   |
| refresh        | boolean | query    | If `true`, the worksheet is refreshed after applying the filter.           |
| folder         | string  | query    | The folder in storage where the Excel file is located.                      |
| storageName    | string  | query    | The name of the storage service (e.g., Aspose Cloud Storage).              |

**`colorFilter` JSON schema**

| Property          | Type   | Description                                                                    | Required |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | string | Filter pattern (e.g., `"Solid"`).                                             | Yes      |
| ForegroundColor   | object | Defines the foreground color. Contains sub‑properties such as `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor`, and `Type`. | No |
| BackgroundColor   | object | Defines the background color. Same sub‑properties as `ForegroundColor`.      | No |

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

**Error handling** – The API may return standard error objects. Example responses:

```json
// 400 Bad Request – missing or invalid parameters
{
  "Code": 400,
  "Message": "Invalid request parameters."
}
```

```json
// 401 Unauthorized – authentication failed or token missing
{
  "Code": 401,
  "Message": "Authentication failed. Please provide a valid JWT token."
}
```

## Cloud SDK Family

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