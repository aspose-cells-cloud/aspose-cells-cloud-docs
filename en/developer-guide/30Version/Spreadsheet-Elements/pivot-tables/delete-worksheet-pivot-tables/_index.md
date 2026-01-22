---
title: "Delete all pivot tables in an Excel worksheet"
second_title: "Document"
linktitle: Clear
type: docs
url: /pivot-tables/clear/
aliases: [/delete-worksheet-pivot-tables/]
keywords: "Aspose.Cells Cloud, REST API, delete pivot tables, Excel worksheet, PivotTables"
description: "Learn how to use the Aspose.Cells Cloud REST API to delete all pivot tables from a worksheet in an Excel file. Includes the HTTP request, cURL example, and SDK snippets for multiple programming languages."
weight: 80
---

This REST API deletes all pivot tables in a worksheet.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Request parameters

| Parameter Name | Type   | Location | Description                     |
|----------------|--------|----------|---------------------------------|
| name           | string | path     | The name of the Excel file.     |
| sheetName      | string | path     | The name of the worksheet.      |
| folder         | string | query    | The folder that contains the file. |
| storageName    | string | query    | The storage name to use.        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The example below shows how to delete all pivot tables in a worksheet.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
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

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK speeds up development. An SDK abstracts low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call the Aspose.Cells web service using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTable-delete-worksheet-pivot-table.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTables.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTable-delete-worksheet-pivot-table.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "12f056c6733b4961979d35a32ef99e61" >}}

{{< /tab >}}

{{< /tabs >}}