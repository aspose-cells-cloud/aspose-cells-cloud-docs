---
title: "更新 Excel 工作表中的图形"
second_title: "文档"
linktitle: "更新"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "更新 Excel 图形 API、Aspose.Cells Cloud、Excel 图形更新、REST API、SDK、C#、Java、Python、Node.js、Go、Ruby、PHP、Perl、Swift"
description: "了解如何使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中的图形。内容包括 HTTPS 端点、身份验证详情、数据传输对象（DTO）架构、分步使用说明、cURL 示例及多种编程语言的 SDK 代码示例。"
ArticleTitle: "更新 Excel 工作表中的图形 - Aspose.Cells Cloud API"
weight: 31
---

此 REST API 用于更新 Excel 工作表中的图形。

## 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### 请求参数

| 参数名称         | 类型    | 位置   | 描述                                                                 |
| ---------------- | ------- | ------ | -------------------------------------------------------------------- |
| **name**         | string  | 路径   | 工作簿文件的名称。                                                   |
| **sheetName**    | string  | 路径   | 包含目标图形的工作表名称。                                           |
| **shapeindex**   | integer | 路径   | 图形在工作表中的从零开始的索引。                                     |
| **dto**          | object  | 请求体 | 包含待更新属性的数据传输对象（见下方 _DTO 架构_）。                 |
| **folder**       | string  | 查询   | 工作簿所在的文件夹。                                                 |
| **storageName**  | string  | 查询   | Aspose Cloud 存储空间的名称。                                        |

### DTO 架构

`dto` 对象包含可更新的属性字段。除特别说明外，所有字段均为可选。

| 字段                | 类型    | 必填 | 描述                                                                 |
| ------------------- | ------- | ---- | -------------------------------------------------------------------- |
| **Name**            | string  | 否   | 图形的新名称。                                                       |
| **UpperLeftRow**    | integer | 否   | 图形左上角所在的行索引。                                             |
| **UpperLeftColumn** | integer | 否   | 图形左上角所在的列索引。                                             |
| **Width**           | integer | 否   | 图形宽度（单位：磅）。                                               |
| **Height**          | integer | 否   | 图形高度（单位：磅）。                                               |
| **RotationAngle**   | integer | 否   | 旋转角度（单位：度）。                                               |
| **IsHidden**        | boolean | 否   | `true` 表示隐藏图形。                                                |
| **IsLocked**        | boolean | 否   | `true` 表示锁定图形。                                                |
| **Font**            | object  | 否   | 字体设置（子属性详见 OpenAPI 规范）。                                |
| **...**             | …       | 否   | 其他属性，如 `HtmlText`、`AlternativeText`、`ZOrderPosition` 等。   |

> 完整字段列表请参阅官方 OpenAPI 规范：<https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>

### 请求头

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>`（来自 _身份验证_ 步骤的 JWT 令牌）

### 请求体示例

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## 使用 cURL（命令行工具）的示例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### 响应示例

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**错误处理** – API 可能返回以下状态码：

| 状态码 | 含义             | 常见原因                                             |
| ------ | ---------------- | ---------------------------------------------------- |
| 400    | 请求无效（Bad Request） | JSON 格式错误或缺少必要字段。                         |
| 401    | 未授权（Unauthorized）  | 缺失或无效的 JWT 令牌。                               |
| 404    | 未找到（Not Found）     | 工作簿、工作表或图形索引不存在。                      |
| 500    | 服务器内部错误（Internal Server Error） | 服务器端意外错误。                               |

**错误响应示例**

*400 – 请求无效*

```json
{
  "Code": 400,
  "Message": "Invalid request payload. 'Name' field exceeds maximum length."
}
```

*401 – 未授权*

```json
{
  "Code": 401,
  "Message": "Authentication failed. Invalid or expired JWT token."
}
```

*404 – 未找到*

```json
{
  "Code": 404,
  "Message": "The specified workbook, worksheet, or shape index was not found."
}
```

*500 – 服务器内部错误*

```json
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

## 云 SDK 工具集

使用 SDK 是加速开发的最优方式。SDK 封装了底层细节，让您专注于业务逻辑与项目任务。请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}