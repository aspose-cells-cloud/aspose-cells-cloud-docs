---
title: "删除 Excel 工作表中的数据透视表"
second_title: "文档"
linktitle: 删除
type: docs
url: /zh/pivot-tables/delete/
aliases: [  /zh/delete-worksheet-pivot-table-by-index/ ]
keywords: "Aspose.Cells, 数据透视表, 删除, Excel, REST API"
description: "使用 Aspose.Cells Cloud REST API（v3.0）从 Excel 工作表中删除数据透视表。包含请求格式、cURL 示例、错误代码以及 C#、Java、Python、Node.js 的 SDK 代码片段。"
weight: 70
ArticleTitle: "如何使用 Aspose.Cells Cloud 删除 Excel 工作表中的数据透视表"
---

此 REST API 可按索引从工作表中删除数据透视表。

**前提条件** – 您需拥有有效的 Aspose.Cells Cloud JWT 访问令牌，并且目标 Excel 文件已存储在受支持的存储位置中。调用 API 前，请确保文件名、工作表名称及存储信息均已正确指定。

数据透视表是**Excel 工作表**中汇总数据的强大工具。借助 Aspose.Cells Cloud，您只需发送一条 HTTP DELETE 请求，即可程序化地删除不需要的数据透视表。该操作非常适合清理工作表、自动化报表生成，或将 Excel 处理功能集成到您的应用程序中。

## DeleteWorksheetPivotTable API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名            | 类型     | 位置   | 描述                                       |
| ----------------- | -------- | ------ | ------------------------------------------ |
| name              | string   | path   | Excel 文档的名称。                         |
| sheetName         | string   | path   | 包含目标数据透视表的工作表名称。           |
| pivotTableIndex   | integer  | path   | 待删除数据透视表的从零开始的索引。         |
| folder            | string   | query  | 文档所在文件夹的路径。                     |
| storageName       | string   | query  | 存储服务的名称。                           |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 调用。

您可使用 **cURL 命令行工具**轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**响应示例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

响应遵循简洁的 JSON 结构：

```json
{
  "Code": integer,   // 操作的类 HTTP 状态码
  "Status": string   // 文本描述，例如 "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 错误处理

常见响应状态码如下：

| HTTP 状态码 | 描述                                       |
| ----------- | ------------------------------------------ |
| 400         | 请求错误 — 缺少或无效参数。                |
| 401         | 未授权 — 无效或缺失 JWT 令牌。             |
| 404         | 未找到 — 文件、工作表或数据透视表不存在。  |
| 500         | 服务器内部错误 — 服务器发生意外情况。      |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---