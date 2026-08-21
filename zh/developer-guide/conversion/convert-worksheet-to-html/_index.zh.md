---
title: "Aspose.Cells Cloud Web API – 将工作表转换为 HTML"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将工作表转换为 HTML"
linktitle: "将工作表转换为 HTML"
type: docs
url: /convert-worksheet-to-html/
description: "了解如何使用 Aspose.Cells Cloud API 将 Excel 工作表转换为 HTML —— 零上传、自定义字体、区域支持及错误处理。"
keywords: "Aspose.Cells, Excel 转 HTML, 工作表转换, 云 API"
weight: 100
---

**ConvertWorksheetToHtml** 端点从本地文件系统读取 Excel 工作簿，提取指定的工作表，并将内容以 HTML 文件形式返回。转换过程完全在 Aspose 的云服务器上执行，因此无需中间上传或存储操作。该 API 非常适合生成电子表格数据的网页就绪视图，支持可选的输出路径、自定义字体、区域设置以及密码保护的工作簿。

## 将工作表转换为 HTML 的 API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 位置     | 必填/可选 | 描述                                                                                                                                                                 |
| :--------------- | :----- | :------- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件   | 必填     | FormData  | 待处理的二进制 Excel 文件。必须是有效的 .xlsx、.xls、.xlsb 等格式。示例：`myWorkbook.xlsx`。Excel 文件直接从请求体读取，无需预先上传至云存储。                         |
| worksheet        | 字符串 | 必填     | 查询参数  | 要转换的工作表名称（区分大小写）。必须存在于提供的工作簿中。示例：`Sheet1`。                                                                                         |
| outPath          | 字符串 | 可选     | 查询参数  | 生成的 HTML 文件将保存到的云存储目标文件夹路径。若省略，则直接在响应中返回文件。示例：`/output/html/`。                                                                |
| outStorageName   | 字符串 | 可选     | 查询参数  | 用于 `outPath` 的云存储服务名称。仅当 `outPath` 指向非默认存储时才需提供。                                                                                           |
| fontsLocation    | 字符串 | 可选     | 查询参数  | 包含自定义 TrueType/OpenType 字体的绝对路径，转换时应使用这些字体。可确保非标准字符正确渲染。                                                                        |
| region           | 字符串 | 可选     | 查询参数  | 区域标识符，影响数字/日期格式（例如 `zh-CN`、`en-US`、`fr-FR`）。默认使用工作簿内部的区域设置。                                                                       |
| password         | 字符串 | 可选     | 查询参数  | 打开受保护工作簿所需的密码。无密码保护的文件可省略此项。                                                                                                             |

### 响应

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                           |

## 应该在哪里使用“将工作表转换为 HTML”的 API？

- 在 Web 门户中嵌入实时电子表格数据 —— 将财务报告工作表转换为 HTML，以便直接在浏览器中查看，无需安装 Excel 插件。
- 从 Excel 模板生成可打印的 HTML 发票 —— 从预定义工作表自动创建网页就绪的发票页面。
- 创建文档代码片段 —— 将设计规范工作表转换为 HTML 片段，可插入技术手册或维基百科中。
- 开发低代码 BI 仪表板 —— 提取工作表数据、转换为 HTML，并在自定义仪表板组件中显示。

## 为什么应使用“将工作表转换为 HTML”的 API？

- **零上传工作流**：直接在云端转换本地文件，无需先将大型工作簿传输到存储空间。
- **高性能渲染**：服务端转换利用 Aspose 优化引擎，快速且准确地生成 HTML 输出。
- **完全控制输出结果**：可选参数（自定义字体、区域、密码）使您能够根据区域设置和品牌需求定制 HTML。
- **无缝集成**：简单的 PUT 请求配合 multipart/form-data 格式，可轻松融入 CI/CD 流水线、微服务或无服务器函数中。

## 如何使用 SDK 调用“将工作表转换为 HTML” API

### Convert worksheet to HTML API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">Convert Worksheet to HTML API 规范</a> 提供了可公开访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 编码)",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方案，因为它抽象了底层细节，让您能够通过简洁的代码合并工作表。  
请参阅 <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud SDK GitHub 仓库</a>，获取完整的 Aspose.Cells Cloud SDK 列表。  
以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务进行交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}