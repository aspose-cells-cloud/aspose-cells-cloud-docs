---
title: "Get MinDataRow from Excel Worksheet"
type: docs
url: /get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose.Cells Cloud API, MinDataRow, Excel, REST, v3.0, worksheet, cellOrMethodName"
description: "Retrieve the minimum data row index of a worksheet using Aspose.Cells Cloud API v3.0. Includes authentication steps, request pattern, parameters table, sample cURL, response schema, error codes, and SDK examples."
---

The **Get MinDataRow** endpoint of **Aspose.Cells Cloud API v3.0** returns the index of the first row that contains data in a specified worksheet. The operation requires a valid access token (Bearer authentication) and the query parameter `cellOrMethodName` set to `mindatarow`.

## **cURL Example**

The request uses the HTTP GET method. Replace the placeholders `{fileName}` and `{sheetName}` with the actual workbook and worksheet names.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

### **Parameters**

| Name               | Type   | Required | Description                                             |
| ------------------ | ------ | -------- | ------------------------------------------------------- |
| `cellOrMethodName` | string | Yes      | Must be set to **mindatarow** to invoke this operation. |
| `folder`           | string | No       | Path to the folder containing the workbook.             |
| `storage`          | string | No       | Name of the Aspose Cloud storage to use.                |

### **Response**

A successful call returns HTTP 200 with a JSON payload that contains the minimum data‑row index (0‑based).

```json
{
  "MinDataRow": 5
}
```

### **Error Handling**

| HTTP Status | Code          | Message                  | When it occurs                                              |
| ----------- | ------------- | ------------------------ | ----------------------------------------------------------- |
| 400         | BadRequest    | Invalid query parameter. | `cellOrMethodName` missing or set to an unsupported value.  |
| 401         | Unauthorized  | Authentication failed.   | Missing or invalid Bearer token.                            |
| 404         | FileNotFound  | Worksheet not found.     | The specified `{fileName}` or `{sheetName}` does not exist. |
| 500         | InternalError | Unexpected server error. | Server‑side problem while processing the request.           |

**See Also**

- [Get MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MinRow](https://docs.aspose.cloud/cells/get-minrow-from-excel-worksheet/)
- [Authentication Guide](https://docs.aspose.cloud/cells/authentication/)

- **Cloud SDK Family**

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}
