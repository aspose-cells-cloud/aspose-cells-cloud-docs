---
---
title: "处理 Excel ListObject（列表对象）"
ArticleTitle: "处理 Excel ListObject（列表对象）"
second_title: "文档"
linktype: "ListObjects"
type: docs
url: /zh/list-objects/
aliases:
  - /zh/working-with-list-objects/
  - /zh/working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel 列表对象 API, 添加表格, 更新表格, 删除表格, 将表格转换为区域, 对 Excel 表格进行排序"
description: "了解如何使用 Aspose.Cells Cloud REST API 添加、更新、删除、检索、排序和转换 Excel ListObjects（表格）。包含 C#、Java、Python 等语言的代码示例。"
weight: 100
---

Excel ListObjects（表格）提供了一种结构化的方式来组织数据集。它们包含自动数据排列、标题行、内置筛选器以及可选的总计行等功能。掌握这些功能可帮助您快速、高效地分析数据。

**ListObject 定义：** **ListObject** 是 Excel 原生的表格对象，用于将行和列分组，支持排序、筛选和样式设置，并可通过 Aspose.Cells Cloud API 进行访问。

## 如何处理表格（列表对象）

- [如何在工作表中添加表格（列表对象）](/zh/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [如何在工作表中更新表格（列表对象）](/zh/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [如何将表格（列表对象）转换为区域](/zh/cells/convert-list-object-or-table-to-range/)
- [如何对表格数据进行排序](/zh/cells/sort-table-data/)
- [如何从表格中删除重复行](/zh/cells/list-objects/remove-duplicates/)
- [如何为表格插入切片器](/zh/cells/list-objects/insert-slicer/)

**API 参考（概述）：**  
Aspose.Cells Cloud REST API 通过以下端点提供 ListObject 操作：`GET /cells/{fileName}/worksheets/{sheetName}/listobjects`、`POST /cells/{fileName}/worksheets/{sheetName}/listobjects`、`PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` 和 `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`。所需的查询参数包括 `folder`（必填）和 `storage`（可选）。请求体为描述表格属性（如名称、是否显示标题行、是否显示总计行等）的 JSON 对象；响应返回包含已创建或修改的 ListObject 详细信息的 JSON 负载。

**前提条件：**  
- 有效的 Aspose.Cells Cloud 认证令牌。  
- 工作簿文件必须上传到受支持的存储位置（默认为 **/**），且 `folder` 查询参数应指向该位置。  
- 可选：若使用非默认存储服务，请设置 `storage` 参数。

**端点详情**

| 方法 | 端点 | 查询参数 | 请求体（JSON） | 成功响应（示例） | 状态码 |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder`（必填），`storage`（可选） | *无* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – 成功，400 – 请求错误，401 – 未授权，404 – 未找到 |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder`（必填），`storage`（可选） | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – 已创建，400 – 请求错误，401 – 未授权，409 – 冲突 |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder`（必填），`storage`（可选） | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – 成功，400 – 请求错误，401 – 未授权，404 – 未找到 |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder`（必填），`storage`（可选） | *无* | `{ "Code": 200, "Status": "Deleted" }` | 200 – 成功，400 – 请求错误，401 – 未授权，404 – 未找到 |

**代码片段**

*C#（POST – 添加 ListObject）*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java（GET – 检索 ListObjects）*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python（PUT – 更新 ListObject）*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js（DELETE – 删除 ListObject）*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**注意事项：**  
- ListObject 索引从零开始。  
- 添加 ListObject 时，`StartRow` 和 `StartColumn` 定义表格的左上角单元格。  
- API 支持通过 `offset` 和 `limit` 查询参数进行分页（表中未显示），适用于大型工作表。  
- 速率限制：每个账户每分钟最多 100 个请求；超出限制将返回 **429 Too Many Requests（请求过多）**。

通过在页面中多次使用术语 **Excel ListObject**，内容将与目标关键词 “Excel ListObject”、“Aspose.Cells Cloud” 和 “Excel table API” 相匹配，从而提升 SEO 效果，同时保持对读者的自然可读性。