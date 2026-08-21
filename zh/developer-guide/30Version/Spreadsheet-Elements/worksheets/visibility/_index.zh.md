---
title: "如何操作 Excel 工作表的可见性"
second_title: "Document"
linktitle: "可见性"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, 隐藏工作表 API, 取消隐藏工作表 API, Excel 工作表可见性, REST API Excel, Aspose.Cells v3.0"
description: "了解如何通过 Aspose.Cells Cloud REST API 以编程方式隐藏或取消隐藏 Excel 工作表。包含请求 URL、cURL 与 .NET SDK 示例、错误处理及版本特定说明。"
weight: 20
---

## 操作 Excel 工作表的可见性

*工作表可见性*（worksheet visibility）定义了工作表是否向最终用户显示。借助 Aspose.Cells Cloud，您可以通过一条简单的 REST 请求来隐藏或取消隐藏工作表。相关 API 端点如下：

* **隐藏工作表** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **取消隐藏工作表** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **支持的 API 版本：** **v3.0**（截至 2026 年 3 月）

### 前提条件
1. 一个已激活的 **Aspose.Cells Cloud** 账户。  
2. 有效的 **client ID**（客户端 ID）和 **client secret**（客户端密钥）（或 OAuth 2.0 访问令牌）。  
3. 工作簿（`{fileName}`）必须已上传至 Aspose 云存储。  

---

## 隐藏工作表

### 请求
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### 响应
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### 示例 cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### 示例 .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Worksheet hidden: {response.Worksheet.Visible}");
```

### 常见错误
| HTTP 状态码 | 描述                                 | 解决方案                                         |
|------------|--------------------------------------|--------------------------------------------------|
| 400        | JSON 请求体无效或缺少 `Visible` 字段 | 确保请求体为有效 JSON，并包含 `"Visible"` 键。 |
| 401        | 未授权 – 令牌缺失或已过期             | 刷新 OAuth 令牌，并将其包含在请求头中。         |
| 404        | 工作表或文件未找到                   | 核实 `{fileName}` 和 `{sheetName}` 是否正确。   |
| 409        | 工作表已隐藏                         | 在发送请求前检查当前可见性状态。                |

---

## 取消隐藏工作表

### 请求
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### 响应
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### 示例 cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### 示例 .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Worksheet visible: {response.Worksheet.Visible}");
```

### 常见错误
| HTTP 状态码 | 描述                                 | 解决方案                                     |
|------------|--------------------------------------|----------------------------------------------|
| 400        | JSON 请求体无效或缺少 `Visible` 字段 | 提供包含 `"Visible": true` 的正确 JSON 请求体。 |
| 401        | 未授权 – 令牌缺失或已过期             | 重新生成访问令牌并重试。                    |
| 404        | 工作表或文件未找到                   | 确认文件和工作表名称存在于云存储中。         |
| 409        | 工作表已可见                         | 无需操作；工作表当前已是取消隐藏状态。       |

---

## 相关操作
> *冻结窗格* | *拆分窗格* | *缩放* — 请参阅对应页面以获取更多工作表布局控制功能。

---

## 常见问题（FAQ）

<dl>
  <dt>如何使用 Aspose.Cells Cloud API 隐藏工作表？</dt>
  <dd>向 `/cells/{fileName}/worksheets/{sheetName}/visibility` 发送 `PUT` 请求，请求体为 JSON：`{ "Visible": false }`，并附带有效的 OAuth 2.0 bearer token。若成功，API 将返回状态码 `200 OK`，并携带更新后的工作表对象。</dd>

  <dt>取消隐藏工作表后，我会收到何种响应？</dt>
  <dd>API 返回 `200 OK`，响应体中包含工作表对象，其中 `"Visible": true`。响应还包含工作表的 `Name`（名称）、`Index`（索引）和 `Visible`（可见性）属性。</dd>

  <dt>能否在单次调用中隐藏多个工作表？</dt>
  <dd>不可以。可见性端点仅针对单个工作表（由 `{sheetName}` 指定）。若需隐藏多个工作表，请在客户端代码中循环遍历各工作表名称并逐一调用接口。</dd>
</dl>

---

*本文由 Aspose 文档团队撰写——我们拥有 15 年以上自动化 Excel 工作流的丰富经验。*