---
title: "创建电子表格 API – Aspose.Cells Cloud (v5.0) | 生成 Excel 文件"
second_title: "文档"
ArticleTitle: "如何创建新的 Excel 电子表格 —— 生成空白或基于模板的文件"
linktype: "create-spreadsheet"
type: docs
url: /zh/create-spreadsheet/
keywords: "Aspose.Cells, 电子表格 API, 创建 Excel, 云服务, XLSX, ODS, CSV, 模板, SDK, 自动化"
description: "了解如何使用 Aspose.Cells Cloud API (v5.0) 创建空白或基于模板的 Excel 工作簿。内容包括端点、参数、错误代码、身份验证步骤以及 SDK 示例。"
weight: 100
---

使用 Aspose.Cells Cloud API 以编程方式创建新的 Excel 电子表格。可生成空白工作簿，或从自定义模板实例化文件。该 RESTful API 支持自动化 Excel 文件创建，非常适合用于报表生成、文档自动化及数据处理工作流。

## **创建电子表格 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称           | 类型   | 位置   | 描述                                                                                                                                           |
| ------------------ | ------ | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | 字符串 | 查询   | **必填**。新电子表格的文件格式（例如 `XLSX`、`XLS`、`ODS`、`CSV`）。                                                                           |
| **template**       | 字符串 | 查询   | **可选**。存储于您云端存储中的模板文件名（例如 `invoice_template.xlsx`）。若省略，则创建空白工作簿。                                             |
| **outPath**        | 字符串 | 查询   | **可选**。生成文件在云端存储中的目标文件夹路径。若为 `null` 或省略，则保存至默认位置。                                                         |
| **outStorageName** | 字符串 | 查询   | **必填**。已配置的云端存储标识符（例如 `MyDrive`）。                                                                                           |
| **region**         | 字符串 | 查询   | **可选**。区域设置（例如 `fr-FR`），用于确定日期、数字和货币格式的默认值。                                                                     |
| **password**       | 字符串 | 查询   | **可选**。加密模板文件的密码。若模板未受保护，请留空。                                                                                         |

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

| 状态码 | 含义                | 描述                                     |
| ------ | ------------------- | ---------------------------------------- |
| 200    | 成功 (OK)           | 操作成功；响应包含操作详情。             |
| 400    | 错误请求 (Bad Request) | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | 未授权 (Unauthorized) | 无效或缺失 JWT 令牌。                    |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超过大小限制。                 |
| 500    | 内部服务器错误 (Internal Server Error) | 服务器发生意外错误。                   |

## 在何处应使用创建电子表格 API？

- **自动化报表系统的初始化**——在每日/每周自动化周期开始时，创建新的空白工作簿，或根据标准模板生成报表文件。
- **用户自助服务门户**——允许客户选择模板（报价单、项目进度表等），并即时下载自定义的 Excel 文件。
- **批量数据导出与分发**——为每份导出数据集生成格式统一的独立工作簿，简化下游分发与处理流程。

后续操作（如添加工作表或填充单元格），请参阅 **添加工作表 API**、**更新单元格 API** 和 **导出工作簿 API**。

## 为何应使用创建电子表格 API？

- **开发者友好**——提供多种编程语言的 SDK 库及详尽文档，相比自研方案，更易于集成。
- **提升效率**——实现文档整合自动化，减少人工操作。
- **按需付费定价**——仅按 API 调用次数收费，无需预付许可费用。
- **托管式服务**——API 完全托管，无需维护本地服务器或更新软件。

## 如何通过 SDK 使用创建电子表格 API？

### 创建电子表格 API 规范

[创建电子表格 API 规范](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) 定义了一个公开可访问的编程接口，可直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
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

使用 SDK 是开发速度最快的方式，它能屏蔽底层细节，让您用简洁代码构建电子表格。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}