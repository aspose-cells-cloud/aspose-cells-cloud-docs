---
title: "为单元格应用富文本格式"
type: docs
url: /zh/apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, 富文本, 单元格格式, REST API, Aspose.Cells Cloud"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 单元格应用富文本格式。包含请求语法、参数详情、cURL 示例及 SDK 代码片段。"
ArticleTitle: "使用 Aspose.Cells Cloud API 为单元格应用富文本格式"
---

此 REST API 可对 Excel 文件中的单元格应用**富文本格式**。

**前置条件：** 调用本操作前，您必须拥有有效的 JWT 令牌，且目标 Excel 文件已存在于指定的存储文件夹中。

**背景说明：** 富文本格式允许在单个单元格内应用多种字体样式，从而在 Excel 工作表中实现更丰富的数据呈现效果。

## PostCellCharacters API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型   | 位置     | 描述                                                         |
|----------------|--------|----------|--------------------------------------------------------------|
| name           | string | path     | Excel 文件名称（例如 `Book1.xlsx`）。                         |
| sheetName      | string | path     | 包含目标单元格的工作表名称。                                  |
| cellName       | string | path     | 要格式化的单元格地址（例如 `A1`）。                           |
| options        | object | body     | 定义单元格富文本格式设置的 JSON 对象。                        |
| folder         | string | query    | 存储中 Excel 文件所在的文件夹路径。                           |
| storageName    | string | query    | 存储服务名称（若使用自定义存储）。                            |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。           |
| 400    | Bad Request（请求错误） | 缺少或参数无效（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。                      |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                        |

## 如何结合 SDK 使用 PostCellCharacters API

### PostCellCharacters API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*C# SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Java SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*PHP SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Ruby SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Node.js SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Python SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Perl SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Go SDK 示例*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}