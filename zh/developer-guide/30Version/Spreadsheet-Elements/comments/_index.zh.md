---
title: "处理 Excel 评论"
second_title: "文档"
linktitle: "评论"
type: docs
url: /zh/comments/
aliases: [/zh/working-with-comments/]
keywords: "Aspose.Cells Cloud, Excel 评论 API, 电子表格评论, REST API"
description: "学习如何使用 Aspose.Cells Cloud REST API v3.0 添加、获取、更新和删除 Excel 评论，包含代码示例、前置条件及错误处理。"
weight: 100
ArticleTitle: "处理 Excel 评论 – Aspose.Cells Cloud API 指南"
---

在创建 Excel 工作簿时，用户出于多种原因可添加评论。常见用途包括解释单元格中的公式（尤其当文件将与他人共享时），也可作为提醒、协作者备注，或用于与其他工作簿交叉引用。添加评论后，Excel 允许用户调整评论框大小、形状并进行格式设置，以符合个人偏好风格。掌握评论管理技巧有助于用户充分发掘该功能的潜力。

**前置条件**

- 有效的 Aspose.Cells Cloud 账户。  
- 通过 OAuth 2.0 获取的**访问令牌（access token）**。  
- API 版本 **v3.0**（本指南所用端点均属于该版本）。  
- 可选：使用 Aspose.Cells SDK（适用于您偏好的编程语言），以简化请求构造过程。

**版本说明**

以下示例基于 **Aspose.Cells Cloud REST API v3.0**。未来 API 版本可能引入新增参数或修改响应结构，请始终查阅最新 API 文档以获取最新详情。

**添加评论**

要添加评论，请向以下端点发送 **POST** 请求：

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**路径参数**

| 参数名    | 类型   | 必填 | 描述                                   |
|-----------|--------|------|----------------------------------------|
| `file`    | 字符串 | 是   | 工作簿文件名（含扩展名）。             |
| `sheet`   | 字符串 | 是   | 将添加评论的工作表名称。               |

**请求体字段说明**

| 字段名    | 类型   | 必填 | 描述                             |
|-----------|--------|------|----------------------------------|
| `CellName`| 字符串 | 是   | 单元格的 A1 样式地址（例如 **B2**）。 |
| `Comment` | 字符串 | 是   | 要保存的评论文本内容。             |
| `Author`  | 字符串 | 否   | 评论作者姓名。                     |

**请求体示例**

```json
{
  "CellName": "B2",
  "Comment": "需要审阅",
  "Author": "张三"
}
```

**成功响应示例**（`200 OK`）

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "张三",
    "HtmlComment": "需要审阅",
    "Note": "需要审阅"
  }
}
```

**常见错误码**

| 状态码 | 含义                             |
|--------|----------------------------------|
| 400    | 单元格地址无效或请求体格式错误   |
| 401    | 未授权 — 缺失或无效的访问令牌    |
| 404    | 工作簿或工作表未找到             |

**获取评论**

获取工作表中的所有评论：

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**路径参数**

| 参数名  | 类型   | 必填 | 描述             |
|---------|--------|------|------------------|
| `file`  | 字符串 | 是   | 工作簿文件名。   |
| `sheet` | 字符串 | 是   | 工作表名称。     |

**响应示例**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "李四",
      "HtmlComment": "初始值",
      "Note": "初始值"
    },
    {
      "CellName": "B2",
      "Author": "张三",
      "HtmlComment": "需要审阅",
      "Note": "需要审阅"
    }
  ]
}
```

**更新评论**

要修改现有评论，请发送 **PUT** 请求。评论通过其在工作表评论集合中的**索引**标识（索引从 0 开始）。

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**路径参数**

| 参数名         | 类型   | 必填 | 描述                           |
|----------------|--------|------|--------------------------------|
| `file`         | 字符串 | 是   | 工作簿文件名。                 |
| `sheet`        | 字符串 | 是   | 工作表名称。                   |
| `commentIndex` | 整数   | 是   | 待更新评论的从 0 开始的索引值。 |

**请求体字段说明**

| 字段名    | 类型   | 必填 | 描述                   |
|-----------|--------|------|------------------------|
| `Comment` | 字符串 | 是   | 新的评论文本内容。     |
| `Author`  | 字符串 | 否   | 更新后的作者姓名（可选）。 |

**请求体示例**

```json
{
  "Comment": "更新后的备注内容",
  "Author": "张三"
}
```

响应结构与**添加评论**的响应结构相同。

**删除评论**

根据索引删除单条评论：

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**路径参数**

| 参数名         | 类型   | 必填 | 描述                         |
|----------------|--------|------|------------------------------|
| `file`         | 字符串 | 是   | 工作簿文件名。               |
| `sheet`        | 字符串 | 是   | 工作表名称。                 |
| `commentIndex` | 整数   | 是   | 待删除评论的从 0 开始的索引值。 |

删除成功后返回：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**删除所有评论**

清空工作表中所有评论：

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**路径参数**

| 参数名  | 类型   | 必填 | 描述         |
|---------|--------|------|--------------|
| `file`  | 字符串 | 是   | 工作簿文件名。 |
| `sheet` | 字符串 | 是   | 工作表名称。   |

**错误处理指南**

- **404 Not Found（未找到）** —— 请核实工作簿 ID、工作表名称及评论索引是否正确。  
- **400 Bad Request（错误请求）** —— 请检查 JSON 语法及必填字段（`CellName`、`Comment`）。  
- **429 Too Many Requests（请求过多）** —— 请实现指数退避机制，并遵守 `Retry-After` 响应头提示。

**小结**

- Excel 评论可用于[为单元格添加备注或解释公式](/zh/cells/comments/add/)。  
- Excel 提供了灵活的[编辑](/zh/cells/comments/update/)、[删除](/zh/cells/comments/delete/)、[显示](/zh/cells/comments/get/)或[隐藏](/zh/cells/comments/update/)工作表中评论的功能。  
- 用户还可[调整](/zh/cells/comments/update/)和[移动](/zh/cells/comments/update/)评论框位置与大小。  

如需了解处理其他电子表格元素的更多信息，请参阅 [处理单元格](/zh/cells/working-with-cells/) 指南。