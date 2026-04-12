---
title: "Add a List Object (Table) to an Excel Worksheet"
second_title: "Document"
linktitle: "Add"
type: docs
url: /list-objects/add/
aliases: [/add-a-list-object-or-table-inside-the-worksheet/, /tables/add/]
keywords: "Aspose.Cells Cloud, Excel API, add list object, table, REST, worksheet"
description: "Learn how to add a list object (Excel table) to a worksheet using Aspose.Cells Cloud REST API. Includes endpoint, parameters, authentication steps, cURL example, and SDK code samples."
weight: 10
---

This REST API adds a **list object (table)** to an Excel worksheet.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Request parameters

| Parameter Name  | Type    | Location | Description                                                         |
| --------------- | ------- | -------- | ------------------------------------------------------------------- |
| **name**        | string  | path     | Workbook file name.                                                 |
| **sheetName**   | string  | path     | Worksheet name.                                                     |
| **startRow**    | integer | query    | Zero‑based index of the first row of the table range.               |
| **startColumn** | integer | query    | Zero‑based index of the first column of the table range.            |
| **endRow**      | integer | query    | Zero‑based index of the last row of the table range.                |
| **endColumn**   | integer | query    | Zero‑based index of the last column of the table range.             |
| **hasHeaders**  | boolean | query    | `true` if the first row contains column headers; otherwise `false`. |
| **listObject**  | object  | body     | Definition of the list object (see **Request body schema**).        |
| **folder**      | string  | query    | Folder that contains the workbook.                                  |
| **storageName** | string  | query    | Storage name.                                                       |

### Request body schema

The **listObject** object describes the table that will be created. Only the most common properties are shown; see the OpenAPI specification for the complete list.

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Example request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Example response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error codes

| HTTP Status | Reason                | Description                                      |
| ----------- | --------------------- | ------------------------------------------------ |
| **400**     | Bad Request           | Invalid range parameters or malformed JSON body. |
| **401**     | Unauthorized          | Missing or expired JWT token.                    |
| **404**     | Not Found             | Specified workbook or worksheet does not exist.  |
| **500**     | Internal Server Error | Unexpected server‑side failure.                  |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) provides the full contract for this operation.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
