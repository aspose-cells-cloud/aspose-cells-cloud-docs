---
title: 从 Excel 工作表中获取自动形状
second_title: Aspose.Cells Cloud Documen
linktitle: 自动形状
type: docs
url: /zh/shapes/get-autoshape/
aliases: [/get-autoshape-from-a-worksheet/]
keywords: Get autoshape to different format from an Excel worksheet
description: Aspose.Cells Cloud REST API 支持从 Excel 工作表获取不同格式的自动形状。SDK 支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、从 Excel 工作表获取自动形状
---
这个 REST API 表示 `get autoshape info`。
 
## 重置 API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoshapes/{autoshapeNumber}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|自动形状编号|整数|小路|自動圖形數量。|
|格式|细绳|询问|导出的格式。|
|文件夹|细绳|询问|文檔夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Autoshapes/GetWorksheetAutoshape)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用云 API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/autoshapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "AutoShape": {

    "Name": "AutoShape 2",

    "MsoDrawingType": "CellsDrawing",

    "AutoShapeType": "FlowChartDocument",

    "Placement": "FreeFloating",

    "UpperLeftRow": 7,

    "Top": 6,

    "UpperLeftColumn": 5,

    "Left": 0,

    "LowerRightRow": 10,

    "Bottom": 0,

    "LowerRightColumn": 11,

    "Right": 0,

    "Width": 102,

    "Height": 45,

    "X": 85,

    "Y": 129,

    "RotationAngle": 0.0,

    "HtmlText": "<Font Style=\"FONT-FAMILY: Tahoma;FONT-SIZE: 10pt;COLOR: #000000;TEXT-ALIGN: center;\">Body</Font>",

    "Text": "Body",

    "AlternativeText": "",

    "TextHorizontalAlignment": "Center",

    "TextHorizontalOverflow": "Overflow",

    "TextOrientationType": "NoRotation",

    "TextVerticalAlignment": "Center",

    "TextVerticalOverflow": "Overflow",

    "IsGroup": false,

    "IsHidden": false,

    "IsLockAspectRatio": false,

    "IsLocked": false,

    "IsPrintable": false,

    "IsTextWrapped": false,

    "IsWordArt": false,

    "ZOrderPosition": 1,

    "link": {

      "Href": "http://api.aspose.cloud/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1",

      "Rel": "self"

    }

  },

  "Code": "200",

  "Status": "OK"

}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK 系列
 
使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。
 
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-GetAutoshape-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-GetAutoshape-get-auto-shape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-GetWorksheetAutoshape-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-get_autoshape_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetAutoshapeFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-GetAutoshape-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-GetAutoshape-get-auto-shape.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-GetAutoshape-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "de52ec3211922aa795d7dd11ef0bd755" >}}

{{< /tab >}}

{{< /tabs >}}
