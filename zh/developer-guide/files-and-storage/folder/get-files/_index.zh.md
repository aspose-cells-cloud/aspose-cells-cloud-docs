---
title: 获取文件
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/folder/get-files/
keywords: Learn how to get files from folder with Aspose Cells Cloud REST API
description: 了解如何使用 Aspose 从文件夹中获取文件 Cells Cloud REST API SDK 支持各种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 100
---
这个 REST API 表示 `get files`。
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件夹路径，例如“/文件夹”|
|存储名称|细绳|询问|存储名称|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## 云 SDK 系列
 
使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。
 
以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 
 
 

