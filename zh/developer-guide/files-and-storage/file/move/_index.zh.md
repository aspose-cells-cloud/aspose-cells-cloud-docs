---
title: 移動檔案
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/file/move/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: 了解如何使用 Aspose Cells Cloud REST API SDK 下载文件，支持多种开发语言。其中包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdwon, 移动文件
---
此 REST API 表示 `move file`
 
## 重置 API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|源路径|细绳|小路|源文件路径，例如“/src.ext”|
|目标路径|细绳|询问|目标文件路径，例如“/dest.ext”|
|源存储名称|细绳|询问|源存储名称|
|目标存储名称|细绳|询问|目标存储名称|
|版本ID|细绳|询问|要移动的文件版本 ID|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/File/MoveFile)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用云 API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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
 
 
