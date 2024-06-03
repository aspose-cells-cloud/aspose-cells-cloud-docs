---
title: 文件版本
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/storage/file-versions/
keywords: Learn how to get file version with Aspose Cells Cloud REST API
description: 了解如何使用 Aspose Cells Cloud REST API 获取文件版本 SDK 支持多种开发语言。其中包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdwon, 文件版本
---
这个REST API表示获取`file versions`。
 
## 重置 API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件路径，例如“/file.ext”|
|存储名称|细绳|询问|存储名称|

 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用云 API。
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
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
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK 系列
 
使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。
 
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 
