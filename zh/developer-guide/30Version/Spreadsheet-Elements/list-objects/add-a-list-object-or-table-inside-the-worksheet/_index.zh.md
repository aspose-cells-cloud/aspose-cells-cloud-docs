---
title: "向 Excel 工作表添加列表对象（表格）"
second_title: "文档"
linktitle: "添加"
type: docs
url: /zh/list-objects/add/
aliases: [  /zh/add-a-list-object-or-table-inside-the-worksheet/ , /zh/tables/add/ ]
keywords: "Aspose.Cells Cloud、Excel API、列表对象、表格、REST API、工作表"
description: "了解如何使用 Aspose.Cells Cloud REST API 向工作表添加列表对象（Excel 表格）。包含端点、参数、身份验证步骤、cURL 示例和 SDK 代码示例。"
weight: 10
ArticleTitle: "向 Excel 工作表添加列表对象（表格） – Aspose.Cells Cloud 文档"
---

此 REST API 可向 Excel 工作表添加**列表对象（表格）**。

在使用此端点前，请确保您已获取有效的 JWT 令牌、工作簿存储在受支持的云存储中，且目标工作表已存在。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### 请求参数

| 参数名称        | 类型    | 位置   | 描述                                                       |
| --------------- | ------- | ------ | ---------------------------------------------------------- |
| **name**        | string  | 路径   | 工作簿文件名。                                             |
| **sheetName**   | string  | 路径   | 工作表名称。                                               |
| **startRow**    | integer | 查询   | 表格区域首行的从零开始索引。                               |
| **startColumn** | integer | 查询   | 表格区域首列的从零开始索引。                               |
| **endRow**      | integer | 查询   | 表格区域末行的从零开始索引。                               |
| **endColumn**   | integer | 查询   | 表格区域末列的从零开始索引。                               |
| **hasHeaders**  | boolean | 查询   | 若首行包含列标题则为 `true`，否则为 `false`。             |
| **listObject**  | object  | 请求体 | 列表对象定义（详见 **请求体架构**）。                      |
| **folder**      | string  | 查询   | 包含工作簿的文件夹。                                       |
| **storageName** | string  | 查询   | 存储名称。                                                 |

### 请求体架构

**listObject** 对象描述将创建的表格。仅列出最常用属性；完整属性列表请参阅 OpenAPI 规范。

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### 示例请求（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### 示例响应

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 错误代码

| HTTP 状态码 | 原因             | 描述                             |
| ----------- | ---------------- | -------------------------------- |
| **400**     | 错误请求         | 范围参数无效或 JSON 请求体格式错误。 |
| **401**     | 未授权           | 缺失或已过期的 JWT 令牌。          |
| **404**     | 未找到           | 指定的工作簿或工作表不存在。       |
| **500**     | 内部服务器错误   | 服务器端意外错误。                 |

**示例 400 响应**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**示例 401 响应**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) 提供了此操作的完整接口定义。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}