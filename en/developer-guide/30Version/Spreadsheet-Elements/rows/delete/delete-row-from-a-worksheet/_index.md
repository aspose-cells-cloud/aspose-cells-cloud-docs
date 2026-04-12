---
title: "Delete a Row in an Excel Worksheet"
second_title: "Document"
linktitle: "Row"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "Learn how to delete a specific row from an Excel worksheet using Aspose.Cells Cloud REST API. Includes a complete cURL command, SDK code samples, and a full parameter reference."
keywords: "Aspose.Cells delete row, Excel API delete row, REST delete worksheet row, Aspose Cloud SDK delete row"
weight: 80
---

This REST API deletes a row from an Excel worksheet.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Request parameters**

| Parameter Name      | Type    | Path / Query | Required | Description                                                                                         |
| ------------------- | ------- | ------------ | -------- | --------------------------------------------------------------------------------------------------- |
| **name**            | string  | path         | Yes      | The workbook name.                                                                                  |
| **sheetName**       | string  | path         | Yes      | The worksheet name.                                                                                 |
| **rowIndex**        | integer | path         | Yes      | Zero‑based index of the row to delete.                                                              |
| **startrow**        | integer | query        | Yes      | Index of the first row to delete (normally the same as `rowIndex`).                                 |
| **totalRows**       | integer | query        | Yes      | Number of consecutive rows to delete.                                                               |
| **updateReference** | boolean | query        | No       | When `true` (default), formulas, named ranges, and other references are updated after the deletion. |
| **folder**          | string  | query        | No       | Folder that contains the workbook.                                                                  |
| **storageName**     | string  | query        | No       | Name of the storage service.                                                                        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows a complete, executable call.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
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
