---
title: "Convert List Object to Range – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Conversion"
type: docs
url: /list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, convert list object to range, Excel REST API"
description: "Learn how to convert an Excel ListObject (table) to a Range using Aspose.Cells Cloud REST API. Includes request syntax, parameters, sample cURL, response schema, authentication details, error codes, and SDK examples."
weight: 30
---

This REST API converts a **ListObject (table)** to a **Range** within an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### Request Parameters

| Name                | Type    | Location | Required | Default | Description                                                 |
| ------------------- | ------- | -------- | -------- | ------- | ----------------------------------------------------------- |
| **name**            | string  | path     | Yes      | –       | The name of the Excel file.                                 |
| **sheetName**       | string  | path     | Yes      | –       | The name of the worksheet that contains the ListObject.     |
| **listObjectIndex** | integer | path     | Yes      | –       | Zero‑based index of the ListObject (table) to be converted. |
| **folder**          | string  | query    | No       | –       | Folder path where the file is stored.                       |
| **storageName**     | string  | query    | No       | –       | Name of the storage service.                                |

### cURL Example (Request)

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your‑jwt‑token>"
```

{{< /tab >}}

#### Response Schema

The API returns a **200 OK** response with details of the newly created range.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Field           | Type    | Description                                        |
| --------------- | ------- | -------------------------------------------------- |
| **Code**        | integer | HTTP‑like status code (200 indicates success).     |
| **Status**      | string  | Textual status message.                            |
| **RangeName**   | string  | The name assigned to the created range.            |
| **Address**     | string  | Full address of the range, including sheet name.   |
| **FirstRow**    | integer | Zero‑based index of the first row in the range.    |
| **FirstColumn** | integer | Zero‑based index of the first column in the range. |
| **RowCount**    | integer | Number of rows in the range.                       |
| **ColumnCount** | integer | Number of columns in the range.                    |

### Error Codes

| Code | Meaning               | When it occurs                                                            |
| ---- | --------------------- | ------------------------------------------------------------------------- |
| 400  | Bad Request           | The `listObjectIndex` is out of range or required parameters are missing. |
| 401  | Unauthorized          | Missing or invalid JWT token.                                             |
| 404  | Not Found             | The specified workbook, worksheet, or ListObject does not exist.          |
| 500  | Internal Server Error | An unexpected server‑side error occurred.                                 |

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}
