---
title: "向 Excel 工作表添加空列 - Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "添加"
type: docs
url: /columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "添加, 列, Excel, API, Aspose.Cells, 云, REST, 插入"
description: "了解如何使用 Aspose.Cells Cloud REST API 向 Excel 工作表中插入新列。包含请求语法、cURL 示例和 SDK 代码示例。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 向 Excel 工作表添加空列"
---

此 REST API 可向工作表中插入一列或多列。

**前提条件**  
调用此接口前，请确保已完成以下步骤：

- 获取有效的 OAuth 2.0 访问令牌，并将其包含在 `Authorization` 请求头中。  
- 将目标工作簿存储在所选存储中（默认为 “Default”），或指定适当的 `folder` 和 `storageName` 参数。  
- 确认 `sheetName` 参数中提供的工作表名称存在于工作簿中。

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名              | 类型    | 位置   | 描述                                                           |
| ------------------- | ------- | ------ | -------------------------------------------------------------- |
| **name**            | string  | 路径   | 工作簿文件名。                                                 |
| **sheetName**       | string  | 路径   | 工作表名称。                                                   |
| **columnIndex**     | integer | 路径   | 插入起始列的从零开始的索引。                                   |
| **totalColumns**    | integer | 查询   | 要插入的列数。                                                 |
| **updateReference** | boolean | 查询   | 若为 **true**，单元格引用将更新以反映插入操作。               |
| **folder**          | string  | 查询   | 包含工作簿的文件夹路径。                                       |
| **storageName**     | string  | 查询   | 存储服务名称。                                                 |

**说明**

- `columnIndex` 必须介于 0 与工作表当前列数之间；超出现有范围插入将自动扩展工作表。  
- 插入多列（`totalColumns` > 1）会将现有列向右移动。  
- `updateReference` 标志默认为 `false`；若需更新公式与命名区域，请设置为 `true`。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) 定义了一个公开可访问的编程接口，您可直接在 Web 浏览器中进行 REST 交互。

您可使用 cURL 命令行工具调用 Aspose.Cells Web 服务。以下示例展示了一个完整的请求，包括身份验证与正确的路径参数。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**响应码**

| 状态码 | 描述                                 |
|--------|--------------------------------------|
| 200    | 列插入成功。                         |
| 400    | 请求错误 — 缺少或无效的参数。        |
| 401    | 未授权 — 令牌无效或缺失。            |
| 404    | 工作簿或工作表未找到。               |
| 500    | 服务器内部错误。                     |

**示例错误响应**

```json
// 400 请求错误 — 缺少或无效的参数
{
  "Code": 400,
  "Message": "无效参数：totalColumns 必须为正整数。"
}

// 401 未授权 — 令牌无效或缺失
{
  "Code": 401,
  "Message": "身份验证失败。访问令牌缺失或无效。"
}

// 404 未找到 — 工作簿或工作表不存在
{
  "Code": 404,
  "Message": "未找到工作簿 'test.xlsx'。"
}

// 500 服务器内部错误
{
  "Code": 500,
  "Message": "服务器上发生意外错误。"
}
```

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 处理底层细节，让您专注于项目逻辑。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
---