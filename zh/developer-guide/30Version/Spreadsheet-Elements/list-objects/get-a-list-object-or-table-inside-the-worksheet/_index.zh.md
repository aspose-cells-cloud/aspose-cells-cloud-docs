---
title: 获取 Excel 工作表中的列表对象
second_title: Documen
linktitle: 葛
type: docs
url: /zh/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API 支持将列表对象（表格）导入 Excel 工作表。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 9
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、在 Excel 工作表中获取列表对象
---
此 REST API 通过索引向 `get` 指示列表对象信息，或在 Excel 工作表中将 `list object` 转换为不同格式的文件。

## 重新设置 API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|列表对象索引|整数|小路|列出对象索引。|
|格式|细绳|询问|导出格式。|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
 "ListObject": {
  "AutoFilter": {
   "FilterColumns": [],
   "Range": "B2:F11",
   "Sorter": {
    "CaseSensitive": false,
    "HasHeaders": false,
    "KeyList": [],
    "SortLeftToRight": false
   }
  },
  "DisplayName": "Table3",
  "StartColumn": 1,
  "StartRow": 1,
  "EndColumn": 5,
  "EndRow": 10,
  "ListColumns": [{
   "Name": "Column1",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 1,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$B$2:$B$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column2",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 2,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$C$2:$C$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column3",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 3,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$D$2:$D$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column4",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 4,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$E$2:$E$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column5",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 5,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$F$2:$F$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }],
  "ShowHeaderRow": true,
  "ShowTableStyleColumnStripes": false,
  "ShowTableStyleFirstColumn": false,
  "ShowTableStyleLastColumn": false,
  "ShowTableStyleRowStripes": true,
  "ShowTotals": false,
  "TableStyleName": "None",
  "TableStyleType": "None",
  "link": {
   "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
   "Rel": "self"
  }
 },
 "Code": 200,
 "Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

此 REST API 将 excel `listobject` 对象转换为不同格式的文件。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
