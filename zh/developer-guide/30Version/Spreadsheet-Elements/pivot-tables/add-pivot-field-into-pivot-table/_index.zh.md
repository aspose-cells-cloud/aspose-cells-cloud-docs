---
title: "向数据透视表添加数据透视字段"
second_title: "Document"
linktitle: "添加数据透视字段"
type: docs
url: /zh/pivot-tables/add-pivot-field/
aliases: [  /zh/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 数据透视表, 添加数据透视字段, REST API, SDK"
description: "使用 Aspose.Cells Cloud REST API 向现有数据透视表添加数据透视字段。包含请求详情、cURL 示例和 SDK 代码片段。"
weight: 40
ArticleTitle: "向数据透视表添加数据透视字段 – Aspose.Cells Cloud 文档"
---

此 REST API **添加**一个数据透视字段到现有的数据透视表中。

> **前提条件：** 调用此接口前，您必须在 `Authorization` 请求头中包含有效的 JWT 认证令牌，并确保工作簿存储在指定文件夹或默认存储中。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### 请求参数

| 参数名称         | 类型     | 位置   | 描述                                           |
| ---------------- | -------- | ------ | ---------------------------------------------- |
| name             | string   | path   | 文档名称。                                     |
| sheetName        | string   | path   | 工作表名称。                                   |
| pivotTableIndex  | integer  | path   | 数据透视表的索引。                             |
| pivotFieldType   | string   | query  | 字段区域类型（例如：Row、Column）。            |
| request          | object   | body   | 包含待添加字段索引的 DTO 对象。                |
| needReCalculate  | boolean  | query  | 设置为 **true** 以在操作后重新计算数据透视表。 |
| folder           | string   | query  | 文档所在的文件夹。                             |
| storageName      | string   | query  | 存储名称。                                     |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具调用 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 添加数据透视字段。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

成功响应将返回一个包含 `Code` 和 `Status` 字段的 JSON 对象。示例结构如下：

```json
{
  "Code": 0,        // 整数，表示 HTTP 状态码
  "Status": "OK"    // 字符串，表示状态消息
}
```

可能的错误响应包括：**400 Bad Request**（缺少必要参数）、**401 Unauthorized**（令牌无效）以及 **500 Internal Server Error**（服务器端问题）。

## 云 SDK 家族

使用 SDK 是集成此功能的最快方式。SDK 封装了底层细节，使您能够专注于业务逻辑。有关 Aspose.Cells Cloud SDK 的完整列表，请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例演示如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅：**  
- [添加数据透视表](https://docs.aspose.cloud/cells/zh/pivot-tables/add-pivot-table/)  
- [删除数据透视字段](https://docs.aspose.cloud/cells/zh/pivot-tables/delete-pivot-field/)