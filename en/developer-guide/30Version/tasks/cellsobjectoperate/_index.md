---
title: "Aspose.Cells Cloud API – Working with CellsObjectOperate Task (REST)"
second_title: "Document"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Learn how to use the CellsObjectOperate task in Aspose.Cells Cloud API. Detailed parameter reference, request/response examples, and best‑practice tips for operating worksheets, charts, pivot tables, and more."
weight: 20
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate task"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "chart operation"
  - "pivot table API"
  - "page break API"
---

**Overview**  
The **CellsObjectOperate** task lets you perform create, read, update, and delete (CRUD) operations on Excel objects such as workbooks, worksheets, charts, pivot tables, shapes, page breaks, and more via a single REST call. Specify the object type with `OperateObjectType` and provide the corresponding parameter block (e.g., `ChartOperateParameter` for chart‑related actions).

---

**OperateObject**

| Parameter Name          | Type   | Description |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | The type of Excel object to operate on. Allowed values: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | object | Container that identifies the target object’s location (e.g., workbook name, worksheet name, chart index). Required for most operations. |

**OperateObjectPosition**

| Parameter Name | Type   | Description |
| -------------- | ------ | ----------- |
| Workbook       | object | The workbook that contains the target object. Must include either `FileName` (cloud storage) or `FileContent` (base‑64). |
| SheetName      | string | Name of the worksheet where the operation is applied. Required for worksheet‑level objects (charts, shapes, etc.). |
| ChartIndex     | integer| Zero‑based index of the chart within the worksheet (used when `OperateObjectType` is `Chart`). |
| ShapeIndex     | integer| Zero‑based index of the shape within the worksheet (used when `OperateObjectType` is `Shape`). |
| CellName       | string | A1‑style cell reference (e.g., `A1`). Used for cell‑level operations. |
| ListObjectIndex| integer| Zero‑based index of the list object (used when `OperateObjectType` is `ListObject`). |

**ChartOperateParameter**

| Parameter Name        | Type    | Description |
| --------------------- | ------- | ----------- |
| ChartIndex            | integer | Index of the chart to modify. Required when updating an existing chart. |
| ChartType             | string  | Type of chart to create (e.g., `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer | Row number of the chart’s upper‑left corner (zero‑based). |
| UpperLeftColumn       | integer | Column number of the chart’s upper‑left corner (zero‑based). |
| LowerRightRow         | integer | Row number of the chart’s lower‑right corner. |
| LowerRightColumn      | integer | Column number of the chart’s lower‑right corner. |
| Area                  | string  | Data range for the chart (e.g., `A1:B5`). |
| IsVertical            | string  | `true` if the chart orientation is vertical; otherwise `false`. |
| CategoryData          | string  | Range that provides category (X‑axis) labels. |
| IsAutoGetSerialName   | string  | `true` to automatically generate series names; `false` to use custom names. |
| Title                 | string  | Title text displayed on the chart. |

**ListObjectOperateParameter**

| Parameter Name | Type   | Description |
| -------------- | ------ | ----------- |
| ListObject     | object | Configuration object for a list (table) operation. Includes properties such as `ShowHeader`, `ShowTotal`, and `Style`. |

**PageBreakOperateParameter**

| Parameter Name | Type    | Description |
| -------------- | ------- | ----------- |
| PageBreakType  | string  | Type of page break (`Horizontal` or `Vertical`). |
| Index          | integer | Zero‑based index of the page break to delete or modify. |
| Row            | integer | Row number where a horizontal page break is placed. |
| Column         | integer | Column number where a vertical page break is placed. |
| StartIndex     | integer | Starting index for a range‑based page‑break operation. |
| EndIndex       | integer | Ending index for a range‑based page‑break operation. |

**PageSetupOperateParameter**

| Parameter Name | Type   | Description |
| -------------- | ------ | ----------- |
| PageSetup      | object | Settings for page layout (margins, orientation, paper size, etc.). |

**PivotTableOperateParameter**

| Parameter Name   | Type        | Description |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | Upper‑left cell of the destination range for the pivot table (e.g., `C5`). |
| SourceData       | string      | Source range for the pivot table (e.g., `A1:D100`). |
| TableName        | string      | Name assigned to the created pivot table. |
| UseSameSource    | string      | `true` to reuse an existing source range; `false` to create a new one. |
| PivotTableIndex  | integer     | Index of the pivot table to update (required for modify/delete actions). |
| PivotFieldRows   | integer[]   | Collection of field indexes that will appear in the rows area. |
| PivotFieldColumns| integer[]   | Collection of field indexes that will appear in the columns area. |
| PivotFieldData   | integer[]   | Collection of field indexes that will appear in the data area. |

**ShapeOperateParameter**

| Parameter Name | Type   | Description |
| -------------- | ------ | ----------- |
| Shape          | object | Definition of the shape (type, position, size, text, etc.). |

**WorkbookSettingsOperateParameter**

| Parameter Name   | Type   | Description |
| ---------------- | ------ | ----------- |
| WorkbookSettings | object | Settings that affect the whole workbook (e.g., calculation mode, precision). |

**WorksheetOperateParameter**

| Parameter Name | Type   | Description |
| -------------- | ------ | ----------- |
| Name           | string | Current name of the worksheet to be operated on. |
| SheetType      | string | Type of sheet (`Worksheet`, `Chart`, etc.). |
| NewName        | string | New name for the worksheet when renaming. |
| MovingRequest  | object | Parameters for moving a worksheet (e.g., `FromIndex`, `ToIndex`). |

## REST API

| API                | Type | Description | Resource Link |
| ------------------ | ---- | ----------- | ------------- |
| /cells/task/runtask| POST | Run Task    | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Prerequisites
- **Authentication** – Include a valid `Authorization: Bearer <access_token>` header.  
- **Storage** – The source workbook must be stored in Aspose Cloud Storage or supplied as base‑64‑encoded content in the request body.  
- **API Version** – This documentation targets **v3.0** of the Aspose.Cells Cloud API.

### Sample Request (cURL)

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

### Sample Response (Success – 200)

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

### Error Handling

| HTTP Status | Error Code | Description | Suggested Remedy |
| ----------- | ---------- | ----------- | ---------------- |
| 400         | InvalidParameter | One or more request parameters are missing or malformed. | Verify required fields and data types. |
| 401         | Unauthorized | Invalid or missing authentication token. | Refresh the access token and include it in the `Authorization` header. |
| 404         | NotFound | Specified workbook, worksheet, or object does not exist. | Check the `FileName`, `SheetName`, and object indexes. |
| 500         | ServerError | An unexpected error occurred on the server. | Retry the request; if the problem persists, contact support. |

### Common Use Cases
- **Add a new chart** to a worksheet.  
- **Rename a worksheet** (`OperateObjectType = "Worksheet"` with `WorksheetOperateParameter.NewName`).  
- **Insert a page break** (`OperateObjectType = "PageBreak"` with `PageBreakOperateParameter`).  
- **Update pivot‑table source data** (`OperateObjectType = "PivotTable"` with `PivotTableOperateParameter.SourceData`).  
- **Modify workbook settings** such as calculation mode (`OperateObjectType = "WorkbookSettings"`).  

---  

*All descriptions are derived from the official Aspose.Cells Cloud OpenAPI specification.*