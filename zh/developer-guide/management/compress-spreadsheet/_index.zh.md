---
title: "Aspose.Cells Cloud Excel 压缩 Web API —— 以编程方式减小电子表格文件大小"
second_title: "文档"
ArticleTitle: "如何压缩 Excel 文件 —— 减小电子表格尺寸并优化性能"
linktitle: "压缩电子表格"
type: docs
url: /compress-spreadsheet/
keywords: "Excel 压缩, Aspose.Cells Cloud, 电子表格尺寸缩减, API, 工作簿优化"
description: "了解如何使用 Aspose.Cells Cloud API 压缩 Excel 工作簿。获取分步示例、参数说明、身份验证方法及最佳实践。"
weight: 100
---

使用 Aspose.Cells Cloud API 以编程方式压缩 Excel 电子表格并减小文件大小。通过移除未使用的数据、压缩嵌入对象以及清理格式，可优化工作簿性能。该 RESTful API 支持自动化 Excel 文件压缩与优化工作流。

## **压缩电子表格 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名             | 类型     | 位置（路径/查询/字符串/HTTP 请求体） | 描述                                                                                             |
| ------------------ | -------- | ----------------------------------- | ------------------------------------------------------------------------------------------------ |
| Spreadsheet        | 文件     | FormData                            | **必填项。** 待压缩的源 Excel 工作簿文件（`.xlsx`、`.xls` 等）。                                |
| level              | 整数     | Query                               | **可选项。** 压缩强度（0 = 最快/最低压缩，9 = 最慢/最高压缩）。若未指定，默认采用平衡值（5）。     |
| outPath            | 字符串   | Query                               | **可选项。** 压缩后文件在您云存储中的目标文件夹路径。若未指定，则保存至源工作簿所在文件夹。       |
| outStorageName     | 字符串   | Query                               | **必填项。** 已配置的云存储服务的标识符（例如：`CorporateDrive`）。                              |
| region             | 字符串   | Query                               | **可选项。** 区域设置（例如：`de-DE`），可能影响区域特定数据处理方式。                           |
| password           | 字符串   | Query                               | **可选项。** 解密受保护电子表格所需的密码。若文件未加密，请留空。                                |

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

| 状态码 | 含义             | 描述                                         |
| ------ | ---------------- | -------------------------------------------- |
| 200    | OK（成功）       | 压缩操作成功；响应包含操作详情。             |
| 400    | Bad Request      | 缺少或无效参数（如不支持的文件类型）。       |
| 401    | Unauthorized     | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large| 上传文件超出大小限制。                       |
| 500    | Internal Server Error | 服务器内部错误。                         |

## 压缩电子表格 API 的适用场景

- **自动化报告分发** —— 在发送月度财务报表前进行压缩，确保邮件成功投递并提升收件人体验。
- **用户上传文件优化** —— 在后台压缩用户上传的 Excel 文件，节省云存储空间并降低存储成本。
- **数据管道处理与迁移** —— 压缩 ETL 流程中生成的中间 Excel 文件，加快网络传输速度并减轻临时存储压力。

## 为何应使用压缩电子表格 API？

- **开发者友好** —— Aspose.Cells Cloud 提供多种语言的 SDK 库，配合详尽文档，可快速完成开发。
- **降低人工成本** —— 无需专人手动合并文档。
- **按需付费定价** —— 无需前期投入，仅对实际调用的 API 请求计费。
- **免服务器维护** —— 无需管理服务器、软件更新或兼容性问题。

## 如何结合 SDK 使用压缩电子表格 API

### 压缩电子表格 API 规范

[压缩电子表格 API 规范](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) 提供了公开可访问的 REST 接口，支持直接从网页浏览器发起 API 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
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

使用 SDK 是最快捷的开发方式，它抽象了底层细节，仅需寥寥数行代码即可完成电子表格压缩。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}