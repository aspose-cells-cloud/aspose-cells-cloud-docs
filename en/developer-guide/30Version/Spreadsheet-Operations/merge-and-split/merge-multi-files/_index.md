---
title: "Merge multi Excel files into an Excel file."
second_title: "Document"
linktitle: "Merge Multi Excel files"
type: docs
url: /merge-multi-files-into-excel/
aliases: [ /merge/multi-files/]
keywords: "Excel merge, Aspose.Cells Cloud, REST API, spreadsheet merge, cloud SDK, multiple Excel files"
description: "Learn how to use Aspose.Cells Cloud REST API to merge multiple Excel files into a single workbook. Includes cURL examples and SDK code snippets for various programming languages."
weight: 32
---

This REST API merges multiple Excel files into a single Excel workbook.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/merge
```

The request parameters are:

| Parameter Name | Type   | Location                     | Description                                                                 |
|----------------|--------|------------------------------|-----------------------------------------------------------------------------|
| file           | file   | formData (body)              | Excel file to upload.                                                       |
| format         | string | query                        | Desired output format (e.g., `xlsx`).                                      |
| mergeToOneSheet| boolean| query                        | Set to `true` to merge all worksheets into one sheet; default is `false`. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'file1=@file1.xlsx' \
-F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
    "Files": [
        {
            "Filename": "file1.xlsx",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "file2.xlsx",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}