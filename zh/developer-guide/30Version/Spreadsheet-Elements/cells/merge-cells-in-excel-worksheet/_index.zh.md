---
title: "如何合并 Excel 工作表中的单元格——Aspose.Cells Cloud API（v3.0）"
type: docs
url: /merge-cells-in-excel-worksheet/zh/
weight: 110
keywords: "合并单元格, Aspose.Cells, 云 API, Excel"
description: "使用 Aspose.Cells Cloud REST API 合并 Excel 工作表中单元格的指南，并提供 cURL 和 SDK 示例。"
ArticleTitle: "如何合并 Excel 工作表中的单元格——Aspose.Cells Cloud API（v3.0）"
---

Aspose.Cells Cloud REST API 可将一个矩形区域的单元格合并为一个跨越指定行和列的单一单元格。

**前置条件**  
- 具备有效的 JWT 令牌用于身份验证。  
- 工作簿必须已存在于指定的存储文件夹中。  
- 存储配置（文件夹名称和存储名称）需已在您的 Aspose.Cloud 账户中设置完毕。

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名          | 类型    | 位置   | 描述                                     |
|-----------------|---------|--------|------------------------------------------|
| name            | string  | path   | 工作簿名称。                             |
| sheetName       | string  | path   | 工作表名称。                             |
| startRow        | integer | query  | 起始行索引（从 0 开始，0 表示第一行）。   |
| startColumn     | integer | query  | 起始列索引（从 0 开始，0 表示第一列）。   |
| totalRows       | integer | query  | 需要合并的行数。                         |
| totalColumns    | integer | query  | 需要合并的列数。                         |
| folder          | string  | query  | 包含工作簿的文件夹名称。                 |
| storageName     | string  | query  | 存储名称。                               |

*此操作无需请求体。*

## **响应**

返回 CellsCloudResponse。

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码说明**

| 状态码 | 含义             | 描述                                               |
|--------|------------------|----------------------------------------------------|
| 200    | OK（成功）       | 合并操作成功；响应包含操作详情。                   |
| 400    | Bad Request（错误请求） | 参数缺失或无效（如文件类型不支持）。             |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何结合 SDK 使用 PostWorksheetMerge API

### PostWorksheetMerge API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器进行 REST 交互。

您可使用 **cURL 命令行工具**轻松访问 Aspose.Cells 网络服务。以下示例展示了如何通过 cURL 调用 Cloud API：

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

使用 SDK 是加速开发进程的最佳方式。SDK 将处理底层细节，使您能专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}