---
title: "Delete row on an Excel worksheet"
second_title: "Document"
linktitle: "Row"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
keywords: "Delete row Excel worksheet, Aspose.Cells Cloud, REST API, Excel row deletion, SDK examples"
description: "Use Aspose.Cells Cloud REST API to delete a row from an Excel worksheet. The API is available through cURL and multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)."
weight: 80
---

This REST API deletes a row from an Excel worksheet.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

The request parameters are:

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                 |
|----------------|---------|----------------------------|---------------------------------------------|
| name           | string  | path                       | The workbook name.                          |
| sheetName      | string  | path                       | The worksheet name.                         |
| rowIndex       | integer | path                       | The zero‑based index of the row to delete.  |
| folder         | string  | query                      | The folder containing the workbook.         |
| storageName    | string  | query                      | The storage name.                           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/" \
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

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

## Introduction

This example shows how to delete a row from an Excel worksheet using Aspose.Cells Cloud API in your applications. You can use the REST API with any language: .NET, Java, PHP, Ruby, Python, JavaScript, and many more.

## API Information

| API                                   | Type | Description                         | Resource Link |
|---------------------------------------|------|-------------------------------------|---------------|
| /cells/{name}/worksheets/{sheetName}/cells/rows | POST | Delete rows from an Excel worksheet | [DeleteWorksheetRows](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) |

### cURL Example

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" -H "accept: application/json"
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

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}