---
title: 更新
type: docs
url: /zh/comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: REST API, spreadsheets, excel, update commen
description: Cells.Cloud API for Excel操作：更新评论
weight: 30
---
此 REST API 表示更新工作表的单元格注释。
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|细胞名称|细绳|小路|细胞名称|
|评论||身体|评论对象|
|文件夹|细绳|询问|文档文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"\
-d "{ \"CellName\": \"a1\", \"Author\": \"test\", \"HtmlNote\": \"string\", \"Note\": \"this is a comment\", \"AutoSize\": true, \"IsVisible\": true, \"Width\": 10, \"Height\": 10}"

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

## 云 SDK 系列
 
使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。
 
以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "bf512f63ac7d0c31f9a0f1008cd3e031" >}}

{{< /tab >}}

{{< /tabs >}}




