---
title: 更新
type: docs
url: /zh/hyperlinks/update/
aliases: [/update-hyperlinks-in-excel-worksheet/]
keywords: Update a hyperlink in an Excel worksheet
description: Aspose.Cells Cloud REST API 支持更新 Excel 工作表中的超链接。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 30
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, 更新
---
此 REST API 通过 Excel 工作表上的索引指示为 `update worksheet hyperlink`。

## 重新设置 API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
 
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|超链接索引|整数|小路|超链接的索引。|
|超级链接||身体|超链接对象|
|文件夹|细绳|询问|文件夹。|
|存储名称|细绳|询问|存储名称。|

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/Hypelinks/PostWorksheetHyperlink)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v  "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Hyperlink\": { \"Address\": \"https://www.msnbc.com/\", \"Area\": { \"EndColumn\": 6, \"EndRow\": 1, \"StartColumn\": 6, \"StartRow\": 1 }, \"ScreenTip\": null, \"TextToDisplay\": \"https://www.msnbc.com/\", \"link\": { \"Href\": \"/test.xlsx/worksheets/Sheet1/hyperlinks/4\", \"Rel\": \"self\", \"Title\": null, \"Type\": null } }, \"Code\": 200, \"Status\": \"OK\"}"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
