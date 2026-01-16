---
title: "Replace text in an Excel workbook"
second_title: "Document"
linktitle: "Replace in workbook"
type: docs
url: /workbook/replace-text/
aliases: [/replace-text-in-a-workbook/]
weight: 60
keywords: "Aspose Cells Cloud, Replace Text, Excel Workbook, XLSX, ODS, REST API, Spreadsheet, SDK"
description: "Use Aspose.Cells Cloud REST API to replace text in Excel (XLS, XLSX, XLSM, XLSB) and OpenDocument Spreadsheet (ODS) workbooks. The API is available via cURL and multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, etc.)."
---

This REST API replaces text in an Excel workbook.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```

### Request parameters

| Parameter Name | Type   | Location                     | Description                                           |
|----------------|--------|------------------------------|-------------------------------------------------------|
| name           | string | path                         | Name of the workbook file.                            |
| sheetName      | string | path                         | Name of the worksheet where the replacement occurs.  |
| oldValue       | string | query                        | Text that should be replaced.                         |
| newValue       | string | query                        | Text that will replace the old value.                 |
| folder         | string | query                        | Folder path containing the workbook.                 |
| storageName    | string | query                        | Name of the storage service where the workbook resides.|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorsheetTextReplace) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to call Aspose.Cells web services easily. The example below shows how to make a request with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/replaceText?oldValue=a&newValue=a12" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 26,
  "Workbook": {
    "link": {
      "Href": "/test.xlsx",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality. An SDK handles low‑level details, allowing you to focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}