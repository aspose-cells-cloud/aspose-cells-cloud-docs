---
title: "Delete All Pivot Tables in an Excel Worksheet"
second_title: "Documentation"
linktitle: Clear
type: docs
url: /pivot-tables/clear/
aliases: [/delete-worksheet-pivot-tables/]
keywords: "Aspose.Cells, delete pivot tables, Excel API, REST, cloud, pivot table clear, worksheet"
description: "Learn how to delete every pivot table from a worksheet using Aspose.Cells Cloud REST API. Includes endpoint, required parameters, cURL request, response, and SDK examples for C#, Java, Python, Node.js, and more."
weight: 80
---

When you need to reset a worksheet’s analysis, you can remove all pivot tables in a single call. This REST API deletes all pivot tables from a worksheet.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Request parameters

| Parameter Name | Type   | Location | Description                                                         |
|----------------|--------|----------|---------------------------------------------------------------------|
| **name**       | string | path     | **Required.** The name of the Excel file.                           |
| **sheetName**  | string | path     | **Required.** The name of the worksheet.                            |
| **folder**     | string | query    | The folder that contains the file (optional).                       |
| **storageName**| string | query    | The storage name to use (optional).                                 |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

### Authentication

All calls must be made over TLS 1.2 or higher. Obtain a JWT access token with the appropriate scope and include it in the `Authorization` header:

```
Authorization: Bearer <jwt token>
```

### cURL example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error handling

| HTTP Status | Meaning                              | Example error payload |
|-------------|--------------------------------------|-----------------------|
| 400         | Bad Request – missing or invalid parameters | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| 401         | Unauthorized – invalid or expired JWT | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| 404         | Not Found – file or worksheet does not exist | `{ "Code": 404, "Message": "Worksheet not found." }` |
| 500         | Internal Server Error – unexpected failure | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

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