---
title: "Get MaxColumn from Excel Worksheet"
type: docs
url: /get-maxcolumn-from-excel-worksheet/
weight: 60
keywords: "Aspose Cells API, maxcolumn, Excel worksheet, REST, SDK"
description: "Retrieve the maximum column index of a worksheet using Aspose.Cells Cloud API. Includes cURL request with authentication, response schema, parameters, error codes, and SDK examples (C#, Java, Python, etc.)."
---

This REST API returns the maximum column index in an Excel worksheet when the `cellOrMethodName` parameter is set to `maxcolumn`.

## Parameters

| Parameter          | Type   | Required | Default | Description                                               |
| ------------------ | ------ | -------- | ------- | --------------------------------------------------------- |
| `cellOrMethodName` | string | **Yes**  | —       | Must be set to `maxcolumn` to invoke this method.         |
| `folder`           | string | No       | `""`    | Folder path in cloud storage where the workbook resides.  |
| `storage`          | string | No       | `""`    | Name of the storage service (if multiple are configured). |
| `fileName`         | string | **Yes**  | —       | Name of the Excel file (e.g., `myWorkbook.xlsx`).         |
| `sheetName`        | string | **Yes**  | —       | Name of the worksheet (e.g., `Sheet1`).                   |

- **cURL Example**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxcolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxColumn": 15
}
```

{{< /tab >}}

{{< /tabs >}}

- **Error Handling**

| HTTP Status | Meaning                                           | Sample Error Body                                                                |
| ----------- | ------------------------------------------------- | -------------------------------------------------------------------------------- |
| 200         | Success – returns the `MaxColumn` value.          | `{ "MaxColumn": 15 }`                                                            |
| 400         | Bad request – missing or invalid parameters.      | `{ "Code": "BadRequest", "Message": "Parameter`cellOrMethodName`is required." }` |
| 401         | Unauthorized – invalid or missing token.          | `{ "Code": "Unauthorized", "Message": "Access token is invalid or expired." }`   |
| 404         | Not found – workbook or worksheet does not exist. | `{ "Code": "NotFound", "Message": "Worksheet`Sheet1`not found." }`               |
| 500         | Server error – unexpected condition.              | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }`        |

- **Cloud SDK Family**

Using an SDK is the fastest way to develop. An SDK handles low‑level details, allowing you to focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxColumnWorksheet-get-max-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxColumnWorksheet-get-max-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example (currently not provided) -->

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3282f0b23cd22dbd0adee0f1fbd0bf2c" >}}

{{< /tab >}}

{{< /tabs >}}

### Frequently Asked Questions

<details><summary>What does the **Get MaxColumn** endpoint return?</summary>
It returns a JSON object that contains a single property **MaxColumn**. The value is the zero‑based index of the rightmost column that contains data in the specified worksheet.
</details>

<details><summary>How do I authenticate the request?</summary>
Include an `Authorization: Bearer <access_token>` header. The token is obtained via the Aspose Cloud OAuth 2.0 client‑credentials flow.
</details>

<details><summary>What is the difference between **maxcolumn** and **maxdatacolumn**?</summary>
`maxcolumn` returns the last column that contains any cell (including empty cells), whereas `maxdatacolumn` returns the last column that actually contains data.
</details>
