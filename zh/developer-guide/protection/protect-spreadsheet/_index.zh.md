---
title: "Aspose.Cells Cloud Excel 密码保护 Web API —— 自动化设置打开和修改密码加密"
second_title: "Excel 保护开发者指南"
ArticleTitle: "Excel 密码保护工具 —— 设置打开和修改密码 —— 保护您的电子表格"
linktype: "protect-spreadsheet"
type: docs
url: /zh/protect-spreadsheet/
keywords: "Aspose.Cells, Excel 密码保护, API, 打开密码, 修改密码, 云存储, 电子表格安全"
description: "使用 Aspose.Cells Cloud 以编程方式保护 Excel 文件。通过单次 API 调用即可设置打开密码和修改密码。支持 .xlsx、.xls 格式及云存储。免费试用。"
weight: 100
---

通过我们的开发者 API 以规模化方式自动化 Excel 密码保护 —— 以编程方式同时应用打开密码和修改密码。适用于企业级工作流，兼容 .xlsx 及旧版格式。立即获取文档，开始免费集成。

## **电子表格保护 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名称       | 类型   | 路径/查询字符串/HTTP正文 | 描述                                                                                         |
| :------------- | :----- | :----------------------- | :------------------------------------------------------------------------------------------- |
| Spreadsheet    | 文件   | FormData                 | 要上传并使用密码加密保护的 Excel 电子表格文件。                                              |
| openPassword   | 字符串 | 查询字符串               | 打开（解密）受保护电子表格所需的密码。                                                       |
| modifyPassword | 字符串 | 查询字符串               | 启用电子表格内容编辑或修改所需的密码。                                                       |
| outPath        | 字符串 | 查询字符串               | （可选）指定保存受保护工作簿的输出文件夹路径。若未提供，文件将作为响应返回。                 |
| outStorageName | 字符串 | 查询字符串               | 用于存储输出受保护文件的云存储名称。                                                         |
| region         | 字符串 | 查询字符串               | 指定处理过程中应用于电子表格的区域/语言环境设置（例如日期格式、数字格式）。                  |

**身份验证**  
调用电子表格保护 API 所有请求均需有效的 OAuth 2.0 访问令牌。请将令牌包含在 `Authorization` 请求头中：

```http
Authorization: Bearer {access_token}
```

令牌须从 Aspose Cloud 的身份验证端点获取，并且必须包含 **Cells** 作用域。

## **响应**

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

| 状态码 | 含义               | 描述                                       |
| ------ | ------------------ | ------------------------------------------ |
| 200    | OK（请求成功）     | 应用过滤器成功；响应包含操作详情。         |
| 400    | Bad Request（请求错误） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（负载过大） | 上传文件超过大小限制。                 |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                 |

## 应在何处使用电子表格保护 API？

- **保护敏感财务数据** —— 使用打开密码和修改密码保护包含预算、发票或工资信息的 Excel 文件，防止未授权访问或修改。
- **安全共享机密报告** —— 在内部或外部分发业务、审计或合规性报告时，确保仅授权收件人可查看或修改内容。
- **在工作流中自动化文档安全** —— 将 API 集成到企业系统（如 ERP、CRM）中，在存储或邮件发送前自动为生成的电子表格设置密码保护。
- **强制实施只读访问权限** —— 允许用户打开报告进行查看，同时通过独立的修改密码限制其修改操作 —— 非常适用于模板或最终确定的数据集。
- **满足监管合规要求** —— 通过自动化保护，对静态及传输中的敏感电子表格数据进行加密，从而协助满足 GDPR、HIPAA 或 SOX 等合规要求。

## 为何应使用电子表格保护 API？

- **开发者友好** —— Aspose.Cells Cloud 提供多种编程语言的 SDK 库，可快速开发，并配有详尽文档。相比构建自定义解决方案，可显著减少开发工作量。
- **降低人员需求** —— 自动化文档整合与安全保护，减少对专职人员的依赖。
- **按需付费** —— 无需前期投入，仅为您实际使用的 API 调用次数付费。
- **零维护成本** —— 无需维护服务器、无需软件更新、无需兼容性顾虑。
- **保留原始 Excel 格式** —— 应用密码保护的同时保留所有原始 Excel 格式，确保受保护工作簿外观与源文件完全一致。

## 如何通过 SDK 使用电子表格保护 API

### OpenAPI 规范

[电子表格保护 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) 提供公开可访问的编程接口，便于从 Web 浏览器直接进行 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
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

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，使您仅需少量代码即可实现电子表格保护功能。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 与 Aspose.Cells Web 服务进行交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}