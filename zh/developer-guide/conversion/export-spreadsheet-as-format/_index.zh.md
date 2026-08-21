---
title: "Aspose.Cells Cloud Web API — 导出远程 Excel 工作表为其他格式的免费在线工具"
second_title: "文档"
ArticleTitle: "如何将远程电子表格工作表导出为其他格式：分步指南"
linktype: "文档"
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells, 电子表格转换, API, 导出, PDF, CSV, JSON, XLSX"
description: "通过单个 REST 端点，将存储在 Aspose Cloud 中的 Excel 工作簿转换为 PDF、XLSX、CSV、JSON 或 HTML 格式。了解请求语法、参数，并查看 C#、Java、Python 等语言的 SDK 示例。"
weight: 100
---

将云存储中的电子表格（Excel）导出为其他文件格式。

## **将电子表格导出为指定格式的 API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型   | 路径 / 查询字符串 / HTTP 请求体 | 描述                                                                                          |
| :--------------- | :----- | :---------------------------- | :-------------------------------------------------------------------------------------------- |
| name             | String | Path                          | （必填）需检索的工作簿文件名。                                                                |
| format           | String | Query                         | （必填）期望的输出格式（如 “Xlsx”、“PDF”、“CSV”）。                                          |
| folder           | String | Query                         | （可选）工作簿所在的文件夹路径；默认为 null。                                                 |
| storageName      | String | Query                         | （可选）若使用自定义云存储，则指定存储名称；省略时使用默认存储。                             |
| outPath          | String | Query                         | （可选）导出后工作簿的保存路径；默认为 null。                                                 |
| outStorageName   | String | Query                         | （可选）输出文件的存储名称。                                                                  |
| fontsLocation    | String | Query                         | （可选）自定义字体所在路径。                                                                  |
| region           | String | Query                         | （可选）电子表格区域/语言设置（如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式、日期解析及本地化行为。 |
| password         | String | Query                         | （可选）打开电子表格文件所需的密码。                                                          |

### **响应**

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

响应包含一个对象，表示已转换的文件流。

**HTTP 状态码**

| 状态码 | 含义           | 描述                                       |
| ------ | -------------- | ------------------------------------------ |
| 200    | OK（成功）     | 过滤操作成功；响应包含操作详情。           |
| 400    | Bad Request    | 缺失或无效参数（如不支持的文件类型）。     |
| 401    | Unauthorized   | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large | 上传文件超出大小限制。                   |
| 500    | Internal Server Error | 服务器内部错误。                        |

## 应在何处使用“将电子表格导出为其他格式” API？

- **遗留系统迁移**：将数以千计的旧版 XLS 文件转换为 XLSX，适配现代系统。
- **归档标准化**：将多种电子表格格式（XLS、XLSM、ODS、CSV）统一转换为单一格式用于归档。
- **办公套件互操作性**：将 Excel 文件转换为 LibreOffice、Google Sheets 或 Apple Numbers 兼容格式。
- **数据源标准化**：将多种电子表格格式转换为 CSV 或 JSON，便于数据库导入。
- **网页发布**：将财务模型转换为 HTML，以便在网页上展示。

## 为何应使用“将电子表格导出为其他格式” API？

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，可快速开发，并配有详尽文档；相比自行构建图表渲染解决方案，可显著减少开发工作量。
- **降低人力成本**：无需专人负责文档整合任务。
- **按需付费**：无需前期投入，仅对实际调用的 API 请求付费。
- **免服务器维护**：无需维护服务器、更新软件或处理兼容性问题。
- **全面格式支持**：支持 20 多种电子表格格式之间的相互转换。
- **保留数据准确性与格式**：转换过程中保留原始布局、公式和样式。

## 如何结合 SDK 使用“将电子表格导出为指定格式” API？

### 导出电子表格为指定格式 API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">“导出电子表格为指定格式 API” 规范文档</a> 提供了公开可访问的编程接口，便于无缝执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

使用 SDK 是开发速度最快的途径，它屏蔽了底层细节，使您能以简洁代码将电子表格导出为目标格式文件。  
调用 API 前，请先获取 OAuth 2.0 访问令牌，并将其置于 `Authorization: Bearer <token>` 请求头中。

请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过各类 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}