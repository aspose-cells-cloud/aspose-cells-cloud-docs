---
title: "使用 Aspose.Cells Cloud API 从 Excel 工作表中检索单行数据"
description: "学习如何使用 Aspose.Cells Cloud REST API 从 Aspose Cloud 存储中检索 Excel 工作表中的特定行。内容包括请求语法、参数、响应模式、示例 cURL 命令以及 SDK 代码（C#、Java、Python）。"
keywords: "Aspose.Cells Cloud, 获取行, Excel API, 电子表格 REST 接口, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# 从 Excel 工作表中检索单行数据

**端点**：`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

从 Aspose Cloud 存储中的工作表中检索一行数据。该操作需要一个包含 **Read（读取）** 权限范围的有效 OAuth 2.0 访问令牌。

---

## 目录
1. [前置条件](#前置条件)  
2. [HTTP 请求](#http-请求)  
3. [参数](#参数)  
   - [路径参数](#路径参数)  
   - [查询参数](#查询参数)  
4. [cURL 示例](#curl-示例)  
5. [响应](#响应)  
   - [成功响应模式](#成功响应模式)  
   - [状态码](#状态码)  
6. [SDK 代码示例](#sdk-代码示例)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [相关操作](#相关操作)  
8. [注意事项与限制](#注意事项与限制)  

---

## 前置条件
- 已激活订阅的 **Aspose Cloud 账户**。  
- 包含 **Read（读取）** 权限范围的 **OAuth 2.0 访问令牌**。  
- 目标工作簿必须已存在于 Aspose Cloud 存储中。  

---

## HTTP 请求
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*基础 URL*：`https://api.aspose.cloud/v3.0`

---

## 参数

### 路径参数
| 名称         | 类型     | 是否必需 | 描述                                     |
|--------------|----------|----------|------------------------------------------|
| `name`       | 字符串   | ✅       | 工作簿文件的名称（例如：`MyWorkbook.xlsx`）。 |
| `sheetName`  | 字符串   | ✅       | 工作表的名称（例如：`Sheet1`）。           |
| `rowIndex`   | 整数     | ✅       | 要检索的行的**零基索引**。                |

### 查询参数（可选）
| 名称           | 类型     | 是否必需 | 描述                                               |
|----------------|----------|----------|----------------------------------------------------|
| `folder`       | 字符串   | ❌       | 云存储中存放工作簿的文件夹路径。                   |
| `storageName`  | 字符串   | ❌       | 存储服务的名称（如果您使用的是自定义存储）。       |

---

## cURL 示例
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## 响应

### 成功响应模式（`200 OK`）
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* 样式对象 */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...其他单元格... */
    ]
  }
}
```

### 状态码
| 状态码 | 含义                         |
|--------|------------------------------|
| **200** | 成功检索行数据。             |
| **401** | 未授权——缺少或无效的访问令牌。 |
| **404** | 工作簿、工作表或行不存在。     |
| **500** | 服务器内部错误。             |

### 错误响应示例（`401 Unauthorized`）
```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

---

## SDK 代码示例

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // 可选
);

Console.WriteLine($"Row {response.Row.Index} retrieved with {response.Row.Cells.Count} cells.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – 可选
);

System.out.println("Row index: " + response.getRow().getIndex());
System.out.println("Cells count: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Row {response.row.index} retrieved with {len(response.row.cells)} cells.")
except ApiException as e:
    print("Exception when calling CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## 相关操作
| 操作名称         | 描述                                                                 |
|------------------|----------------------------------------------------------------------|
| **添加行**       | `POST /cells/{name}/worksheets/{sheetName}/rows` – 向工作表中插入新行。 |
| **删除行**       | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – 删除现有行。 |
| **获取多行数据** | `GET /cells/{name}/worksheets/{sheetName}/rows` – 检索多行数据集合。   |
| **行相关接口概览** | `/cells/rows/` – 行相关接口的通用文档。                              |

---

## 注意事项与限制
- **速率限制**：每个账户每分钟最多 100 次请求。  
- **支持的格式**：XLS、XLSX、CSV、ODS。  
- 行索引为**零基索引**，第一行为 `0`。  
- 调用此端点前，请确保工作簿已上传至指定的 `folder` 中。  

---