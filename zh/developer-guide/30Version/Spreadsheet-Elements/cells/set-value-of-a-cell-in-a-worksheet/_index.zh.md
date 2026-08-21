---
title: "设置单元格值 – Aspose.Cells Cloud API 参考（v3.0）"
type: docs
url: /zh/set-value-of-a-cell-in-a-worksheet/
weight: 70
keywords: "Aspose Cells API 设置单元格值、Excel 单元格更新 REST、Aspose.Cells Cloud cURL 示例"
description: "了解如何使用 Aspose.Cells Cloud REST API 设置 Excel 工作表中特定单元格的值。包含请求语法、参数、HTTPS cURL 示例以及 SDK 代码示例。"
---

此 REST API 可用于设置 Excel 文件中的**单元格值**。

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## 安全与身份验证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

**请求参数**

| 名称            | 类型     | 位置   | 描述                                         |
|-----------------|----------|--------|----------------------------------------------|
| name            | string   | path   | Excel 文档的名称（包括扩展名）。             |
| sheetName       | string   | path   | 工作表的名称（区分大小写）。                 |
| cellName        | string   | path   | 目标单元格的 A1 样式地址（例如 `A1`）。       |
| value           | string   | query  | 要分配给单元格的值。                         |
| type            | string   | query  | 值的数据类型（`int`、`string`、`float` 等）。|
| formula         | string   | query  | 应用于单元格的公式（可选）。                 |
| folder          | string   | query  | 包含文档的文件夹（可选）。                   |
| storageName     | string   | query  | 文件所在存储的名称（可选）。                 |

## **响应**

返回 `CellResponse`。

- **响应字段概览**

| 字段              | 类型     | 描述                                               |
| ----------------- | -------- | -------------------------------------------------- |
| `Name`            | string   | 单元格地址（例如 `F341`）。                        |
| `Row`             | integer  | 从零开始的行索引。                                 |
| `Column`          | integer  | 从零开始的列索引。                                 |
| `Value`           | string   | 单元格的显示值。                                   |
| `Type`            | string   | 单元格的数据类型（例如 `IsString`）。             |
| `Formula`         | string   | 若单元格包含公式，则为公式文本。                   |
| `IsFormula`       | bool     | 表示单元格是否包含公式。                           |
| `IsMerged`        | bool     | 表示单元格是否属于合并区域。                       |
| `IsArrayHeader`   | bool     | 表示单元格是否为数组标题。                         |
| `IsInArray`       | bool     | 表示单元格是否属于数组。                           |
| `IsErrorValue`    | bool     | 表示单元格是否包含错误值。                         |
| `IsInTable`       | bool     | 表示单元格是否在表格内。                           |
| `IsStyleSet`      | bool     | 表示是否已为单元格应用样式。                       |
| `HtmlString`      | string   | 单元格值的 HTML 编码表示形式。                     |
| `Style.link`      | object   | 指向样式资源的超链接。                             |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                           |
|--------|-------------------|------------------------------------------------|
| 200    | OK（成功）        | 筛选应用成功；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（负载过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                           |

## 如何使用 SDK 调用 PostWorksheetCellSetValue API

### PostWorksheetCellSetValue API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) 定义了一个公开可访问的编程接口，使开发人员能够直接从浏览器或任何 HTTP 客户端调用 REST 端点。

您可以使用 **cURL** 命令行工具调用 Aspose.Cells Web 服务。下面的示例演示如何使用 cURL 设置单元格值。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可加快开发速度，因为它会处理底层细节，使您能专注于项目本身。有关 Aspose.Cells Cloud SDK 的完整列表，请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
---