---
title: "Delete a Row in an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Row"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "Delete a row from an Excel worksheet using Aspose.Cells Cloud REST API DELETE /rows endpoint with SDK support."
keywords: "Aspose.Cells, delete row, Excel, API, REST, Cloud, SDK"
weight: 80
ArticleTitle: "Delete a Row in an Excel Worksheet – Aspose.Cells Cloud API Guide"
---

This REST API deletes a row from an Excel worksheet.

## The Delete Worksheet Row API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Request parameters**

| Parameter Name      | Type    | Path / Query | Required | Description                                                                                         |
| ------------------- | ------- | ------------ | -------- | --------------------------------------------------------------------------------------------------- |
| **name**            | string  | path         | Yes      | The workbook name.                                                                                  |
| **sheetName**       | string  | path         | Yes      | The worksheet name.                                                                                 |
| **rowIndex**        | integer | path         | Yes      | Zero‑based index of the row to delete.                                                              |
| **startrow**        | integer | query        | No       | Index of the first row to delete (normally the same as `rowIndex`).                                 |
| **totalRows**       | integer | query        | No       | Number of consecutive rows to delete.                                                               |
| **updateReference** | boolean | query        | No       | When `true` (default), formulas, named ranges, and other references are updated after the deletion. |
| **folder**          | string  | query        | No       | Folder that contains the workbook.                                                                  |
| **storageName**     | string  | query        | No       | Name of the storage service.                                                                        |

**Possible HTTP response codes**

| Code | Meaning               | Description                                                   |
| ---- | --------------------- | ------------------------------------------------------------- |
| 200  | OK                    | The row was deleted successfully.                             |
| 400  | Bad Request           | Missing or invalid parameters (e.g., non‑numeric `rowIndex`). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                 |
| 404  | Not Found             | Specified workbook, worksheet, or row does not exist.         |
| 500  | Internal Server Error | Unexpected server error; see error response for details.      |

**Error response example**

```json
{
  "Code": 400,
  "Message": "Invalid row index supplied."
}
```

## How to Use the Delete Worksheet Row API with SDKs?

### Delete Worksheet Row API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow" rel="noopener noreferrer">Delete Worksheet Row API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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

**Related operations**

- [Add a Row](/cells/rows/add/row/)
- [Delete Multiple Rows](/cells/rows/delete/rows/)
- [Get Row Details](/cells/rows/get/row/)
