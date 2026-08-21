---
title: "导出工作表 – Aspose.Cells Cloud API v4（PDF、PNG、SVG、CSV）"
second_title: "文档"
ArticleTitle: "如何将远程电子表格工作表导出为其他格式：分步指南"
linktitle: "导出工作表"
type: docs
url: /zh/export-worksheet-as-format/
keywords: "Aspose Cells, 导出工作表, 云 API, PDF, PNG, CSV, Excel 转换"
description: "通过单次 GET 请求，将存储在 Aspose.Cells Cloud 中的工作表转换为 PDF、PNG、SVG、CSV 或其他格式。包含 C#、Java、Python 等语言的代码示例。"
weight: 100
---

使用 Aspose.Cells Cloud Web API 将云存储中的电子表格/Excel 工作表导出为其他格式的文件。

## **导出工作表为指定格式的 API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名            | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                   |
| :---------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| **name**          | 字符串 | 路径                       | （必填）要检索的工作簿文件名称。                                                                                                       |
| **worksheet**     | 字符串 | 路径                       | （必填）需转换的特定工作表名称。                                                                                                       |
| **format**        | 字符串 | 查询字符串                 | （必填）期望的输出格式（例如 `png`、`pdf`、`svg`）。                                                                                  |
| **folder**        | 字符串 | 查询字符串                 | （可选）工作簿所在的文件夹路径。默认为 `null`。                                                                                       |
| **storageName**   | 字符串 | 查询字符串                 | （可选）自定义云存储名称。若省略，则使用默认存储。                                                                                    |
| **outPath**       | 字符串 | 查询字符串                 | （可选）输出文件夹路径。默认为 `null`。                                                                                               |
| **outStorageName**| 字符串 | 查询字符串                 | （可选）输出文件的存储名称。                                                                                                           |
| **fontsLocation** | 字符串 | 查询字符串                 | （可选）如需使用自定义字体，请指定其路径。                                                                                             |
| **region**        | 字符串 | 查询字符串                 | （可选）电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域性相关行为。                                     |
| **password**      | 字符串 | 查询字符串                 | （可选）访问电子表格文件所需的密码。                                                                                                   |

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

**HTTP 状态码**

| 状态码 | 含义                 | 描述                                                   |
| ------ | -------------------- | ------------------------------------------------------ |
| 200    | OK（成功）           | 过滤器应用成功；响应包含操作详情。                     |
| 400    | Bad Request（错误请求）| 缺少或无效参数（例如不支持的文件类型）。               |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                                   |
| 413    | Payload Too Large（请求实体过大）| 上传的文件超出大小限制。                           |
| 500    | Internal Server Error（服务器内部错误）| 服务器发生意外错误。                             |

## **应在何处使用导出工作表为其他格式的 API？**

- **遗留系统迁移** – 将数千个遗留的 XLS 文件转换为 XLSX，以适配现代系统。
- **归档标准化** – 将各种电子表格格式（XLS、XLSM、ODS、CSV）统一转换为单一格式用于长期归档。
- **办公套件互操作性** – 将 Excel 文件转换为与 LibreOffice、Google Sheets 或 Apple Numbers 兼容的格式。
- **数据源标准化** – 将各种电子表格格式转换为 CSV 或 JSON，以便导入数据库。
- **网页发布** – 将财务模型转换为 HTML，用于网页展示。

## **为何使用导出工作表为其他格式的 API？**

- **多语言 SDK 支持** – 提供多种编程语言的客户端库，使开发者能直接从其偏好的开发环境中调用 API。
- **无需中转上传即可直接转换** – 支持直接将云存储中的工作表转换为目标格式，无需下载再重新上传文件。
- **仅提取数据内容** – 返回所选格式的工作表内容，不保留原有视觉样式（如字体、颜色等）。

## **如何结合 SDK 使用导出电子表格工作表为指定格式的 API？**

### 导出工作表为指定格式 API 规范

[导出工作表为指定格式 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) 提供了一个公开可访问的编程接口，允许开发者直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
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

使用 SDK 是开发效率最高的方式，它屏蔽了底层细节，使您能够用简洁的代码完成将电子表格工作表导出为指定格式文件的操作。  
请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}