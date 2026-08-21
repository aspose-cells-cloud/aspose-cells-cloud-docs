---
title: "Aspose.Cells Cloud API – 使用 CellsObjectOperate 任务（REST）"
second_title: "文档"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "了解如何在 Aspose.Cells Cloud API 中使用 CellsObjectOperate 任务，包括参数参考、请求/响应示例以及针对工作表、图表和数据透视表的最佳实践建议。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – 使用 CellsObjectOperate 任务（REST）"
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate 任务"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "图表操作"
  - "数据透视表 API"
  - "分页符 API"
---

**概述**  
**CellsObjectOperate** 任务允许您通过单次 REST 调用对 Excel 对象（例如工作簿、工作表、图表、数据透视表、形状、分页符等）执行创建、读取、更新和删除（CRUD）操作。通过 `OperateObjectType` 指定对象类型，并提供相应的参数块（例如，对于图表相关操作使用 `ChartOperateParameter`）。

---

**OperateObject**

| 参数名称                | 类型   | 描述 |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | 要操作的 Excel 对象类型。允许的值包括：`Workbook`（工作簿）、`Worksheet`（工作表）、`PageSetup`（页面设置）、`Cells`（单元格）、`Chart`（图表）、`Shape`（形状）、`ListObject`（列表对象）、`PivotTable`（数据透视表）、`WorkbookSettings`（工作簿设置）、`PageBreak`（分页符）。 |
| OperateObjectPosition   | object | 用于标识目标对象位置的容器（例如工作簿名称、工作表名称、图表索引）。大多数操作都需要此项。 |

**OperateObjectPosition**

| 参数名称         | 类型   | 描述 |
| ---------------- | ------ | ----------- |
| Workbook         | object | 包含目标对象的工作簿。必须包含 `FileName`（云存储）或 `FileContent`（Base64 编码）。 |
| SheetName        | string | 应用操作的工作表名称。对于工作表级对象（如图表、形状等）为必需项。 |
| ChartIndex       | integer| 工作表中图表的从零开始的索引（当 `OperateObjectType` 为 `Chart` 时使用）。 |
| ShapeIndex       | integer| 工作表中形状的从零开始的索引（当 `OperateObjectType` 为 `Shape` 时使用）。 |
| CellName         | string | A1 样式的单元格引用（例如 `A1`）。用于单元格级操作。 |
| ListObjectIndex  | integer| 列表对象的从零开始的索引（当 `OperateObjectType` 为 `ListObject` 时使用）。 |

**ChartOperateParameter**

| 参数名称              | 类型    | 描述 |
| --------------------- | ------- | ----------- |
| ChartIndex            | integer | 要修改的图表索引。更新现有图表时为必需项。 |
| ChartType             | string  | 要创建的图表类型（例如 `Bar`、`Line`、`Pie`）。 |
| UpperLeftRow          | integer | 图表左上角所在的行号（从零开始）。 |
| UpperLeftColumn       | integer | 图表左上角所在的列号（从零开始）。 |
| LowerRightRow         | integer | 图表右下角所在的行号。 |
| LowerRightColumn      | integer | 图表右下角所在的列号。 |
| Area                  | string  | 图表的数据范围（例如 `A1:B5`）。 |
| IsVertical            | string  | 图表方向是否为垂直；若为垂直则为 `true`，否则为 `false`。 |
| CategoryData          | string  | 提供分类（X 轴）标签的数据范围。 |
| IsAutoGetSerialName   | string  | 是否自动生成系列名称；若为 `true` 则自动生成，否则为 `false`（使用自定义名称）。 |
| Title                 | string  | 图表上显示的标题文本。 |

**ListObjectOperateParameter**

| 参数名称     | 类型   | 描述 |
| ------------ | ------ | ----------- |
| ListObject   | object | 用于列表（表格）操作的配置对象。包括 `ShowHeader`、`ShowTotal` 和 `Style` 等属性。 |

**PageBreakOperateParameter**

| 参数名称     | 类型    | 描述 |
| ------------ | ------- | ----------- |
| PageBreakType| string  | 分页符类型（`Horizontal` 或 `Vertical`）。 |
| Index        | integer | 要删除或修改的分页符的从零开始的索引。 |
| Row          | integer | 水平分页符所在行号。 |
| Column       | integer | 垂直分页符所在列号。 |
| StartIndex   | integer | 基于范围的分页符操作的起始索引。 |
| EndIndex     | integer | 基于范围的分页符操作的结束索引。 |

**PageSetupOperateParameter**

| 参数名称   | 类型   | 描述 |
| ---------- | ------ | ----------- |
| PageSetup  | object | 页面布局设置（页边距、方向、纸张大小等）。 |

**PivotTableOperateParameter**

| 参数名称         | 类型        | 描述 |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | 数据透视表目标区域的左上角单元格（例如 `C5`）。 |
| SourceData       | string      | 数据透视表的源数据范围（例如 `A1:D100`）。 |
| TableName        | string      | 为创建的数据透视表指定的名称。 |
| UseSameSource    | string      | 是否复用现有源数据范围；若为 `true` 则复用，否则为 `false`（新建源数据）。 |
| PivotTableIndex  | integer     | 要更新的数据透视表索引（修改/删除操作时为必需项）。 |
| PivotFieldRows   | integer[]   | 将出现在行区域的字段索引集合。 |
| PivotFieldColumns| integer[]   | 将出现在列区域的字段索引集合。 |
| PivotFieldData   | integer[]   | 将出现在数据区域的字段索引集合。 |

**ShapeOperateParameter**

| 参数名称 | 类型   | 描述 |
| -------- | ------ | ----------- |
| Shape    | object | 形状定义（类型、位置、大小、文本等）。 |

**WorkbookSettingsOperateParameter**

| 参数名称         | 类型   | 描述 |
| ---------------- | ------ | ----------- |
| WorkbookSettings | object | 影响整个工作簿的设置（例如计算模式、精度等）。 |

**WorksheetOperateParameter**

| 参数名称        | 类型   | 描述 |
| --------------- | ------ | ----------- |
| Name            | string | 要操作的工作表当前名称。 |
| SheetType       | string | 工作表类型（`Worksheet`、`Chart` 等）。 |
| NewName         | string | 重命名时的新工作表名称。 |
| MovingRequest   | object | 移动工作表的参数（例如 `FromIndex`、`ToIndex`）。 |

## REST API

| API                | 类型 | 描述 | 资源链接 |
| ------------------ | ---- | ----------- | ------------- |
| /cells/task/runtask| POST | 运行任务    | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

### 前提条件
- **身份验证** – 必须包含有效的 `Authorization: Bearer <access_token>` 请求头。  
- **存储** – 源工作簿必须存储在 Aspose Cloud 存储中，或以 Base64 编码形式在请求体中提供。  
- **API 版本** – 本文档面向 **v3.0** 版本的 Aspose.Cells Cloud API。

### 示例请求（cURL）

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

请求体遵循如下定义的 **CellsObjectOperateRequest** 模式：

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* 为简洁起见，省略了其他定义 */
  }
}
```

### 示例响应（成功 – 200）

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Chart created successfully."
  }
}
```

响应包含以下字段：

| 字段        | 类型   | 描述 |
| ----------- | ------ | ----------- |
| Code        | integer| 任务引擎返回的类 HTTP 状态码。 |
| Status      | string | 可读的状态信息（例如 `OK`）。 |
| TaskId      | string | 异步任务的标识符。 |
| Result      | object | 包含操作特定结果的对象。 |
| Result.ChartId | integer | 已创建或已修改图表的标识符。 |
| Result.Message | string | 描述操作结果的简短消息。 |

### 错误处理

| HTTP 状态码 | 错误代码           | 描述                         | 建议解决方案 |
| ----------- | ------------------ | ---------------------------- | ------------ |
| 400         | InvalidParameter   | 请求参数缺失或格式错误。      | 检查必填字段及其数据类型。 |
| 401         | Unauthorized       | 身份验证令牌无效或缺失。      | 刷新访问令牌，并在 `Authorization` 请求头中包含它。 |
| 404         | NotFound           | 指定的工作簿、工作表或对象不存在。 | 检查 `FileName`、`SheetName` 以及对象索引。 |
| 500         | ServerError        | 服务器发生意外错误。          | 重试请求；若问题持续，请联系支持团队。 |

### 常见使用场景
- 向工作表添加新图表。  
- 重命名工作表（`OperateObjectType = "Worksheet"` 并配合 `WorksheetOperateParameter.NewName`）。  
- 插入分页符（`OperateObjectType = "PageBreak"` 并配合 `PageBreakOperateParameter`）。  
- 更新数据透视表源数据（`OperateObjectType = "PivotTable"` 并配合 `PivotTableOperateParameter.SourceData`）。  
- 修改工作簿设置（例如计算模式）（`OperateObjectType = "WorkbookSettings"`）。  

---  

*所有描述均基于官方 Aspose.Cells Cloud OpenAPI 规范。*
---