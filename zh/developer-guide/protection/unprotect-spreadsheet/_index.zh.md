---
title: "Aspose.Cells Cloud Excel 解除保护 Web API —— 编程方式移除打开与修改密码"
second_title: "文档"
ArticleTitle: "移除 Excel 密码保护 —— 立即解锁打开与修改密码"
linktype: "解除电子表格保护"
type: docs
url: /zh/unprotect-spreadsheet/
keywords: "解除保护, 电子表格, Aspose.Cells, API, Excel, 密码移除"
description: "通过 Aspose.Cells Cloud 解除电子表格保护 API 编程方式移除 Excel 文件的打开密码和修改密码。支持 .xlsx/.xls 格式、OAuth2 身份验证及批量处理。"
weight: 100
---

解除电子表格保护 API 可在单次调用中移除 Excel 文件的打开密码和修改密码保护。该 API 非常适用于数据管道、文档管理系统及迁移工作流等场景。

## **解除电子表格保护 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名称         | 类型     | 位置       | 描述                                                                 |
| ---------------- | -------- | ---------- | -------------------------------------------------------------------- |
| Spreadsheet      | 文件     | FormData   | 需要解除保护的 Excel 文件。                                          |
| password         | 字符串   | Query      | 用于打开文件的密码。                                                 |
| modifyPassword   | 字符串   | Query      | 修改文件所需的密码（若仅设置了打开密码，则此项可选）。               |
| outPath          | 字符串   | Query      | （可选）保存已解除保护工作簿的文件夹路径。                           |
| outStorageName   | 字符串   | Query      | （可选）输出文件将被写入的存储名称。                                 |
| region           | 字符串   | Query      | （可选）电子表格区域设置。                                           |

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

成功响应会以流形式返回已解除保护的文件。该文件可保存至 `outPath`/`outStorageName` 指定的位置，或直接从响应负载中获取。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                   |
| ------ | ---------------- | -------------------------------------- |
| 200    | OK（请求成功）   | 成功应用过滤器；响应包含操作详情。     |
| 400    | Bad Request      | 缺少或无效参数（例如不支持的文件类型）。|
| 401    | Unauthorized     | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large| 上传文件超出大小限制。                 |
| 500    | Internal Server Error | 服务器内部错误。                  |

## 何时应使用解除电子表格保护 API？

- **恢复受锁定工作簿的访问权限**——快速移除遗忘的打开密码或修改密码，无需人工干预。
- **自动化批量解锁**——在数据迁移或归档项目中批量处理大量文件。
- **集成至现有工作流**——结合存储或转换 API 构建端到端流程（例如：上传 → 解除保护 → 转换为 PDF）。
- **保障数据安全**——操作在服务器端完成，确保原始文件安全，而解除保护后的版本将存入您的云存储中。

## 如何使用 SDK 调用解除电子表格保护 API

### OpenAPI 规范

[解除电子表格保护 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) 提供了公开可访问的编程接口，便于从 Web 浏览器直接进行 REST 交互。

您可以使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

使用 SDK 可简化调用过程，自动处理身份验证、请求构建及响应解析。SDK 支持多种编程语言，并包含现成的电子表格解除保护方法。

以下代码示例展示了如何使用不同语言的 SDK 调用解除电子表格保护 API：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}