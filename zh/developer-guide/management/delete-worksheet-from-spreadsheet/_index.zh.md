---
title: "Aspose.Cells Cloud Excel 删除工作表 Web API - 以编程方式从工作簿中移除工作表"
second_title: "文档"
ArticleTitle: "如何删除 Excel 中的工作表 - 从工作簿中移除工作表"
linktitle: "从电子表格中删除工作表"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, 删除工作表 API, Excel 工作表移除, 云电子表格, REST API"
description: "了解如何使用 Aspose.Cells Cloud API 从 Excel 文件中删除工作表。包含端点、参数、示例 cURL 和 SDK 示例。"
weight: 100
---

使用 Aspose.Cells Cloud API 以编程方式从 Excel 工作簿中删除工作表。安全地移除单个或多个工作表，清理工作簿结构，并实现电子表格优化自动化。适用于企业级 Excel 管理和文档处理工作流的 RESTful API。

## 从电子表格中删除工作表 API

### Web API

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数：

| 参数名称         | 类型     | 位置     | 描述                                                                                                                                                            |
| :--------------- | :------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件     | FormData | **必需项。** 源 Excel 工作簿文件（如 .xlsx、.xls 等），将从中删除工作表。                                                                                      |
| sheetName        | 字符串   | Query    | **必需项。** 要删除的工作表的确切名称（例如 `Sheet1`、`TemporaryData`）。                                                                                       |
| outPath          | 字符串   | Query    | **可选项。** 云存储中保存修改后工作簿的目标文件夹路径。若省略或为 `null`，则工作簿将保存在源文件所在位置或默认路径。                                            |
| outStorageName   | 字符串   | Query    | **可选项。** 输出文件将写入的云存储服务标识符（例如 `ProjectStorage`）。若未提供，则使用默认存储。                                                              |
| region           | 字符串   | Query    | **可选项。** 区域设置（例如 `zh-CN`），可能在保存操作期间影响特定区域的公式或数据。                                                                             |
| password         | 字符串   | Query    | **可选项。** 打开和修改受密码保护的电子表格所需的密码。若文件未加密，则无需提供。                                                                               |

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

| 状态码 | 含义             | 描述                               |
| ------ | ---------------- | ---------------------------------- |
| 200    | OK（成功）       | 成功应用过滤器；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。               |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。         |
| 500    | Internal Server Error（内部服务器错误） | 意外服务器错误。             |

## 应在何处使用“从电子表格中删除工作表” API？

- **自动化报告后处理** – 生成最终财务报告后，自动删除用于临时计算的中间工作表，使最终文件保持整洁和专业。
- **模板文件的动态清理** – 用户从模板生成自定义文档（例如报价单）时，删除未被选中的可选页面。
- **工作流归档优化** – 项目或审计完成后，删除草稿或协作用工作表，仅保留最终版本用于归档和合规。

## 为何应使用“从电子表格中删除工作表” API？

- **开发者友好** – Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并提供详尽的文档。
- **降低人工成本** – 无需专人手动整合文档。
- **按需付费** – 无需前期投资；仅对实际使用的 API 调用收费。
- **零维护成本** – 无需维护服务器、无需软件更新、无兼容性问题。

## 如何使用 SDK 调用“从电子表格中删除工作表” API

### 删除工作表 API 规范

<a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">“从电子表格中删除工作表” API 规范</a> 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
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

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您能以极少的代码删除工作表。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}