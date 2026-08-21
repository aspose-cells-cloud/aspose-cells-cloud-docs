---
title: "匹配 Excel 工作表中的所有空白单元格"
ArticleTitle: "匹配 Excel 工作表中的所有空白单元格 – Aspose.Cells Cloud API 指南"
second_title: "文档"
linktitle: "匹配所有空白单元格"
type: docs
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, 空白单元格, 自动筛选, REST API, Excel"
description: "了解如何使用 Aspose.Cells Cloud REST API 过滤并匹配 Excel 工作表中的所有空白单元格。内容包括端点、参数、认证步骤、cURL 示例以及 C#、Java、Python 等多种语言的 SDK 代码片段。"
weight: 100
---

此 REST API 用于匹配 Excel 工作表中筛选列表里的所有**空白单元格**。

**前提条件**：调用此端点前，请确保您已获取有效的 JWT 访问令牌，工作簿已上传至 Aspose Cloud 存储空间，并且已知其所在的存储文件夹（如适用）。若文件不在默认根目录下，请提供 `folder` 和 `storageName` 参数。

## PostWorksheetMatchBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### 请求参数

| 参数名称       | 类型    | 位置   | 描述                                               |
|----------------|---------|--------|----------------------------------------------------|
| name           | string  | path   | 工作簿文件的名称。                                 |
| sheetName      | string  | path   | 包含筛选条件的工作表名称。                         |
| fieldIndex     | integer | query  | 应用筛选的列的从零开始的索引。                     |
| folder         | string  | query  | 工作簿所在的存储空间中的文件夹路径。               |
| storageName    | string  | query  | Aspose Cloud 存储空间的名称。                      |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                             |
|--------|------------------|--------------------------------------------------|
| 200    | OK（成功）       | 筛选操作成功应用；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺失或无效参数（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（载荷过大） | 上传的文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                             |

## 如何结合 SDK 使用 PostWorksheetMatchBlanks API

### PostWorksheetMatchBlanks API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) 定义了一个公开可访问的编程接口，让您能直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
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

使用 SDK 是加速开发的最佳方式。SDK 将底层细节抽象化，使您能专注于项目任务。如需查看 Aspose.Cells Cloud SDK 的完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}