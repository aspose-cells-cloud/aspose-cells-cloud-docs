---
title: 获取列详情 – Aspose.Cells Cloud API 参考（v4.0）
description: 使用 Aspose.Cells Cloud REST API 获取工作表列（索引、宽度、样式、隐藏状态）的详细信息。
keywords: Aspose.Cells, 云 API, Excel 列, 获取列, REST API, JWT, 工作表
date: 2026-07-30
---

# 获取列详情  

从存储在 Aspose Cloud 中的 Excel 工作簿中获取指定工作表列（索引、宽度、样式、隐藏状态）的详细信息。

## 目录
1. [前置条件](#prerequisites)  
2. [身份验证](#authentication)  
3. [接口地址](#endpoint)  
4. [请求参数](#request-parameters)  
5. [cURL 示例](#curl-example)  
6. [响应示例](#response-example)  
7. [响应结构](#response-schema)  
8. [可能的错误](#possible-errors)  
9. [SDK 示例](#sdk-examples)  
10. [其他资源](#additional-resources)  

---

## 前置条件
- 已通过 Aspose Cloud 身份验证获取有效的 **JWT 访问令牌**。  
- 工作簿文件必须已存储在 Aspose Cloud 存储（或其他受支持的存储）中，并需知晓其所在的文件夹路径（如有）。  

---

## 身份验证
所有 Aspose.Cells Cloud API 均采用 **基于 JWT 令牌的身份验证**。请将令牌置于 `Authorization` 请求头中：

```http
Authorization: Bearer <access_token>
```

获取令牌的详细步骤，请参阅 [身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

---

## 接口地址
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – 工作簿文件名（例如 `test.xlsx`）。  
- **{sheetName}** – 工作表名称（例如 `Sheet1`）。  
- **{columnIndex}** – 要获取的列的**零基索引**。

---

### **安全与身份验证**

Aspose.Cells Cloud API 具备高安全性，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

## 请求参数

| 参数名          | 位置 | 类型    | 是否必需 | 说明 |
|-----------------|------|---------|----------|------|
| **name**        | path | string  | 是       | 工作簿文件名。 |
| **sheetName**   | path | string  | 是       | 包含目标列的工作表名称。 |
| **columnIndex** | path | integer | 是       | 要获取的列的**零基索引**。 |
| **folder**      | query| string  | 否       | 工作簿所在的存储文件夹路径。 |
| **storageName** | query| string  | 否       | 存储服务名称（例如 Aspose Cloud Storage）。 |

---

## cURL 示例
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## 响应示例
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## 响应结构
| 字段                | 类型    | 说明 |
|---------------------|---------|------|
| `Column.GroupLevel` | integer | 列的分组级别（用于大纲分组）。 |
| `Column.Index`      | integer | 列的**零基索引**。 |
| `Column.IsHidden`   | boolean | 若列被隐藏则为 `true`，否则为 `false`。 |
| `Column.Width`      | number  | 列宽（以字符数表示）。 |
| `Column.Style`      | object  | 包含指向该列样式资源的 `link`。 |
| `Column.link`       | object  | 指向该列资源的自链接。 |
| `Code`              | integer | 响应的 HTTP 状态码。 |
| `Status`            | string  | 状态的文字描述（例如 **OK**）。 |

---

## 可能的错误
| HTTP 状态码 | 错误码 | 错误消息                 | 出现原因 |
|-------------|--------|--------------------------|----------|
| 400         | 400    | Bad Request              | 缺失或格式错误的必需参数。 |
| 401         | 401    | Unauthorized             | 缺失或无效的 `Authorization` 请求头。 |
| 404         | 404    | Not Found                | 工作簿、工作表或列不存在。 |
| 500         | 500    | Internal Server Error    | 服务器端突发错误。 |

### 示例 – 404 Not Found（未找到）
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### 示例 – 401 Unauthorized（未授权）
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## SDK 示例
以下代码片段演示如何使用官方 Aspose.Cells Cloud SDK 调用 **Get Worksheet Columns（获取工作表列）** 接口。若 Gist 不可用，内联代码亦已提供。

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// 配置 API 客户端
var apiInstance = new CellsApi("client_id", "client_secret");

// 设置必需参数
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // 可选
string storageName = "MyStorage";    // 可选

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // 可选
        String storageName = "MyStorage";    // 可选

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # 可选
storage_name = "MyStorage"  # 可选

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // 可选
const storageName = "MyStorage"; // 可选

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **注意**：所有 SDK 均会在您提供 `client_id` 和 `client_secret` 后自动处理 `Authorization` 请求头。

---

## 其他资源
- **OpenAPI 规范**： <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **身份验证指南**： <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **GitHub 仓库（SDK 与示例）**： <https://github.com/aspose-cells-cloud>  

--- 

*本文档最后更新于 2026‑07‑30。*