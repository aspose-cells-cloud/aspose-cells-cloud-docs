---
title: "获取 Excel 工作表中的所有数据透视表"
second_title: "文档"
linktitle: 获取全部
type: docs
url: /pivot-tables/get-all/
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "获取所有数据透视表, Aspose.Cells Cloud API, Excel 数据透视表, REST API"
description: "通过 Aspose.Cells Cloud API 从 Excel 工作表中检索所有数据透视表。包含 PivotTables API 的端点、参数、认证步骤、cURL 示例和 SDK 示例。"
weight: 20
ArticleTitle: "获取 Excel 工作表中的所有数据透视表 – Aspose.Cells Cloud API"
---

**数据透视表（PivotTable）** 是 Excel 中用于汇总、分析、探索和呈现数据的工具，可帮助您重新组织大型数据集并进行深入分析。此 REST API 可检索指定工作表中**所有**数据透视表的信息。

## 安全与认证

Aspose.Cells Cloud API 是安全的，需要采用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **请求参数**

| 参数名        | 类型   | 位置   | 描述                           |
| ------------- | ------ | ------ | ------------------------------ |
| name          | string | path   | Excel 文档的名称。             |
| sheetName     | string | path   | 工作表的名称。                 |
| folder        | string | query  | 存放文档的文件夹。             |
| storageName   | string | query  | 存储服务的名称。               |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) 定义了一个公开可访问的编程接口，让您能够直接从网页浏览器发起 REST 请求。

### 请求

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### 响应

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 错误响应

| HTTP 状态码 | 描述                                     | 示例 JSON 负载                                       |
| ----------- | ---------------------------------------- | ---------------------------------------------------- |
| 400         | 请求错误 – 缺少必需参数。               | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401         | 未授权 – 令牌无效或缺失。               | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | 未找到 – 工作簿、工作表或数据透视表不存在。 | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | 服务器内部错误 – 服务器上发生意外情况。 | `{ "Code": "500", "Message": "Server error." }`               |

## 云 SDK 开发套件

使用 SDK 是最快捷的开发方式。SDK 将处理底层细节，让您专注于项目本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}