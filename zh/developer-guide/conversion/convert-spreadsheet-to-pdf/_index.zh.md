---
title: "Aspose.Cells Cloud Web API – 将电子表格转换为 PDF"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将本地电子表格转换为 PDF"
linktitle: "将电子表格转换为 PDF"
type: docs
url: /zh/convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud、电子表格转 PDF、Excel 转换、云 API、PDF 生成、REST API、v4.0"
description: "分步指南，介绍如何使用 Aspose.Cells Cloud API 将本地电子表格转换为 PDF。包含请求语法、参数说明、响应详情、错误处理及实际应用场景。"
weight: 100
---

**ConvertSpreadsheetToPdf** 端点可读取从本地驱动器上传的电子表格文件，在 Aspose.Cells Cloud 服务器上处理该文件，并以二进制流形式返回生成的 PDF 文档。这种云原生转换方式无需将源文件上传至云端存储空间，从而降低资源消耗，并通过直接向客户端返回 PDF 简化工作流程。支持的文件格式取决于底层库；API 会验证文件是否存在、权限是否有效以及转换过程的完整性，若输入无效或处理失败，则抛出相应的 HTTP 错误。

## **将电子表格转换为 PDF 的 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **安全与认证**

Aspose.Cells Cloud API 安全可靠，需采用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### **请求参数：**

| 参数名称         | 类型   | 位置     | 必填/可选 | 描述                                                                                                                               |
| :--------------- | :----- | :------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件   | FormData | 必填      | 待转换的源电子表格文件（如 XLS、XLSX、CSV 等），必须是有效且可读的文件，最大尺寸为 100 MB。示例：`myWorkbook.xlsx`。                |
| outPath          | 字符串 | Query    | 可选      | 转换后的 PDF 在服务器上的目标文件夹路径（若需保存）。若省略，则文件将直接在响应中返回。示例：`/output/reports/`。                    |
| outStorageName   | 字符串 | Query    | 可选      | 目标存储服务名称（例如 `MyCloudStorage`）。仅当使用 `outPath` 且存储非默认存储时才需要。                                           |
| fontsLocation    | 字符串 | Query    | 可选      | 服务器上自定义字体文件夹的路径，确保 PDF 中文本正确渲染。示例：`/fonts/custom/`。                                                   |
| region           | 字符串 | Query    | 可选      | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`）。影响数字格式化、日期解析及本地化行为。                                    |
| password         | 字符串 | Query    | 可选      | 打开受保护电子表格所需的密码。若文件未加密，则无需提供。                                                                           |

### **响应**

成功响应（200 OK）  
Content-Type: application/pdf  
Content-Disposition: attachment; filename="converted.pdf"  
Content-Length: `<字节数>`

响应体：生成的 PDF 文件的二进制流

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 转换成功；响应中包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺失或参数无效（如不支持的文件类型）。         |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（载荷过大） | 上传文件超出尺寸限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                           |

## 应在何处使用“将电子表格转换为 PDF”API？

- **自动化报告流程**：将每日生成的 Excel 报告转换为 PDF，用于归档或邮件分发，无需人工干预。
- **文档管理系统（DMS）集成**：转换后直接将 PDF 存入 DMS，源电子表格仅保留在客户端本地。
- **Web 应用程序即时导出功能**：允许终端用户下载浏览器中编辑的电子表格的 PDF 版本，利用云转换保留原始布局。
- **合规性要求场景**：为财务电子表格生成不可变的 PDF 快照，用于审计追踪，确保源文件永不离开客户端环境。
- **跨格式转换工作流**：结合其他转换端点（如 [将电子表格转换为 CSV](/convert-spreadsheet-to-csv/) API），创建多格式归档方案。

## 为何应使用“将电子表格转换为 PDF”API？

- **零上传工作流**：无需将源文件上传至云端存储；转换直接从上传流处理，节省带宽和存储成本。
- **高保真渲染效果**：Aspose.Cells 在转换为 PDF 时保留复杂公式、图表和格式设置，效果与桌面版 Excel 一致。
- **可扩展云执行能力**：依托 Aspose 的云基础设施，无论客户端硬件性能如何，均可实现快速、可靠的转换。
- **简洁的 REST 接口**：仅需一次 `PUT` 请求配合可选查询参数；直接返回可下载的 PDF 流，便于在任意编程语言中集成。

## 如何使用 SDK 调用“将电子表格转换为 PDF”API

### Convert Spreadsheet To Pdf API 规范

[Convert Spreadsheet To Pdf API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) 提供了公开可访问的编程接口，允许直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[]（Base64 编码）",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可显著加快开发速度，因其封装了底层细节，使您仅需少量代码即可完成电子表格合并等操作。请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。以下代码示例展示了如何使用多种 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}