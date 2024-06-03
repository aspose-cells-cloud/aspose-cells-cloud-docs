---
title: 使用粘贴选项复制工作表中的区域
second_title: Aspose.Cells Cloud Documen
linktitle: 警察
type: docs
url: /zh/ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: Copy a range in an Excel worksheet with paste options
description: Aspose.Cells Cloud REST API 支持使用粘贴选项复制 Excel 工作表中的范围。SDK 支持多种开发语言。其中包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 20
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、使用粘贴选项在工作表中复制范围
---
此 REST API 表示在 Excel 工作表上复制工作表中的范围。
 
## 重置 API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|工作簿名称|
|工作表名称|细绳|小路|工作表名称|
|范围操作||身体|复制数据、复制样式、复制到、复制值|
|文件夹|细绳|询问|工作簿文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRanges)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用云 API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Operate\": \"string\", \"Source\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"Target\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"string\", \"SkipBlanks\": true, \"Transpose\": true }}"

```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK 系列
 
使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。
 
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 
 
{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp

string Client_Id = "Use your Client_Id";

string Client_Secret = "Use your Client_Secret";

//Copy Range in a Worksheet with Paste Options - URL

string url = "http://api.aspose.cloud/v3.0/cells/sampleRangeCopyTo.xlsx/worksheets/Sheet1/ranges";

//JSON - Part of Request Body

string strJson = "{ \"Operate\": \"copyto\", \"Source\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 1, \"FirstRow\": 0, \"RowCount\": 7, \"RowHeight\": 15, }, \"Target\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 10, \"FirstRow\": 20, \"RowCount\": 7, \"RowHeight\": 15, } , \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"All\", \"SkipBlanks\": true, \"Transpose\": false } }";

//Sign the URL

string surl = Sign(url, Client_Id, Client_Secret);

//Process Command - Post Signed URL with JSON body

using (Stream stream = ProcessCommand(surl, "Post", strJson, "json"))

{

	//Your code

}

```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "4b9529b9d4238c301f3ee4855843874b" >}}

{{< /tab >}}

{{< /tabs >}}




