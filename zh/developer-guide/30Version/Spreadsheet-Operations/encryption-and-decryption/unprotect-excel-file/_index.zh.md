---
title: "取消保护 Excel 工作簿 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "取消保护 Excel 文件"
type: docs
url: /excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, Excel 取消保护 API, 移除工作簿保护, REST API, 云电子表格"
description: "了解如何使用 Aspose.Cells Cloud REST API 取消 Excel 工作簿的保护。包含请求语法、参数说明、cURL 示例以及多种编程语言的 SDK 代码示例。"
weight: 60
ArticleTitle: "取消保护 Excel 工作簿 – Aspose.Cells Cloud API"
---

使用此 REST API 取消 Excel 工作簿的保护。

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 路径参数

| 参数名   | 类型   | 描述                                 | 必填 |
| -------- | ------ | ------------------------------------ | ---- |
| **name** | string | 工作簿文件名（包含文件扩展名）。     | 是   |

### 查询参数

| 参数名       | 类型   | 描述                             |
| ------------ | ------ | -------------------------------- |
| folder       | string | 包含原始工作簿的文件夹路径。     |
| storageName  | string | 工作簿所在的存储服务名称。       |

### 请求体参数

| 参数名       | 类型                      | 描述                             |
| ------------ | ------------------------- | -------------------------------- |
| protection   | WorkbookProtectionRequest | 指定需移除的保护设置的对象。     |

#### WorkbookProtectionRequest

| 参数名         | 类型   | 描述                                                                 |
| -------------- | ------ | -------------------------------------------------------------------- |
| ProtectionType | string | 需移除的保护类型（`ALL`、`CONTENTS`、`NONE`、`OBJECTS`、`SCENARIOS`、`STRUCTURE`、`WINDOWS`）。 |
| Password       | string | 移除保护所需的密码（可选）。                                         |

#### cURL 示例

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### 响应（成功）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTPS 状态错误响应

| HTTP 状态 | 错误码                | 描述                                         |
| --------- | --------------------- | -------------------------------------------- |
| 400       | BadRequest            | 缺少或无效的参数。                           |
| 401       | Unauthorized          | 无效或缺失的访问令牌。                       |
| 404       | NotFound              | 在指定文件夹或存储中未找到指定的工作簿。     |
| 500       | InternalServerError   | 服务器发生意外错误。                         |

## 如何结合 SDK 使用 DeleteUnProtectWorkbook API

### DeleteUnProtectWorkbook API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可简化集成过程并减少样板代码。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}