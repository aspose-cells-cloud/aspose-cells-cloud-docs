---  
title: "Set Cell Value – Aspose.Cells Cloud API Reference (v3.0)"  
type: docs  
url: /set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "Aspose Cells API set cell value, Excel cell update REST, Aspose.Cells Cloud cURL example"  
description: "Learn how to set the value of a specific cell in an Excel worksheet using Aspose.Cells Cloud REST API. Includes request syntax, parameters, HTTPS cURL example, and SDK code samples."  
---  

> **Version Notice:** This documentation applies to API version **v3.0**. Newer versions (e.g., v3.1, v4) may be available; refer to the changelog for the latest information.  

This REST API sets the **cell value** in an Excel file.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

All requests must be sent over **HTTPS**. The API requires a **JWT bearer token** obtained from the Aspose Cloud OAuth endpoint. Include the token in the `Authorization` header as `Bearer <jwt token>`.

**Request parameters**

| Name          | Type   | Location | Description                                   |
|---------------|--------|----------|-----------------------------------------------|
| name          | string | path     | Name of the Excel document (including extension). |
| sheetName     | string | path     | Name of the worksheet (case‑sensitive). |
| cellName      | string | path     | A1‑style address of the target cell (e.g., `A1`). |
| value         | string | query    | Value to assign to the cell. |
| type          | string | query    | Data type of the value (`int`, `string`, `float`, etc.). |
| formula       | string | query    | Formula to apply to the cell (optional). |
| folder        | string | query    | Folder that contains the document (optional). |
| storageName   | string | query    | Name of the storage where the file resides (optional). |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) defines a publicly accessible programming interface, which enables developers to invoke REST endpoints directly from a browser or any HTTP client.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The example below demonstrates how to set a cell value with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
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

**Error handling**

| HTTP Status | Description                              | Example payload |
|-------------|------------------------------------------|-----------------|
| 400         | Bad request – missing or invalid parameters. | `{"Code":400,"Message":"Invalid parameter 'value'."}` |
| 401         | Unauthorized – JWT token is missing or invalid. | `{"Code":401,"Message":"Authentication failed."}` |
| 404         | Not found – the specified file, worksheet, or cell does not exist. | `{"Code":404,"Message":"Worksheet not found."}` |
| 500         | Internal server error – unexpected condition on the server. | `{"Code":500,"Message":"An unexpected error occurred."}` |

## Cloud SDK Family  

Using an SDK speeds up development by handling low‑level details so you can focus on your project. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples show how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}