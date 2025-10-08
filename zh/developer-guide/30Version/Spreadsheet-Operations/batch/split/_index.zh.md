---
title: 批量拆分
second_title: Documen
type: docs
url: /zh/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API 支持批量文件拆分。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, 批量拆分
---
此 REST API 表示符合条件的文件为 `batch split`。

## 重新设置 API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|批量拆分请求||身体||

**BatchSplitRequest 属性**

名称 | 类型 | 描述 | 备注
------------ | ------------- | ------------- | -------------
源文件夹 | 字符串 | | [可选]源存储 | 字符串 | | [可选]匹配条件 | 匹配条件请求 | | [可选]格式 | 字符串 | | [可选]从索引 | 整数 | | [可选]到索引 | 整数 | | [可选]输出文件夹 | 字符串 | | [可选]保存选项 | 保存选项 | | [可选]**MatchConditionRequest 属性**

名称 | 类型 | 描述 | 备注
------------ | ------------- | ------------- | -------------
RegexPattern | 字符串 | | [可选]FullMatchConditions | 字符串[]| | [可选][OpenAPI 规范](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于拆分的任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

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
{{< /tab >}}

{{< /tabs >}}
