---
title: "清除 Excel 工作表中的单元格格式"
type: docs
url: /zh/clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, 清除单元格格式, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "使用 Aspose.Cells Cloud REST API 清除 Excel 工作表中的单元格格式。包含请求详情、cURL 示例以及多种语言的 SDK 代码片段。"
ArticleTitle: "清除 Excel 工作表中的单元格格式 - Aspose.Cells Cloud API"
---

**注意：** 所有 Aspose.Cells Cloud API 调用必须通过 **HTTPS** 进行。HTTP 接口已被弃用，可能被浏览器拦截。

- **方法：** POST  
- **端点：** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

此 REST API 可清除 Excel 文件中的单元格格式，属于 Aspose.Cells Cloud 套件中用于清除 Excel 工作表单元格格式的功能模块。

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**响应架构**

| 字段   | 类型    | 描述                                           |
|--------|---------|------------------------------------------------|
| Code   | integer | API 返回的 HTTP 状态码（例如：200）。             |
| Status | string  | 操作结果（成功时为 `OK`）。                      |

**HTTP 状态码**

| 状态码 | 含义           | 描述                                           |
|--------|----------------|------------------------------------------------|
| 200    | OK             | 筛选器已成功应用；响应中包含操作详情。             |
| 400    | Bad Request    | 缺少或无效的参数（例如：不支持的文件类型）。         |
| 401    | Unauthorized   | JWT 令牌无效或缺失。                              |
| 413    | Payload Too Large | 上传文件超出大小限制。                          |
| 500    | Internal Server Error | 服务器内部意外错误。                          |

## 如何结合 SDK 使用 PostClearFormats API

### PostClearFormats API 规范

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI 规范</a> 定义了公开可访问的编程接口，使您能直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
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

使用 SDK 是最快捷的开发方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅**

- [清除单元格内容和样式](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [设置单元格样式](https://docs.aspose.cloud/cells/set-cell-style)