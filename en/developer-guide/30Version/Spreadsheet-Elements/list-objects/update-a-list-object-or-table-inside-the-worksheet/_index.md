---
title: "Update a List Object in an Excel Worksheet"
second_title: "Document"
linktitle: "Update"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "update list object, Excel worksheet, Aspose.Cells Cloud, REST API, table, cells API"
description: "Learn how to update an Excel table using Aspose.Cells Cloud API (v3.0). Includes endpoint, parameters, sample cURL, error codes, and SDK examples."
weight: 20
---

This REST API updates the properties of a **list object** (table) in an Excel worksheet.

## Request Body Schema

The `listObject` DTO contains the following fields. Only the fields you need to change are required in the request body.

| Field                                           | Type             | Required | Description                                                                |
| ----------------------------------------------- | ---------------- | -------- | -------------------------------------------------------------------------- |
| **DisplayName**                                 | string           | optional | The name displayed for the table.                                          |
| **StartRow** / **StartColumn**                  | integer          | optional | Zero‑based index of the first row/column of the table.                     |
| **EndRow** / **EndColumn**                      | integer          | optional | Zero‑based index of the last row/column of the table.                      |
| **Range**                                       | string           | optional | A‑1 style address that defines the table range (e.g., `A1:D10`).           |
| **ShowHeaderRow**                               | boolean          | optional | `true` to display the header row.                                          |
| **ShowTotals**                                  | boolean          | optional | `true` to display the totals row.                                          |
| **TableStyleName**                              | string           | optional | Name of the built‑in table style to apply.                                 |
| **TableStyleType**                              | string           | optional | Style type (`TableStyleLight`, `TableStyleMedium`, etc.).                  |
| **ListColumns**                                 | array of objects | optional | Collection of column definitions (`Name`, `TotalsCalculation`).            |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | object           | optional | Advanced styling and filtering options (see full DTO in the OpenAPI spec). |

### Minimal Example Payload

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Request parameters**

| Parameter Name      | Type    | Location | Description                         |
| ------------------- | ------- | -------- | ----------------------------------- |
| **name**            | string  | path     | Document name.                      |
| **sheetName**       | string  | path     | Worksheet name.                     |
| **listObjectIndex** | integer | path     | Index of the list object to update. |
| **listObject**      | object  | body     | ListObject DTO in the request body. |
| **folder**          | string  | query    | Folder that contains the document.  |
| **storageName**     | string  | query    | Name of the storage.                |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Request

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Response

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Error Responses

| HTTP Code | Description                                                                   | Sample Payload                                         |
| --------- | ----------------------------------------------------------------------------- | ------------------------------------------------------ |
| **400**   | Bad request – missing required fields or malformed JSON.                      | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**   | Unauthorized – JWT token is missing or invalid.                               | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Not found – the specified workbook, worksheet, or list object does not exist. | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**   | Internal server error – unexpected condition on the server side.              | `{ "Code": 500, "Message": "Server error." }`          |

## FAQ

<details>  
<summary>How do I update a list object using the Aspose.Cells Cloud API?</summary>

Use the `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}` endpoint. Include a JSON body with the properties you wish to change (e.g., `DisplayName`, `ShowHeaderRow`). Authenticate with a JWT token in the `Authorization` header.

</details>

<details>  
<summary>What response do I receive after a successful update?</summary>

A JSON object with `Code: 200` and `Status: "OK"` is returned. If an error occurs, the response contains the appropriate HTTP status code and an `Error` object describing the problem.

</details>

<details>  
<summary>Can I update only a subset of list object properties?</summary>

Yes. Include only the fields you want to modify in the request body; all omitted fields remain unchanged.

</details>

## Related Documentation

- [Add a List Object](https://docs.aspose.cloud/cells/list-objects/add/)
- [Get List Object](https://docs.aspose.cloud/cells/list-objects/get/)
- [Delete List Object](https://docs.aspose.cloud/cells/list-objects/delete/)

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
