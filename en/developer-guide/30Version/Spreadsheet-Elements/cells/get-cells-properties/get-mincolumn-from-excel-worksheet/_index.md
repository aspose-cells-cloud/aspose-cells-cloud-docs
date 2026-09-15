---
title: "Get MinColumn from Excel Worksheet"
type: docs
url: /get-mincolumn-from-excel-worksheet/
weight: 100
date: 2024-05-10
keywords: "Excel API, REST API tutorial, cloud spreadsheet SDK, Aspose.Cells Cloud, Get MinColumn, Worksheet, SDK, Cloud API"
description: "Learn how to programmatically retrieve the minimum column index with data in an Excel worksheet using Aspose.Cells Cloud REST API, including cURL and SDK examples."
ArticleTitle: "Get MinColumn from Excel Worksheet - Aspose.Cells Cloud API"
robots: index, follow
---

This REST API returns the minimum column index that contains data in an Excel worksheet when the `cellOrMethodName` parameter is set to `mincolumn`.

- **cURL Example**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer `YOUR_ACCESS_TOKEN`" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Request details**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `cellOrMethodName` | string | Yes | Fixed value `mincolumn` to indicate the operation. |
| `folder` | string | No | Path to the folder containing the workbook (if not the root). |
| `storageName` | string | No | Name of the Aspose Cloud storage to use. |

**Response details**

The API returns a JSON object with a single property:

```json
{
  "MinColumn": integer   // Zero‑based index of the left‑most column that contains data.
}
```

Typical HTTP status codes:

- **200 OK** – Successful request, returns the `MinColumn` value.  
- **401 Unauthorized** – Missing or invalid authentication token.  
- **404 Not Found** – The specified workbook, worksheet, or cell range does not exist.  
- **500 Internal Server Error** – Unexpected server error.

- **Use Aspose.Cells Cloud SDKs**

Using an SDK is the most efficient way to develop. An SDK abstracts low‑level details, allowing you to focus on your project logic. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" target="_blank">Aspose.Cells Cloud SDKs on GitHub</a> for a complete list of Aspose.Cells Cloud SDKs.

> All SDK examples are compatible with the latest stable release (v23.12+). For older versions, consult the [version matrix](#).

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< note >}}Swift example coming soon.{{< /note >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}