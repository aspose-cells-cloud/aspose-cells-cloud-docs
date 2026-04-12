---
title: "Delete a Filter from an Excel Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Delete filter"
type: docs
url: /delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud delete filter, Excel, REST API, SDK"
description: "Learn how to delete an AutoFilter from an Excel worksheet using Aspose.Cells Cloud REST API, cURL, and SDKs (C#, Java, Python, etc.). Includes endpoint, parameters, authentication, and sample code."
weight: 100
---

This REST API deletes an **AutoFilter** on an Excel worksheet.  
SDKs are available for multiple development languages, including Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

The request parameters are:

| Parameter Name           | Type    | Location | Required? | Description                                                                              |
| ------------------------ | ------- | -------- | --------- | ---------------------------------------------------------------------------------------- |
| **name**                 | string  | Path     | Yes       | The workbook name.                                                                       |
| **sheetName**            | string  | Path     | Yes       | The worksheet name.                                                                      |
| **range**                | string  | Query    | No        | The cell range to which the filter applies (e.g., `A1:C10`).                             |
| **fieldIndex**           | integer | Query    | Yes       | Zero‑based index of the column to which the filter is applied.                           |
| **dateTimeGroupingType** | string  | Query    | No        | How date/time values are grouped: `Day`, `Hour`, `Minute`, `Month`, `Second`, or `Year`. |
| **year**                 | integer | Query    | No        | Year component for date grouping.                                                        |
| **month**                | integer | Query    | No        | Month component for date grouping.                                                       |
| **day**                  | integer | Query    | No        | Day component for date grouping.                                                         |
| **hour**                 | integer | Query    | No        | Hour component for date grouping.                                                        |
| **minute**               | integer | Query    | No        | Minute component for date grouping.                                                      |
| **second**               | integer | Query    | No        | Second component for date grouping.                                                      |
| **matchBlanks**          | boolean | Query    | No        | `true` / `false` – whether blank cells are included in the filter.                       |
| **refresh**              | boolean | Query    | No        | `true` / `false` – whether to refresh the worksheet after deletion.                      |
| **folder**               | string  | Query    | No        | Original workbook folder.                                                                |
| **storageName**          | string  | Query    | No        | Storage name.                                                                            |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Step‑by‑step usage flow

1. **Obtain a JWT token** via the OAuth 2.0 authentication endpoint.
2. **Build the request URL** by replacing `{name}` and `{sheetName}` and adding required query parameters (at minimum `fieldIndex`).
3. **Send the DELETE request** with the `Authorization` header.
4. **Verify the response** – a successful call returns HTTP 200 with a JSON body indicating success.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API using cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

## Error Handling

| HTTP Status | Description                                                        | Example Response Body                                         |
| ----------- | ------------------------------------------------------------------ | ------------------------------------------------------------- |
| **400**     | Bad request – missing required fields or invalid parameter values. | `{ "Code": 400, "Message": "Invalid fieldIndex value." }`     |
| **401**     | Unauthorized – missing or invalid JWT token.                       | `{ "Code": 401, "Message": "Authentication failed." }`        |
| **404**     | Not found – workbook, worksheet, or filter does not exist.         | `{ "Code": 404, "Message": "Worksheet not found." }`          |
| **500**     | Internal server error – unexpected condition on the server side.   | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Cloud SDK Family

Using an SDK is the most efficient way to accelerate development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
