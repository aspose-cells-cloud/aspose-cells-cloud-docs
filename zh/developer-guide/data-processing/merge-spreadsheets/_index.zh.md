---
title: "合并多个 Excel 文件为一个工作表 — Aspose.Cells Cloud API"
secondtitle: "文档"
articletitle: "将多个 Excel 文件合并为一个 — 批量合并电子表格为 30 多种格式"
linktitle: "合并电子表格"
type: docs
url: /zh/merge-spreadsheets/
keywords: "Aspose.Cells, 合并电子表格, Excel API, 云电子表格, 批量合并, PDF 转换, CSV 合并, ODS 合并, API 参考, SDK"
description: "使用 Aspose.Cells Cloud 将多个本地 Excel、CSV 或 ODS 文件合并为一个工作簿，并将结果转换为 30 多种格式（PDF、HTML 等）。包含端点说明、参数说明、认证指南及 SDK 示例。"
weight: 100
---

使用 Aspose.Cells Cloud API，将多个本地 Excel、CSV 或 ODS 文件合并为一个工作簿，并转换为 30 多种输出格式。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名             | 类型     | 位置         | 描述                                                                                   |
| ------------------ | -------- | ------------ | -------------------------------------------------------------------------------------- |
| Spreadsheet        | 文件     | FormData     | 待上传的本地电子表格文件，支持 XLSX、XLS、CSV、ODS 等格式。                             |
| outFormat          | 字符串   | 查询参数     | 目标输出格式（如 `XLSX`、`PDF`、`CSV`、`HTML`），支持 30 多种格式。                      |
| mergeInOneSheet    | 布尔值   | 查询参数     | `true` → 所有数据合并到单个工作表；`false` → 保留原始各工作表。                         |
| outPath            | 字符串   | 查询参数（可选） | 云存储路径，用于保存合并后的文件；若省略，则使用默认路径。                              |
| outStorageName     | 字符串   | 查询参数     | 使用的云存储名称（默认或自定义存储）。                                                  |
| fontsLocation      | 字符串   | 查询参数（可选） | 包含自定义字体的云存储路径，用于确保 PDF/图像正确渲染。                                 |
| region             | 字符串   | 查询参数（可选） | 用于数字、日期和货币格式化的区域设置（如 `en-US`、`zh-CN`）。                            |
| password           | 字符串   | 查询参数（可选） | 打开受密码保护的电子表格所需的密码。                                                    |

### **响应**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

生成的文件可直接从云存储下载，或保存到 `outPath` 指定的位置。

**成功响应详情**

| 状态码 | 内容类型                   | 描述                       |
| ------ | -------------------------- | -------------------------- |
| 200 OK | `application/octet-stream` | 合并后工作簿文件的二进制流。 |

**HTTP 状态码说明**

| 状态码 | 含义              | 描述                                         |
| ------ | ----------------- | -------------------------------------------- |
| 200    | OK（成功）        | 合并操作成功执行，响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（如文件类型不支持）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                    |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                    |

## 合并电子表格 API 的适用场景

### **教育与学术应用**

- **学生作业评分**：合并多个学生作业文件，便于统一评阅与批注。
- **科研数据汇总**：整合来自不同实验组的数据电子表格。
- **教学材料制作**：将多章节练习题合并为一个题库工作簿。

### **数据处理与分析**

- **小型数据集整合**：合并来自不同来源的 CSV 或 Excel 文件。
- **数据分析预处理**：在进行分析前合并相关数据文件。
- **模板数据填充**：将合并后的数据填入预设报表模板。

### **开发与技术支持**

- **测试数据准备**：合并多个测试用例文件用于自动化测试。
- **日志文件分析**：整合来自不同时段的系统日志 Excel 报表。
- **配置管理**：将多个配置电子表格合并为统一配置文件。

## 为何选择使用合并电子表格 API？

- **开发者友好**：提供多种编程语言的 SDK 库，相比自研方案大幅减少开发工作量。
- **降低人力成本**：无需专人负责手动合并文档，自动化处理显著节省时间。
- **按需付费**：仅对实际调用的 API 请求计费，无需前期投入。
- **零维护成本**：无需管理服务器、软件更新或兼容性问题。

## 如何使用 SDK 调用合并电子表格 API

### OpenAPI 规范

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI 规范</a> 提供了 API 的机器可读描述，便于直接进行 REST 调用。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells 云服务。以下示例展示如何通过 cURL 调用该云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

SDK 是开发速度最快的方案，它屏蔽了底层细节，仅需少量代码即可完成电子表格数据导入。完整 SDK 列表请参阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}