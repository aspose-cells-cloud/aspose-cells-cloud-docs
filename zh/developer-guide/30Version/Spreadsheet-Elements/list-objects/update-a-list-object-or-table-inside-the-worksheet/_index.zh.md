---
title: "更新 Excel 工作表中的列表对象"
ArticleTitle: "更新 Excel 工作表中的列表对象 – Aspose.Cells Cloud API 文档"
second_title: "文档"
linktitle: "更新"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, 更新表格, Excel API, REST, 云 SDK, 列表对象更新, Excel 工作表, 表格"
description: "了解如何使用 Aspose.Cells Cloud API（v3.0）更新 Excel 表格。内容包括端点、参数、示例 cURL、错误代码及 SDK 示例。"
weight: 20
---

此 REST API 可用于更新 Excel 工作表中**列表对象**（表格）的属性。

## 安全性与身份验证

Aspose.Cells Cloud API 采用安全机制，需要使用基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## 请求体结构

`listObject` 数据传输对象（DTO）包含以下字段。请求体中仅需包含您希望修改的字段。

| 字段                                              | 类型                 | 是否必需 | 描述                                                             |
| ------------------------------------------------- | -------------------- | -------- | ---------------------------------------------------------------- |
| **DisplayName**                                   | 字符串（string）     | 可选     | 表格的显示名称。                                                 |
| **StartRow** / **StartColumn**                    | 整数（integer）      | 可选     | 表格起始行/列的从零开始索引。                                    |
| **EndRow** / **EndColumn**                        | 整数（integer）      | 可选     | 表格末尾行/列的从零开始索引。                                    |
| **Range**                                         | 字符串（string）     | 可选     | 以 A1 样式表示的地址，定义表格范围（例如：`A1:D10`）。           |
| **ShowHeaderRow**                                 | 布尔值（boolean）    | 可选     | 为 `true` 时显示标题行。                                         |
| **ShowTotals**                                    | 布尔值（boolean）    | 可选     | 为 `true` 时显示总计行。                                         |
| **TableStyleName**                                | 字符串（string）     | 可选     | 要应用的内置表格样式名称。                                       |
| **TableStyleType**                                | 字符串（string）     | 可选     | 样式类型（如 `TableStyleLight`、`TableStyleMedium` 等）。        |
| **ListColumns**                                   | 对象数组（array）    | 可选     | 列定义集合（包含 `Name`、`TotalsCalculation` 等字段）。          |
| **Sorter**、**AutoFilter**、**ShowTableStyle…**  | 对象（object）       | 可选     | 高级样式与筛选选项（完整 DTO 详见 OpenAPI 规范）。               |

### 最小示例请求体

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **请求参数**

| 参数名称            | 类型     | 位置   | 描述                                   |
| ------------------- | -------- | ------ | -------------------------------------- |
| **name**            | 字符串   | 路径   | 文档名称。                             |
| **sheetName**       | 字符串   | 路径   | 工作表名称。                           |
| **listObjectIndex** | 整数     | 路径   | 要更新的列表对象索引。                 |
| **listObject**      | 对象     | 请求体 | 请求体中的 ListObject DTO 对象。       |
| **folder**          | 字符串   | 查询   | 包含该文档的文件夹。                   |
| **storageName**     | 字符串   | 查询   | 存储空间名称。                         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) 定义了一个公开可用的编程接口，您可直接在网页浏览器中发起 REST 调用。

### 请求

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### 响应

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

成功响应包含以下字段：

| 字段                      | 类型   | 描述                                   |
| ------------------------- | ------ | -------------------------------------- |
| **Code**                  | 整数   | HTTP 状态码（200 表示成功）。          |
| **Status**                | 字符串 | 状态的文本描述。                       |
| **UpdatedObject** *（可选）* | 对象   | 更新后的 `ListObject` 表示，包含已修改的字段。 |

{{< /tab >}}

{{< /tabs >}}

## 错误响应

| HTTP 状态码 | 描述                                                     | 示例响应体                                            |
| ----------- | -------------------------------------------------------- | ----------------------------------------------------- |
| **400**     | 请求错误 — 缺少必需字段或 JSON 格式错误。               | `{ "Code": 400, "Message": "Invalid request body." }` |
| **401**     | 未授权 — JWT 令牌缺失或无效。                            | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | 未找到 — 指定的工作簿、工作表或列表对象不存在。         | `{ "Code": 404, "Message": "Resource not found." }`   |
| **500**     | 服务器内部错误 — 服务器端发生意外情况。                  | `{ "Code": 500, "Message": "Server error." }`         |

## 常见问题（FAQ）

<details>  
<summary>如何使用 Aspose.Cells Cloud API 更新列表对象？</summary>

调用 `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}` 端点。在请求体中包含您希望修改的属性（如 `DisplayName`、`ShowHeaderRow`），并在 `Authorization` 请求头中提供 JWT 令牌进行身份验证。

</details>

<details>  
<summary>更新成功后，我将收到什么响应？</summary>

返回包含 `Code: 200` 和 `Status: "OK"` 的 JSON 对象。若发生错误，响应将包含对应的 HTTP 状态码及描述问题的 `Error` 对象。

</details>

<details>  
<summary>是否可以仅更新列表对象的部分属性？</summary>

可以。请求体中仅需包含您希望修改的字段；所有省略字段将保持不变。

</details>

## 相关文档

- [添加列表对象](https://docs.aspose.cloud/cells/list-objects/add/)
- [获取列表对象](https://docs.aspose.cloud/cells/list-objects/get/)
- [删除列表对象](https://docs.aspose.cloud/cells/list-objects/delete/)

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}