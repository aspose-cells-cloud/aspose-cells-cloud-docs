---
title: "使用 Aspose.Cells Cloud API 保护 Excel 工作簿"
second_title: "文档"
linktitle: "保护 Excel 文件"
type: docs
url: /zh/protect-excel-file/
aliases: [  /zh/protect-excel-workbooks/ , /zh/workbook/protect/ ]
keywords: "Aspose.Cells, Excel 保护, API, REST, SDK"
description: "了解如何通过 Aspose.Cells Cloud REST API 保护 Excel 工作簿。包含身份验证步骤、查询与请求体参数、cURL 请求示例，以及 C#、Java、PHP、Ruby、Node.js、Python、Perl 和 Go 的 SDK 代码示例。"
weight: 30
ArticleTitle: "使用 Aspose.Cells Cloud API 保护 Excel 工作簿"
---

此 REST API **保护** Excel 工作簿，使您能够使用 Aspose.Cells Cloud 安全地以密码和保护选项保护 Excel 工作簿。

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 查询参数

| 参数名         | 类型   | 描述                                         |
| -------------- | ------ | -------------------------------------------- |
| folder         | string | 包含源工作簿的文件夹。（可选）               |
| storageName    | string | 存储位置的名称。（可选；默认值为 "Default"） |

### 请求体参数

| 参数名       | 类型                      | 描述                                |
| ------------ | ------------------------- | ----------------------------------- |
| protection   | WorkbookProtectionRequest | 定义工作簿保护设置的对象。          |

#### WorkbookProtectionRequest

| 参数名           | 类型   | 描述                                                                                                                                              |
| ---------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType   | string | 要应用的保护类型。允许的值（不区分大小写）：**ALL**、**CONTENTS**、**NONE**、**OBJECTS**、**SCENARIOS**、**STRUCTURE**、**WINDOWS**。             |
| Password         | string | 用于设置保护的可选密码。                                                                                                                          |

### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                 |
|--------|------------------|--------------------------------------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。     |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。             |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                 |

## 如何使用 SDK 调用 PostProtectDocument API

### 前提条件

在调用 API 之前，请确保已完成以下步骤：

- **获取 JWT 访问令牌**：按照“安全与身份验证”一节中描述的身份验证流程获取。  
- **上传工作簿**：将工作簿上传至您的 Aspose Cloud 存储空间，或确认其已存在于目标文件夹中。  
- **明确存储名称**（若未指定，默认为 `"Default"`）及您希望保护的文件名。

### PostProtectDocument API 规范

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

### 示例：使用 cURL 保护工作簿

1. 按照**前提条件 / 身份验证**中的说明获取访问令牌。  
2. 执行请求：

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   响应将包含一个状态对象，确认保护已成功应用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发 Aspose.Cells Cloud 应用程序的最快方式。SDK 封装了底层细节，使您能够专注于业务逻辑。有关 Aspose.Cells Cloud SDK 的完整列表，请参阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 示例完整响应

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```