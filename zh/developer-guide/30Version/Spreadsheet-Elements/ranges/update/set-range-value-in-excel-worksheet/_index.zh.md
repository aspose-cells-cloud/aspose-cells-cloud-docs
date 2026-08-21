---
title: "在 Excel 工作表中设置范围值"
second_title: "文档"
linktitle: "设置值"
type: docs
url: /zh/ranges/update/values/
aliases: [  /zh/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel API, 设置范围值, REST API, 云 SDK, 工作表更新"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作簿中设置单元格或范围的值。包含端点、参数、cURL 示例、SDK 代码示例及错误处理。"
weight: 72
ArticleTitle: "在 Excel 工作表中设置范围值 – Aspose.Cells Cloud API"
---

使用此 REST API 在指定范围内设置值。在适当情况下，该值将被转换为其他数据类型，并重置单元格的数字格式。

**前提条件**  
- 有效的 Aspose Cloud 账户。  
- 包含 `Cells.ReadWrite` 权限范围的 JWT 令牌。  
- 工作簿必须已上传至目标存储位置。

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

请求参数如下：

| 参数名称     | 类型    | 位置   | 描述                                   |
|--------------|---------|--------|----------------------------------------|
| name         | string  | path   | 工作簿名称                             |
| sheetName    | string  | path   | 工作表名称                             |
| value        | string  | query  | 输入值                                 |
| range        | object  | body   | 工作表中的范围对象                     |
| isConverted  | boolean | query  | 指示是否应转换输入值                   |
| setStyle     | boolean | query  | 指示是否将样式应用于目标单元格         |
| folder       | string  | query  | 工作簿所在文件夹                       |
| storageName  | string  | query  | 存储名称                               |

**可在请求体中发送的 `range` 对象示例**：

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用云 API。**请在 `Authorization` 请求头中包含有效的 JWT 令牌**。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应架构**

| 字段    | 类型    | 描述                                       |
|---------|---------|--------------------------------------------|
| Code    | integer | 操作的 HTTP 状态码                         |
| Status  | string  | 结果的简短描述（例如："OK"）               |
| Message | string  | 请求失败时的详细错误消息（可选）           |
| Result  | object  | 成功调用时返回的额外数据（可选）           |

**可能的 HTTP 状态码**

- **200 OK** – 范围值已成功设置。  
- **400 Bad Request** – 参数无效或请求体格式错误。  
- **401 Unauthorized** – 缺少或无效的 JWT 令牌。  
- **403 Forbidden** – 对所请求的操作权限不足。  
- **404 Not Found** – 指定的工作簿、工作表或范围不存在。  
- **500 Internal Server Error** – 意外服务器错误。

*400 Bad Request 的示例错误响应：*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "范围对象 'range' 缺少必需字段。"
}
```

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您能够专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}