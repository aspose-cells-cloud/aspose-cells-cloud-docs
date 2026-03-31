---
title: "Change Column Widths Inside a Range"
second_title: "Document"
linktitle: "Column width"
type: docs
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, column width, REST API, Excel, SDK, range, cloud"
description: "Learn how to change column widths inside a range using Aspose.Cells Cloud REST API or SDKs (C#, Java, Python, etc.). Includes cURL, request/response details, and authentication steps."
weight: 74
---

This REST API sets the column width of a range.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Prerequisites** – Before calling the endpoint you must:

1. Create an Aspose Cloud account and obtain a *client ID* and *client secret*.  
2. Request a JWT token by calling the OAuth endpoint (`/connect/token`). The token is returned in the `access_token` field.  
3. Upload the target workbook to your Aspose Cloud storage (or ensure it already exists in the specified folder).  

The request parameters are:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| name           | string | path     | Name of the workbook file |
| sheetName      | string | path     | Name of the worksheet |
| value          | number | query    | Desired column width value |
| range          | object | body     | Range object that defines the target cells |
| folder         | string | query    | Folder path where the workbook is stored |
| storageName    | string | query    | Name of the storage service |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Call the column‑width endpoint for workbook *test.xlsx*,
# worksheet *Sheet1*, setting the width of the selected columns to 20 points.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
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

*Possible error responses*  

| HTTP Code | Description                               |
|-----------|-------------------------------------------|
| 400       | Bad Request – invalid JSON or parameters |
| 401       | Unauthorized – missing or invalid token   |
| 404       | Not Found – workbook or worksheet absent   |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *What endpoint do I call to set the column width of a range in an Excel workbook?*  
**A:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth` where `{name}` is the workbook file name and `{sheetName}` is the target worksheet.

**Q:** *How do I authenticate the request when using the column‑width API?*  
**A:** Include an `Authorization: Bearer <jwt token>` header. Obtain the JWT token via the Aspose Cloud OAuth flow (`/connect/token`) using your client ID and client secret.

**Q:** *What JSON body should I send to change the width of columns A‑C to 25 points?*  
**A:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Add the query parameter `value=25` to the request URL.