---
title: "从工作表中获取单元格样式 – Aspose.Cells Cloud API"
type: docs
url: /zh/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, 单元格样式, 电子表格, 云 SDK, API 文档"
description: "了解如何使用 Aspose.Cells Cloud REST API v3 检索 Excel 工作表中特定单元格的样式。包含 cURL 示例、响应模式、状态码以及 SDK 代码片段。"
ArticleTitle: "使用 Aspose.Cells Cloud API 从工作表中获取单元格样式 – 详细指南"
---

使用此 REST API 可检索 Excel 工作表中单元格的**样式**。

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数


| 参数名称     | 类型   | 位置 | 描述                           |
| ------------ | ------ | ---- | ------------------------------ |
| name         | string | path | Excel 文档的名称。             |
| sheetName    | string | path | 工作表的名称。                 |
| cellName     | string | path | 单元格的地址（例如 A1）。      |
| folder       | string | query | 包含该文件的文件夹。           |
| storageName  | string | query | 要使用的存储名称。             |


### **响应**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                           |
|--------|----------------|------------------------------------------------|
| 200    | OK（成功）     | 筛选操作成功；响应包含操作详情。               |
| 400    | Bad Request（请求错误） | 缺少或无效的参数（例如，不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                            |
| 413    | Payload Too Large（载荷过大） | 上传的文件超出大小限制。                        |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                            |

**错误响应**  
此端点的典型错误响应遵循 Aspose.Cells 标准错误格式。例如，400 Bad Request 返回：

```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

类似地，401 Unauthorized 返回：

```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

## 如何结合 SDK 使用 GetWorksheetCellStyle API

### GetWorksheetCellStyle API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle)定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 响应模式

| 字段                     | 类型    | 描述                                                         |
| ------------------------ | ------- | ------------------------------------------------------------ |
| **Style**                | object  | 包含单元格所有样式相关属性的容器。                           |
| Style.Font               | object  | 字体设置（字体名、字号、颜色、样式标志）。                    |
| Style.Font.Color         | object  | 字体的 RGBA 颜色值。                                          |
| Style.Font.IsBold        | boolean | 若字体为粗体，则为 `true`。                                   |
| Style.Font.IsItalic      | boolean | 若字体为斜体，则为 `true`。                                   |
| Style.Font.IsStrikeout   | boolean | 若字体带删除线，则为 `true`。                                 |
| Style.Font.IsSubscript   | boolean | 若字体为下标，则为 `true`。                                   |
| Style.Font.IsSuperscript | boolean | 若字体为上标，则为 `true`。                                   |
| Style.Font.Name          | string  | 字体族名称（例如 **Calibri**）。                             |
| Style.Font.Size          | number  | 字体大小（单位：磅）。                                        |
| Style.Font.Underline     | string  | 下划线样式（例如 **Single**）。                              |
| Style.IsLocked           | boolean | 指示该单元格是否受保护、禁止编辑。                           |
| Style.IsTextWrapped      | boolean | 若启用了自动换行，则为 `true`。                               |
| Style.IsGradient         | boolean | 若应用了渐变填充，则为 `true`。                               |
| Style.Pattern            | string  | 填充图案名称（例如 **None**）。                              |
| Style.BorderCollection   | array   | 边框对象列表，定义线型、颜色和边框类型。                     |
| Style.BackgroundColor    | object  | 单元格背景的 RGBA 值。                                       |
| Style.ForegroundColor    | object  | 单元格前景的 RGBA 值。                                       |
| …                        | …       | _（其他字段遵循 API 参考中定义的相同模式。）_                |

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅**  
- [设置单元格样式](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [获取单元格值](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)