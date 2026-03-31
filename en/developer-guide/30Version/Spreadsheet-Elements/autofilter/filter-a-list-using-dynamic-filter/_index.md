---
title: "Add a dynamic filter in an Excel worksheet"
second_title: "Document"
linktitle: "Add dynamic filter"
type: docs
url: /autofilter/add-dynamic-filter/
aliases:
  - /filter-a-list-using-dynamic-filter/
  - /autofilter/add-a-dynamic-filter/
keywords: "Aspose.Cells, dynamic filter, Excel API, REST, auto filter, cloud SDK"
description: "Learn how to apply a dynamic filter (e.g., BelowAverage, Tomorrow, LastMonth) to an Excel worksheet using the Aspose.Cells Cloud REST API. Includes cURL, SDK snippets, authentication guidance, and error handling."
weight: 65
---

This REST API adds a **dynamic filter** to an Excel worksheet.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Request parameters

| Parameter Name       | Type    | Location | Description                                                                                           |
|----------------------|---------|----------|-------------------------------------------------------------------------------------------------------|
| **name**             | string  | path     | The name of the Excel file (e.g., `Book1.xlsx`).                                                      |
| **sheetName**        | string  | path     | The name of the worksheet that contains the range to be filtered.                                    |
| **range**            | string  | query    | The cell range on which the filter is applied (e.g., `A1:B1`).                                        |
| **fieldIndex**       | integer | query    | Zero‑based index of the column within the range to which the dynamic filter is applied.              |
| **dynamicFilterType**| string  | query    | The type of dynamic filter. Supported values are listed below.                                        |
| **matchBlanks**      | boolean | query    | Indicates whether blank cells should be included in the filter results.                             |
| **refresh**          | boolean | query    | If `true`, the filter is refreshed after being applied.                                               |
| **folder**           | string  | query    | The folder path in storage where the workbook is located.                                            |
| **storageName**      | string  | query    | The name of the Aspose Cloud storage to use.                                                          |

**Supported `dynamicFilterType` values**

- `BelowAverage` – rows whose value is below the column’s average.  
- `AboveAverage` – rows whose value is above the column’s average.  
- `Tomorrow` – rows with dates equal to tomorrow’s date.  
- `Yesterday` – rows with dates equal to yesterday’s date.  
- `NextWeek` – rows with dates falling in the next calendar week.  
- `LastMonth` – rows with dates from the previous month.  
- `ThisYear` – rows with dates occurring in the current year.  
- *(and other built‑in date/statistical conditions offered by the API).*

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDynamicFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL. **First obtain a JWT token** by authenticating against the `/connect/token` endpoint and replace `<jwt token>` with the token value.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
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

*Error responses*  
The API can also return the following error codes:

| HTTP Status | Description                               | Sample Body |
|-------------|-------------------------------------------|-------------|
| 400         | Invalid request parameters                | `{ "Code":400, "Message":"Invalid parameter value." }` |
| 401         | Unauthorized – missing or invalid token   | `{ "Code":401, "Message":"Authentication failed." }` |
| 404         | Resource not found (e.g., workbook)      | `{ "Code":404, "Message":"File not found." }` |
| 500         | Internal server error                     | `{ "Code":500, "Message":"Unexpected error." }` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the most efficient way to develop. An SDK abstracts low‑level details so you can focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDynamicFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDynamicFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDynamicFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDynamicFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDynamicFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDynamicFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDynamicFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDynamicFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}