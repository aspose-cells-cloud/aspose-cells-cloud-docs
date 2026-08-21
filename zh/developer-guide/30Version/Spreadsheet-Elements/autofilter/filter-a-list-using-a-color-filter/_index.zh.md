---
title: "在 Excel 工作表中添加颜色筛选器"
second_title: "文档"
linktitle: "添加颜色筛选器"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: "Excel, 颜色筛选器, Aspose.Cells Cloud, REST API, 自动筛选, JWT 身份验证"
description: "了解如何使用 Aspose.Cells Cloud API 为 Excel 工作表应用颜色筛选器。包含端点、参数、cURL 示例、错误处理和 SDK 示例。"
weight: 65
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中添加颜色筛选器"
---

了解如何使用 Aspose.Cells Cloud API 为 Excel 工作表添加颜色筛选器。本指南涵盖所需端点、参数、身份验证前提条件、示例 cURL 请求、SDK 示例以及响应处理。

此 REST API 可向 Excel 工作表添加**颜色筛选器**。

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数：

| 参数名称       | 类型    | 位置   | 描述                                                                 |
|----------------|---------|--------|----------------------------------------------------------------------|
| name           | string  | 路径   | Excel 文件的名称。                                                  |
| sheetName      | string  | 路径   | 包含待筛选数据的工作表名称。                                         |
| range          | string  | 查询   | 应用筛选器的单元格范围（例如 `A1:B10`）。                           |
| fieldIndex     | integer | 查询   | 应用颜色筛选器的列的从零开始索引。                                   |
| colorFilter    | object  | 请求体 | 定义前景色和背景色的 JSON 对象。                                     |
| matchBlanks    | boolean | 查询   | 是否将空单元格所在的行包含在筛选结果中。                            |
| refresh        | boolean | 查询   | 若为 `true`，则在应用筛选器后刷新工作表。                           |
| folder         | string  | 查询   | 存储中 Excel 文件所在的文件夹。                                      |
| storageName    | string  | 查询   | 存储服务的名称（例如 Aspose Cloud Storage）。                        |

**`colorFilter` JSON 结构定义**

| 属性              | 类型   | 描述                                                                                       | 必填 |
|-------------------|--------|--------------------------------------------------------------------------------------------|------|
| Pattern           | string | 筛选模式（例如 `"Solid"`）。                                                              | 是   |
| ForegroundColor   | object | 定义前景色。包含子属性，例如 `Color`、`ColorIndex`、`IsShapeColor`、`ThemeColor` 和 `Type`。 | 否   |
| BackgroundColor   | object | 定义背景色。子属性与 `ForegroundColor` 相同。                                              | 否   |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义                  | 描述                                           |
|--------|-----------------------|------------------------------------------------|
| 200    | OK（成功）            | 筛选器已成功应用；响应包含操作详情。           |
| 400    | Bad Request（错误请求）| 缺失或无效参数（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大）| 上传文件超出大小限制。                    |
| 500    | Internal Server Error（内部服务器错误）| 服务器发生意外错误。                  |

## 如何结合 SDK 使用 PutWorksheetColorFilter API

### PutWorksheetColorFilter API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

使用 SDK 是加快开发速度的最佳方式。SDK 封装了底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅**：[添加自定义筛选器](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/)、[添加日期筛选器](https://docs.aspose.cloud/cells/autofilter/add-date-filter/)、[移除自动筛选器](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/)。