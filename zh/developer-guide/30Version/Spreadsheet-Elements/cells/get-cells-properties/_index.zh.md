---
title: "获取单元格属性"
type: docs
url: /get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, 工作表, 单元格属性, 获取单元格属性"
description: "了解如何使用 Aspose.Cells Cloud REST API 获取 Excel 工作表中特定单元格的属性或预定义单元格方法。"
---

此 REST API 演示了如何获取 Excel 文件中的特定单元格。

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## 安全与身份验证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数


| 参数名称             | 类型   | 位置 | 描述                                                                                                                                                                        |
| -------------------- | ------ | ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | string | path | Excel 文档的名称。                                                                                                                                                          |
| **sheetName**        | string | path | 包含目标单元格的工作表名称。                                                                                                                                                |
| **cellOrMethodName** | string | path | 单元格名称或预定义方法名称（例如 `firstcell`、`endcell`、`maxrow`、`maxdatarow`、`maxcolumn`、`maxdatacolumn`、`minrow`、`mindatarow`、`mincolumn`、`mindatacolumn`）。 |
| **folder**           | string | query | 存放文档的文件夹。                                                                                                                                                          |
| **storageName**      | string | query | 存储服务的名称。                                                                                                                                                            |

## **响应**

返回 CellResponse。

- **响应字段概览**

| 字段            | 类型    | 描述                                               |
| --------------- | ------- | -------------------------------------------------- |
| `Name`          | string  | 单元格地址（例如 `F341`）。                        |
| `Row`           | integer | 以 0 为起始的行索引。                              |
| `Column`        | integer | 以 0 为起始的列索引。                              |
| `Value`         | string  | 单元格显示的值。                                   |
| `Type`          | string  | 单元格的数据类型（例如 `IsString`）。             |
| `Formula`       | string  | 若单元格包含公式，则为公式文本。                   |
| `IsFormula`     | bool    | 指示单元格是否包含公式。                           |
| `IsMerged`      | bool    | 指示单元格是否属于合并区域。                       |
| `IsArrayHeader` | bool    | 指示单元格是否为数组标题。                         |
| `IsInArray`     | bool    | 指示单元格是否属于数组。                           |
| `IsErrorValue`  | bool    | 指示单元格是否包含错误值。                         |
| `IsInTable`     | bool    | 指示单元格是否位于表格内。                         |
| `IsStyleSet`    | bool    | 指示单元格是否已应用样式。                         |
| `HtmlString`    | string  | 单元格值的 HTML 编码表示形式。                     |
| `Style.link`    | object  | 样式资源的超链接。                                 |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
|------|------------------|--------------------------------------------|
| 200  | OK（成功）       | 成功应用筛选器；响应包含操作详情。          |
| 400  | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401  | Unauthorized（未授权）  | JWT 令牌无效或缺失。                        |
| 413  | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。             |
| 500  | Internal Server Error（内部服务器错误） | 服务器内部发生意外错误。         |

## 如何使用 GetWorksheetCell API 与 SDK

### GetWorksheetCell API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。
{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最高效方式。SDK 抽象了底层细节，使您能够专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 如何获取特定单元格

- [从工作表获取单元格数据](/cells/get-cell-data-from-a-worksheet/)
- [从 Excel 工作表获取第一个单元格](/cells/get-first-cell-from-excel-worksheet/)
- [获取 Excel 工作表的最后一个单元格](/cells/get-last-cell-of-excel-worksheet/)
- [从 Excel 工作表获取 MaxRow](/cells/get-maxrow-from-excel-worksheet/)
- [从 Excel 工作表获取 MaxDataRow](/cells/get-maxdatarow-from-excel-worksheet/)
- [从 Excel 工作表获取 MaxColumn](/cells/get-maxcolumn-from-excel-worksheet/)
- [从 Excel 工作表获取 MaxDataColumn](/cells/get-maxdatacolumn-from-excel-worksheet/)
- [从 Excel 工作表获取 MinRow](/cells/get-minrow-from-excel-worksheet/)
- [从 Excel 工作表获取 MinDataRow](/cells/get-mindatarow-from-excel-worksheet/)
- [从 Excel 工作表获取 MinColumn](/cells/get-mincolumn-from-excel-worksheet/)
- [从 Excel 工作表获取 MinDataColumn](/cells/get-mindatacolumn-from-excel-worksheet/)