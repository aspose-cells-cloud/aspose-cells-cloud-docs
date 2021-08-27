---
title: "Apply Rich Text Formatting to a Cell"
type: docs
url: /apply-rich-text-formatting-to-a-cell/
weight: 40
---

This REST API indicates apply `rich text formatting` to a cell in an Excel file.

```bash

POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string |  The worksheet name. |
| cellName | string |  Cell name. |

- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|


- **Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|List[FontSetting] |object |  Represents a range of characters within the cell text. |


- **Response**


```bash
{
    "Code": 200,
    "Status": "OK"
}

```


- **Api Reference**   

 [PostCellCharacters](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters)

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNet-CSharp-Cells-ApplyRichTextFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Cells-PostCellTextFormatting-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "" "53fb9eb3d3d0d6e836078d4677a51ab5" "Examples-Ruby-Cells-post_cell_text_formatting-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Cells-ApplyRichTextFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Cells-ApplyRichTextFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "9decd80776653e876bf47e2cfb298eee" >}}

{{< /tab >}}

{{< /tabs >}}
