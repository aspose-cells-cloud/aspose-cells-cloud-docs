---
title: "删除条件格式 – Aspose.Cells Cloud API 参考"
type: docs
url: /zh/conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, 条件格式, 删除, API, Excel, 云"
description: "使用 Aspose.Cells Cloud REST API 从工作表中删除条件格式规则。包含参数说明、身份验证、请求/响应示例及 SDK 代码片段。"
weight: 60
---

# 删除条件格式

## 背景说明
条件格式可让您根据特定条件（例如：高亮显示大于阈值的数值）为单元格应用视觉样式。在自动化场景中，您可能需要删除已存在的规则。本接口用于从存储在 Aspose Cloud 存储中的 Excel 工作簿的工作表中删除条件格式规则。

## 前提条件
- 已启用 **Cells** 产品的 **Aspose Cloud** 账户。  
- 通过 OAuth 2.0 客户端凭据流程生成的 **JWT 访问令牌**。  
- 工作簿（`{name}`）必须已存在于指定的 **文件夹** 和 **存储**（如有）中。  
- 下方 URL 使用的 API 版本为 **v3.0**（默认版本）。

## 身份验证
所有 Aspose.Cells Cloud 接口均要求使用 **基于 JWT 令牌的身份验证**。

```http
Authorization: Bearer <access_token>
```

### 获取访问令牌（cURL）

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**响应示例**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

请在每个请求的 `Authorization` 请求头中使用返回的 `access_token`。

## HTTP 请求

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### 路径参数

| 名称         | 类型    | 必填 | 描述 |
|--------------|---------|------|------|
| `name`       | 字符串  | 是   | 工作簿文件名（例如：`Book1.xlsx`）。 |
| `sheetName`  | 字符串  | 是   | 包含条件格式的工作表名称。 |
| `index`      | 整数    | 是   | 待删除条件格式规则的从零开始的索引。 |

### 查询参数

| 名称            | 类型   | 必填 | 描述 |
|-----------------|--------|------|------|
| `folder`        | 字符串 | 否   | 工作簿所在的云文件夹。 |
| `storageName`   | 字符串 | 否   | Aspose Cloud 存储服务的名称。 |

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### 成功响应

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP 状态码说明**

| 状态码 | 含义             | 描述 |
|--------|------------------|------|
| 200    | OK（成功）       | 条件格式删除成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

## 错误响应

| HTTP 状态码 | 原因 | 响应体示例 |
|-------------|------|------------|
| **400**     | Bad Request（错误请求） – 参数缺失或无效。 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**     | Unauthorized（未授权） – JWT 令牌缺失或无效。 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | Not Found（未找到） – 工作簿或工作表不存在。 | `{ "Code":"404", "Message":"File not found." }` |
| **500**     | Internal Server Error（内部服务器错误） – 服务器发生意外故障。 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## SDK 示例
以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK 调用 **删除条件格式** 接口。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// 配置 API 客户端
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// 删除条件格式
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

*（Ruby、Go、Perl 和 Swift 的 SDK 代码片段请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。）*

## 参考链接
- **身份验证指南** – [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI 规范** – 本接口的详细架构定义（将在新标签页中打开）  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>`  
- **条件格式概览** – 了解如何创建、更新和列出格式规则。  
- **Aspose.Cells Cloud SDK 列表** – 支持的语言完整列表，请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。  

---  

*本页面遵循标准 Aspose.Cells Cloud API 文档模板，包含“前提条件”部分，并符合无障碍性和 SEO 最佳实践。*