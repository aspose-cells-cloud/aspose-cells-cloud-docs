---
title: "Set Row Height for a Range in Excel – Aspose.Cells Cloud API (v3.0)"
second_title: "Document"
linktitle: "Row height"
type: docs
url: /ranges/update/row-height/
aliases: [/change-heights-of-rows-inside-the-range/]
keywords: "row height, range, Excel, Aspose.Cells Cloud, REST API, SDK, cURL"
description: "Learn how to change the height of rows within a specific range of an Excel worksheet using the Aspose.Cells Cloud REST API. Includes endpoint, parameters, cURL example, and SDK code snippets for C#, Java, Python, and more."
weight: 76
---

This REST API sets the row height of a range on an Excel worksheet.

## Prerequisites / Authentication

To call the **Set Row Height for a Range** endpoint you must obtain a JWT access token from the Aspose Cloud OAuth service.  
The token must contain the **Cells.ReadWrite** scope and is passed in the request header:

```http
Authorization: Bearer <jwt token>
```

If you do not yet have a token, follow the steps in the Aspose Cloud authentication guide to request one.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight
```

### Request parameters

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **name**       | string | Path     | The name of the Excel file stored in the cloud. |
| **sheetName**  | string | Path     | The name of the worksheet that contains the target range. |
| **value**      | number | Query    | The desired row height (in points) to apply to the range. |
| **range**      | object | Body (JSON) | JSON object that defines the range (e.g., start row, row count, etc.). |
| **folder**     | string | Query    | Folder path in storage where the file is located. |
| **storageName**| string | Query    | The name of the storage service (if multiple storages are configured). |

#### Range JSON Schema
The **range** object must contain the following properties:

- **FirstRow** *(integer, required)* – Zero‑based index of the first row in the range.  
- **RowCount** *(integer, required)* – Number of rows the operation should affect.  
- **FirstColumn** *(integer, optional)* – Zero‑based index of the first column (if needed).  
- **ColumnCount** *(integer, optional)* – Number of columns the range spans (optional for row‑height only).

Only the properties listed above are required for the row‑height operation; any additional fields will be ignored.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "FirstRow": 9,
    "RowCount": 1
  }'
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

## Response Details

| HTTP Status | Description | Example Payload |
|-------------|-------------|-----------------|
| **200 OK** | The row height was updated successfully. | `{ "Code": 200, "Status": "OK" }` |
| **400 Bad Request** | Missing or invalid parameters (e.g., negative height). | `{ "Code": 400, "Message": "Invalid row height value." }` |
| **401 Unauthorized** | No token supplied or token is invalid/expired. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **500 Internal Server Error** | An unexpected server‑side error occurred. | `{ "Code": 500, "Message": "Internal server error." }` |

The response always contains a **Code** (numeric HTTP status) and a **Message** (human‑readable description). When an error occurs, additional **ErrorDetails** may be provided.

## Cloud SDK Family

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. SDKs handle low‑level details, allowing you to focus on your business logic. Check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call the **Set Row Height for Range** operation using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeRowHeight.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeRowHeight.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeRowHeight.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeRowHeight.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeRowHeight.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeRowHeight.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeRowHeight.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeRowHeight.go" >}}

{{< /tab >}}

{{< /tabs >}}