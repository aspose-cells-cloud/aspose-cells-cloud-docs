﻿---
title: 清除 Excel 文件中的对象
second_title: Aspose.Cells Cloud Documen
linktitle: 克莱尔
type: docs
url: /zh/clear/
aliases: [/clearobjects/]
keywords: Clear internal objects of Excel files
description: Aspose.Cells Cloud REST API 支持清除 Excel 文件的内部对象。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 39
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, 清除
---
此 REST API 表示 Excel 文件中的 `clear` excel 对象。

## 重新设置 API

```bash

POST https://api.aspose.cloud/v3.0/cells/clearobjects

```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件|文件|表单数据|要上传的文件|
|对象类型|细绳|询问|重复行/空白列/空白行/公式/内容/样式/图表/注释/图片/形状/列表对象/超链接/ole对象/数据透视表/验证/背景|

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/LightCells/PostClearObjects)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxx1",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxx2",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearObjects.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearObjects.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearObjects.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearObjects.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearObjects.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearObjects.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearObjects.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearObjects.go" >}}

{{< /tab >}}

{{< /tabs >}}
