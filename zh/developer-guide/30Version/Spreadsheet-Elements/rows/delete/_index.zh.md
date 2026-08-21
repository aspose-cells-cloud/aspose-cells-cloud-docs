---
title: "在 Excel 工作表中删除行"
second_title: "文档"
linktitle: "删除"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, 删除行, Excel API, REST, 云端, 电子表格, Excel, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表中删除单行或多行。包含适用于 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift 的代码示例。"
weight: 20
ArticleTitle: "在 Excel 工作表中删除行 – Aspose.Cells Cloud API 指南"
---

## 可用删除操作

以下示例演示如何使用 Aspose.Cells Cloud REST API 从 Excel 工作表中删除单个空行或多行。

- [如何删除 Excel 工作表中的空行](/cells/rows/delete/row/)
- [如何删除 Excel 工作表中的多行](/cells/rows/delete/rows/)

**API 参考**

| 项目                | 详情 |
|---------------------|---------------------------------------------------------------|
| **HTTP 方法**     | DELETE |
| **端点**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **路径参数**| `fileName` – Excel 文件名（必需）<br>`sheetName` – 工作表名称（必需） |
| **查询参数**| `startrow` – 要删除的第一行的索引（必需）<br>`totalRows` – 要删除的行数（必需）<br>`storage` – 云存储名称（可选）<br>`folder` – 存储中的文件夹路径（可选） |
| **请求体**    | *无* |
| **响应示例**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **可能的状态码**| 200 OK – 行删除成功<br>400 Bad Request – 参数无效<br>401 Unauthorized – 身份验证失败<br>404 Not Found – 文件或工作表未找到<br>500 Internal Server Error – 服务器端问题 |

**另请参阅**

- [添加行](/cells/rows/add/)
- [获取行](/cells/rows/get/)
- [复制行](/cells/rows/copy/)
- [隐藏行](/cells/rows/hide/)
- [行概述](/cells/rows/)
---