---
---
title: "分组列 – Aspise.Cells 云 API 文档"
description: "使用 Aspose.Cells Cloud REST API（v3.0）对 Excel 工作表中的列进行分组。包含请求语法、参数、cURL 和 SDK 示例，以及响应详情。"
keywords: "Aspose.Cells, 分组列, Excel API, REST, 云 SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Excel 工作表中的列分组

**API 版本：** v3.0  
**操作：** `PostGroupWorksheetColumns` – 对工作表中的列进行分组。

---

## 概述

此 REST API 允许您对工作表中的一组列进行分组。分组后的列可以显示或隐藏，从而实现类似 Microsoft Excel 中可折叠部分的功能。

---

## 前置条件

- 从 Aspose Cloud 身份验证服务获取有效的 **JWT 访问令牌**。  
- 工作簿必须存储在 Aspose.Cells Cloud 可访问的位置（默认存储或自定义存储名称）。  
- 所需 SDK 版本（如使用 SDK）：支持 API 版本 **v3.0** 的最新版本。

---

## 身份验证

所有请求均需要 **Bearer token** 身份验证。

```http
Authorization: Bearer <access_token>
```

有关获取令牌的详细信息，请参阅 [JWT 身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

---

## HTTP 请求

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| 参数 | 位置 | 必填 | 描述 |
|-----------|----------|----------|-------------|
| `name` | 路径 | 是 | 工作簿文件名（例如 `test.xlsx`）。 |
| `sheetName` | 路径 | 是 | 包含待分组列的工作表名称。 |
| `firstIndex` | 查询参数 | 是 | 要分组的第一列的从零开始的索引。 |
| `lastIndex` | 查询参数 | 是 | 要分组的最后一列的从零开始的索引。 |
| `hide` | 查询参数 | 否 | 若为 `true`，则隐藏分组列；否则保持可见。 |
| `folder` | 查询参数 | 否 | 包含工作簿的文件夹路径。 |
| `storageName` | 查询参数 | 否 | 文件所在存储服务的名称。 |

---

## 请求示例（cURL）

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **注意：** 请求使用 **HTTPS** 以确保通信加密。

---

## 响应

### 成功（200）

| 字段 | 类型 | 描述 |
|--------|---------|-------------|
| `Code` | 整数 | HTTP 状态码（`200`）。 |
| `Status` | 字符串 | 操作的状态文本（`OK`）。 |

**示例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 错误（例如 400 Bad Request）

| 字段 | 类型 | 描述 |
|--------------|---------|-------------|
| `Code` | 整数 | HTTP 状态码（`400`、`401`、`404`、`500` 等）。 |
| `Status` | 字符串 | 状态文本（`Error`）。 |
| `ErrorMessage` | 字符串 | 可读的问题描述。 |
| `ErrorCode` | 字符串 | 错误的程序化标识符。 |

**示例 – 错误请求**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "列索引无效。",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK 示例

以下代码片段展示了如何使用支持的 SDK 调用 **分组工作表列** 操作。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## 备注

- **分组行为：** API 将创建可在 Excel 中展开或折叠的列组；设置 `hide=true` 可立即折叠该组。  
- **从零开始的索引：** `firstIndex` 和 `lastIndex` 均以 **0** 为起始值；工作表中的第一列索引为 0。  
- **存储注意事项：** 若工作簿位于非默认存储中，请同时提供 `folder` 和 `storageName` 查询参数。

---

## 参见

- [身份验证 – 基于 JWT 令牌](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [分组工作表列的 OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDK（GitHub）](https://github.com/aspose-cells-cloud)  
- [Excel 工作表中的行分组](/rows/group/)  

---

> *示意图：* ![显示 Excel 工作表中已分组列的屏幕截图](./images/group-columns.png){: .img-fluid alt="显示 Excel 工作表中已分组列的屏幕截图" }

*上述占位图应替换为实际截图，以展示列分组的视觉效果。*