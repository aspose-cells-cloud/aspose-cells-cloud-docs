---
title: "向 Excel 工作表添加日期筛选器"
second_title: "文档"
linktitle: "添加日期筛选器"
type: docs
url: /autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）向 Excel 工作表添加日期筛选器。包含 cURL 示例、SDK 代码片段（C#、Java、Python 等）、参数说明及错误处理。"
weight: 65
ArticleTitle: "向 Excel 工作表添加日期筛选器 | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel 日期筛选器, AutoFilter API, REST API, 云 SDK, cURL, 电子表格自动化"
---

此 REST API 可向 Excel 工作表添加**日期筛选器**。

**前提条件**：您必须拥有有效的 JWT 令牌，且目标工作簿已存在于指定存储位置。该请求不需要 JSON 请求体。

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数


| 参数名称                 | 类型    | 位置   | 描述                                                                                                                                                                     |
| ------------------------ | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**                 | string  | 路径   | 工作簿名称。                                                                                                                                                             |
| **sheetName**            | string  | 路径   | 工作表名称。                                                                                                                                                             |
| **range**                | string  | 查询参数 | 应用筛选器的 Excel 区域（例如 `A1:B1`）。                                                                                                                                |
| **fieldIndex**           | integer | 查询参数 | 要筛选的列的从零开始索引。                                                                                                                                               |
| **dateTimeGroupingType** | string  | 查询参数 | 日期/时间筛选器的分组类型。允许值为 `Day`、`Hour`、`Minute`、`Month`、`Second`、`Year`。值区分大小写，默认为 `Day`。                                                      |
| **year**                 | integer | 查询参数 | 筛选值的年份部分。                                                                                                                                                       |
| **month**                | integer | 查询参数 | 筛选值的月份部分。                                                                                                                                                       |
| **day**                  | integer | 查询参数 | 筛选值的日期部分。                                                                                                                                                       |
| **hour**                 | integer | 查询参数 | 筛选值的小时部分。                                                                                                                                                       |
| **minute**               | integer | 查询参数 | 筛选值的分钟部分。                                                                                                                                                       |
| **second**               | integer | 查询参数 | 筛选值的秒数部分。                                                                                                                                                       |
| **matchBlanks**          | boolean | 查询参数 | 是否包含空白单元格（`true` 或 `false`）。                                                                                                                                |
| **refresh**              | boolean | 查询参数 | 应用筛选后是否刷新筛选器（`true` 或 `false`）。                                                                                                                          |
| **folder**               | string  | 查询参数 | 原始工作簿所在的文件夹路径。                                                                                                                                             |
| **storageName**          | string  | 查询参数 | 存储服务的名称。                                                                                                                                                         |

*PUT 请求不需要请求体；所有参数均通过查询字符串传递。*

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义            | 描述                                           |
|--------|-----------------|------------------------------------------------|
| 200    | OK（成功）      | 筛选器成功应用；响应包含操作详细信息。          |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                            |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                          |

## 如何结合 SDK 使用 PutWorksheetDateFilter API

### PutWorksheetDateFilter API 规范

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，使您能直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}



### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}