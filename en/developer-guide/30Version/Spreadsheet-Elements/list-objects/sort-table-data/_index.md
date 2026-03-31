---
title: "Sort ListObject Data in an Excel Worksheet"
second_title: "Document"
linktitle: "Sort"
type: docs
url: /list-objects/sort-data/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, list object, sort data, REST API, worksheet"
description: "Learn how to sort ListObject (table) data in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, sample cURL request, and SDK examples."
weight: 40
---

This REST API sorts a table’s data in an Excel worksheet.  
To use this operation, provide the workbook name, worksheet name, and the index of the target ListObject, together with a `dataSorter` JSON body that defines the sorting criteria.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

The request parameters are:

| Parameter Name   | Type    | Path/Query String/HTTPBody | Description |
|------------------|---------|----------------------------|-------------|
| name             | string  | path                       | The name of the Excel file stored in Aspose Cloud storage. |
| sheetName        | string  | path                       | The name of the worksheet that contains the ListObject. |
| listObjectIndex  | integer | path                       | Zero‑based index of the ListObject (table) within the worksheet. |
| dataSorter       | object  | body                       | JSON object that specifies sorting options (e.g., `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder           | string  | query                      | Folder path in storage where the Excel file is located. |
| storageName      | string  | query                      | Name of the Aspose Cloud storage. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
-X POST \
-d '{ "CaseSensitive": true, "HasHeaders": true, "KeyList": [ { "Key": 1, "SortOrder": "Ascending", "CustomList": "string" } ], "SortLeftToRight": true}' \
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}