---
title: "Aspose.Cells Cloud API – Get MaxDataColumn of an Excel Worksheet (v3.0)"
type: docs
url: /get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, Get MaxDataColumn, Excel worksheet, REST API, v3.0, SDK"
description: "Retrieve the highest column index that contains data in a specified worksheet using the Aspose.Cells Cloud REST API (v3.0). Includes request details, sample response, and SDK examples."
ArticleTitle: "Aspose.Cells Cloud API – Get MaxDataColumn of an Excel Worksheet (v3.0)"
---

This REST API returns the maximum data‑column index in an Excel worksheet when the `cellOrMethodName` parameter is set to `maxdatacolumn`.

## **cURL Example**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**Request Details**  
- **HTTP Method:** `GET`  
- **Endpoint pattern:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **Path parameters:**  
  - `fileName` – Name of the Excel file (e.g., `myWorkbook.xlsx`).  
  - `sheetName` – Name of the worksheet (e.g., `Sheet1`).  
- **Headers:**  
  - `Authorization: Bearer <access_token>` (required)  
  - `Accept: application/json` (recommended)  

**Parameters**

| Parameter | Location | Type   | Required | Description |
|-----------|----------|--------|----------|-------------|
| `fileName` | Path     | string | Yes      | The Excel file name stored in the cloud storage. |
| `sheetName` | Path   | string | Yes      | The worksheet from which to obtain the maximum data column. |
| `cellOrMethodName` | Path | string | Yes | Must be set to `maxdatacolumn` to invoke this operation. |

**Responses**

| Status Code | Description                     | Example Payload |
|-------------|---------------------------------|-----------------|
| 200         | Success – returns the max data column index. | `{ "MaxDataColumn": 12 }` |
| 401         | Unauthorized – invalid or missing access token. | `{ "error": "Invalid authentication." }` |
| 404         | Not Found – file or worksheet does not exist. | `{ "error": "Resource not found." }` |
| 500         | Internal Server Error – unexpected condition. | `{ "error": "Server error." }` |

**Error Handling**  
If the request fails, inspect the HTTP status code and the `error` message in the response body. Ensure the access token is valid and the specified file and worksheet exist in your Aspose Cloud storage.

- **Use Aspose.Cells Cloud SDKs**

Using an SDK is the most efficient way to accelerate development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}