---
title: "重命名 Excel 工作表 – Aspose.Cells Cloud API"
second_title: "文档"
articleTitle: "如何重命名 Excel 工作表 – 修改工作表名称"
linktitle: "重命名电子表格中的工作表"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "重命名工作表, Aspose.Cells Cloud, Excel API, 电子表格, SDK, REST API"
description: "通过 Aspose.Cells Cloud API 轻松重命名 Excel 工作表。了解所需参数、查看 cURL 示例，并获取 C#、Java、Python 等语言的 SDK 代码。"
weight: 100
---

使用 Aspose.Cells Cloud API 以编程方式重命名 Excel 工作簿中的工作表。更改工作表名称、动态更新标签页名称，并通过 RESTful API 调用自动化电子表格组织流程。适用于文档标准化和工作流自动化。

## 电子表格 API 中重命名工作表名称

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**cURL 示例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称           | 类型   | 位置   | 描述                                                                                                                                                                                                 |
|--------------------|--------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Spreadsheet**    | 文件   | FormData | **必填**。包含待重命名工作表的 Excel 工作簿文件（.xlsx、.xls 等）。                                                                                                                                |
| **sourceName**     | 字符串 | Query    | **必填**。您希望重命名的工作表当前名称。                                                                                                                                                           |
| **targetName**     | 字符串 | Query    | **必填**。分配给工作表的新名称。必须遵循 Excel 命名规则（不能包含 `:`、`\`、`?`、`*`、`[`、`]`），且在工作簿中必须唯一。                                                                           |
| **outPath**        | 字符串 | Query    | **可选**。重命名后的工作簿将保存到的云存储目标文件夹路径。若为 `null` 或省略，则服务会将文件保存到与源工作簿相同的文件夹（或默认路径）。                                                            |
| **outStorageName** | 字符串 | Query    | **可选**。您已配置的云存储服务的名称标识符（例如 `ArchiveStorage`）。若省略，则使用默认存储。                                                                                                       |
| **region**         | 字符串 | Query    | **可选**。区域设置（例如 `zh-CN`），可能影响字符编码或区域命名规范。                                                                                                                               |
| **password**       | 字符串 | Query    | **可选**。打开和修改密码保护的工作簿所需的解密密码。若文件未加密则省略。                                                                                                                           |

**说明**：工作表名称最多为 31 个字符，且不能包含字符 `:`、`\`、`?`、`*`、`[` 或 `]`。

### 响应

成功请求将返回一个包含状态信息及重命名文件链接的 JSON 对象。

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

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | 成功 (OK)        | 操作成功；响应包含操作详情。               |
| 400    | 请求错误 (Bad Request) | 参数缺失或无效（例如不支持的文件类型）。   |
| 401    | 未授权 (Unauthorized) | JWT 令牌无效或缺失。                      |
| 413    | 负载过大 (Payload Too Large) | 上传文件超出大小限制。                    |
| 500    | 内部服务器错误 (Internal Server Error) | 服务器发生意外错误。                      |

## 应在何处使用电子表格 API 中的重命名工作表功能？

- **报告生成与品牌标准化**——在自动生成客户报告时，将通用工作表名称（例如 `Sheet1`）重命名为客户专属名称（例如 `AcmeCorp_Q1_Summary`），确保交付成果专业规范。
- **数据处理流程标准化**——在 ETL 工作流中，将导出时名称不规范的工作表重命名为标准化名称（例如 `Raw_Data` 或 `Cleaned_Data`），以满足下游分析需求。
- **多语言内容交付**——根据用户语言偏好，在文件交付前将工作表名称本地化（例如 `数据` 或 `Data`），提供个性化体验。

## 为何应使用电子表格 API 中的重命名工作表功能？

- **开发者友好**——提供多种语言的 SDK 及详尽文档，简化集成过程，相较于自建方案更高效。
- **降低人工成本**——自动化重命名工作表，减少人工操作。
- **按需付费模式**——仅对 API 调用收费，无需预付许可费用。
- **无需服务器维护**——作为云服务，无需自行部署和维护服务器，也不用更新软件。
- **支持自动化**——助力工作流中实现文档标准化自动化。

## 如何通过 SDK 使用电子表格 API 中的重命名工作表功能

### OpenAPI 规范

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 提供了公开可访问的编程接口，允许直接通过网页浏览器发起 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

使用 SDK 是加速开发的最快方式。SDK 抽象了底层 HTTP 细节，使您能以最少代码完成工作表重命名。请参阅 GitHub 仓库以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}