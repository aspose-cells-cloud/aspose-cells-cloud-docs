---
title: 从 Excel 文件获取元数据
second_title: Aspose.Cells Cloud Documen
linktitle: 无需使用存储即可获取
type: docs
url: /zh/metadata/get/
keywords: Get properties from Excel files
description: Aspose.Cells Cloud REST API 支持从 excel 文件获取属性。SDK 支持多种开发语言。包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 23
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、从 Excel 文件获取元数据
---
这个 REST API 表示从多个 Excel 文件中获取 `metadata`。

```bash

POST https://api.aspose.cloud/v3.0/cells/metadata/get

```

- **查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|类型|细绳|全部/内置/自定义|


- **请求主体参数**

|参数名称|类型|描述|
|:- |:- |:- |
|excel 文件|数据文件|数据文件保存到多部分内容的第一部分中。|

- **回复**

```bash
{
    [
        { 
            "Name":"test1",
            "Value":"test1",
            ...
        },
        { 
            "Name":"test2",
            "Value":"test3",
            ...
        }
    ]
}
```
- **Cloud SDK 系列**

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Metadata-Get.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-MetaData-Get.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Metadata-Get.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}
{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMetadata-Get.py" >}}
{{< /tab >}}
{{< /tabs >}}
