---
title: "Delete a filter in an Excel worksheet"
second_title: "Document"
linktitle: "Delete filter"
type: docs
url: /delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/,/delete-auto-filter/]
keywords: "Aspose.Cells Cloud, Excel, delete filter, worksheet, REST API, SDK"
description: "The Aspose.Cells Cloud API enables deleting a filter from an Excel worksheet. SDKs are available for multiple development languages, including Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 100
---

This REST API deletes a **filter** on an Excel worksheet.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

The request parameters are:

| Parameter Name          | Type    | Location | Description                                                            |
|--------------------------|---------|----------|------------------------------------------------------------------------|
| **name**                | string  | Path     | The workbook name.                                                     |
| **sheetName**           | string  | Path     | The worksheet name.                                                    |
| **range**               | string  | Query    | The cell range to which the filter applies (e.g., `A1:C10`).          |
| **fieldIndex**          | integer | Query    | Zero‑based index of the column to which the filter is applied.        |
| **dateTimeGroupingType**| string  | Query    | How date/time values are grouped: `Day`, `Hour`, `Minute`, `Month`, `Second`, or `Year`. |
| **year**                | integer | Query    | Year component for date grouping.                                      |
| **month**               | integer | Query    | Month component for date grouping.                                     |
| **day**                 | integer | Query    | Day component for date grouping.                                       |
| **hour**                | integer | Query    | Hour component for date grouping.                                      |
| **minute**              | integer | Query    | Minute component for date grouping.                                    |
| **second**              | integer | Query    | Second component for date grouping.                                    |
| **matchBlanks**         | string  | Query    | `true` / `false` – whether blank cells are included in the filter.     |
| **refresh**             | string  | Query    | `true` / `false` – whether to refresh the worksheet after deletion.    |
| **folder**              | string  | Query    | Original workbook folder.                                              |
| **storageName**         | string  | Query    | Storage name.                                                          |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API using cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&criteria=Year" \
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