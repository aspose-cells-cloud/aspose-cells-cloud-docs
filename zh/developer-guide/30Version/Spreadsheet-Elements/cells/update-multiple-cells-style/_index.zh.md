---
title: "更新多个单元格样式 – Aspose.Cells Cloud API 参考（v3.0）"
type: docs
url: /update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "更新多个单元格样式", "Excel 单元格样式 API", "云 SDK", "REST API", "cURL 示例", "JSON 请求", "JWT 身份验证"]
description: "了解如何使用 Aspose.Cells Cloud REST API v3.0 更新 Excel 工作簿中某范围单元格的样式。内容包括端点、HTTP 方法、参数、cURL 与 SDK 示例、身份验证、错误处理以及版本信息。"
ArticleTitle: "更新多个单元格样式 – Aspose.Cells Cloud API 参考（v3.0）"
---

## REST API

此 REST API 用于为 Excel 工作簿中某范围单元格设置**样式**。

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## 安全性与身份验证

Aspose.Cells Cloud API 是安全的，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称        | 类型   | 位置 | 描述                           |
|----------------|--------|------|--------------------------------|
| **name**       | string | path | 工作簿名称。                   |
| **sheetName**  | string | path | 工作表名称。                   |
| **range**      | string | query | 单元格范围（例如 `A1:A10`）。 |
| **style**      | object | body | 定义要应用样式的 JSON 对象。   |
| **folder**     | string | query | 包含该工作簿的文件夹。         |
| **storageName**| string | query | 存储名称。                     |

#### Style 对象
`style` JSON 对象表示单元格格式设置，可包含以下任选属性：

- **Font** – 字体设置（`Name`、`Size`、`IsBold`、`IsItalic`、`Color` 等）。  
- **BackgroundColor** – 背景颜色，采用 ARGB 格式。  
- **ForegroundColor** – 前景颜色，采用 ARGB 格式。  
- **Name**、**CultureCustom**、**Custom** – 其他样式元数据。

## **响应**

返回 `CellCloudResponse`。

- **响应字段概览**

| 字段            | 类型    | 描述         |
| --------------- | ------- | ------------ |
| `Status`        | string  |              |
| `Code`          | integer | 200, 400, 401, 500, ... |

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                         |
|--------|------------------|----------------------------------------------|
| 200    | OK（成功）       | 筛选成功应用；响应包含操作详细信息。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。               |

## 如何使用 PostUpdateWorksheetRangeStyle API（通过 SDK）

### PostUpdateWorksheetRangeStyle API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) 提供了完整模式。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}