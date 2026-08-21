---
title: "将表格转换为数据透视表"
second_title: "文档"
linktitle: 转换
type: docs
url: /zh/pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/zh/create-a-pivottable-with-table/",
    "/zh/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "数据透视表, 列表对象, Aspose.Cells Cloud, REST API, 将表格转换为数据透视表"
description: "了解如何使用 Aspose.Cells Cloud REST API 从列表对象创建数据透视表。包含请求详情、cURL 示例和 SDK 引用。"
weight: 60
ArticleTitle: "将表格转换为数据透视表 – Aspose.Cells Cloud 文档"
---

此 REST API 可从列表对象创建**数据透视表**。

数据透视表可汇总列表对象中的数据，让您直接在工作簿内分析和报告大型数据集。

**先决条件：**  
- 用于身份验证的有效 JWT bearer token。  
- 工作簿必须存在于指定的存储位置。  
- 目标工作表必须包含您要汇总的列表对象。

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT token 的身份验证</a>。

### **请求参数**

| 参数名称         | 类型     | 位置   | 描述                               |
| ---------------- | -------- | ------ | ---------------------------------- |
| name             | string   | path   | 工作簿文件名。                     |
| sheetName        | string   | path   | 包含列表对象的工作表。             |
| listObjectIndex  | integer  | path   | 工作表中列表对象的索引。           |
| destsheetName    | string   | query  | 目标工作表的名称。                 |
| request          | object   | body   | 定义数据透视表的 JSON 负载。       |
| folder           | string   | query  | 工作簿所在文件夹的路径。           |
| storageName      | string   | query  | 存储空间的名称。                   |

请求体必须遵循以下 JSON Schema 定义：

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "新数据透视表的名称。" },
    "DestCellName": { "type": "string", "description": "数据透视表左上角单元格（例如 \"C1\"）。" },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "要放入行的字段的从零开始的索引。"
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "要放入列的字段的从零开始的索引。"
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "用作数据字段的字段的从零开始的索引。"
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*注意：生产环境请使用生产端点（`api.aspose.cloud`）。QA 端点（`api-qa.aspose.cloud`）仅用于测试。所有生产调用必须使用 HTTPS。*

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

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
| ------ | ---------------- | ------------------------------------------ |
| 200    | OK（成功）       | 筛选器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失的 JWT token。                   |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                  |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。                   |

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：
---