---
title: "匹配 Excel 工作表中所有非空单元格"
second_title: "文档"
linktitle: "匹配所有非空单元格"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, 匹配非空单元格, 自动筛选, Excel API"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表的自动筛选列表中匹配所有非空单元格。内容包括端点、参数、身份验证、响应模式、错误代码以及 SDK 示例。"
ArticleTitle: "使用 Aspose.Cells Cloud API 匹配 Excel 工作表中的所有非空单元格"
weight: 100
---

**概述**  
*匹配所有非空单元格* 操作会对工作表应用自动筛选，并仅返回指定列中包含数据的行，忽略空单元格。此功能可用于清理数据集、生成报告或为后续分析准备数据。

**前提条件**  
- 有效的 Aspose.Cells Cloud 身份验证 JWT 令牌。  
- 工作簿必须已上传至 Aspose Cloud 存储。  
- 您需要文件名、工作表名称以及要筛选的列的从零开始的索引（`fieldIndex`）。

此 REST API 可匹配 Excel 工作表中自动筛选列表里的所有非空单元格。

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型    | 位置   | 描述                                                  |
| ------------ | ------- | ------ | ----------------------------------------------------- |
| name         | string  | 路径   | Excel 文件的名称。                                    |
| sheetName    | string  | 路径   | 包含自动筛选的工作表名称。                            |
| fieldIndex   | integer | 查询   | 要应用筛选的列的从零开始的索引。                      |
| folder       | string  | 查询   | _(可选)_ 文件所在的文件夹路径。                        |
| storageName  | string  | 查询   | _(可选)_ 要使用的存储服务名称。                        |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义            | 描述                                             |
|--------|-----------------|--------------------------------------------------|
| 200    | OK（成功）      | 筛选成功应用；响应包含操作详情。                   |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。         |
| 401    | Unauthorized（未授权）  | 无效或缺失的 JWT 令牌。                             |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                          |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                            |

*示例错误响应（400）*  

```json
{
  "Code": 400,
  "Message": "无效参数：fieldIndex 必须是非负整数。"
}
```

## 如何结合 SDK 使用 PostWorksheetMatchNonBlanks API

### PostWorksheetMatchNonBlanks API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}