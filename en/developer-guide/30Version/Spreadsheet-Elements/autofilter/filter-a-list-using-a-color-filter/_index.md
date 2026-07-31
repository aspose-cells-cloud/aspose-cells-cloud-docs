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
ArticleTitle: "Add a Color Filter in an Excel Worksheet using Aspose.Cells Cloud API"
---

Learn how to add a color filter to an Excel worksheet using the Aspose.Cells Cloud API. This guide covers the required endpoint, parameters, authentication prerequisites, sample cURL request, SDK examples, and response handling.

## REST API

This REST API adds a **color filter** to an Excel worksheet.

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Prerequisites**

- Obtain a JWT token using your client ID and client secret via the authentication endpoint.  
- Include the token in the `Authorization: Bearer <jwt token>` header for every request.  
- Use API version **v3.0** (the endpoint shown above).  
- Ensure the Excel file resides in a supported storage (e.g., Aspose Cloud Storage) and specify the correct `folder` and `storageName` parameters if needed.

### Request Parameters:


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

### **Response**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response confirms the operation. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


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