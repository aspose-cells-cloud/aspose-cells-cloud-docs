---
title: "删除 Excel 工作表中的筛选器 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "删除筛选器"
type: docs
url: /zh/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud 删除筛选器, Excel, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API、cURL 以及 SDK（C#、Java、Python 等）删除 Excel 工作表中的自动筛选器。包含端点、参数、身份验证及示例代码。"
weight: 100
---

## REST API

此 REST API 用于删除 Excel 工作表中的**自动筛选器（AutoFilter）**。

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名                 | 类型    | 位置   | 是否必需？ | 描述                                                                                   |
| ---------------------- | ------- | ------ | ---------- | -------------------------------------------------------------------------------------- |
| **name**               | string  | 路径   | 是         | 工作簿名称。                                                                           |
| **sheetName**          | string  | 路径   | 是         | 工作表名称。                                                                           |
| **range**              | string  | 查询   | 否         | 筛选器适用的单元格范围（例如 `A1:C10`）。                                               |
| **fieldIndex**         | integer | 查询   | 是         | 筛选器所应用列的从零开始索引。                                                          |
| **dateTimeGroupingType** | string | 查询 | 否         | 日期/时间值的分组方式：`Day`（日）、`Hour`（小时）、`Minute`（分钟）、`Month`（月）、`Second`（秒）或 `Year`（年）。 |
| **year**               | integer | 查询   | 否         | 日期分组中的年份部分。                                                                 |
| **month**              | integer | 查询   | 否         | 日期分组中的月份部分。                                                                 |
| **day**                | integer | 查询   | 否         | 日期分组中的日期部分。                                                                 |
| **hour**               | integer | 查询   | 否         | 日期分组中的小时部分。                                                                 |
| **minute**             | integer | 查询   | 否         | 日期分组中的分钟部分。                                                                 |
| **second**             | integer | 查询   | 否         | 日期分组中的秒数部分。                                                                 |
| **matchBlanks**        | boolean | 查询   | 否         | `true` / `false` — 是否在筛选中包含空白单元格。                                        |
| **refresh**            | boolean | 查询   | 否         | `true` / `false` — 删除后是否刷新工作表。                                              |
| **folder**             | string  | 查询   | 否         | 原始工作簿所在文件夹。                                                                 |
| **storageName**        | string  | 查询   | 否         | 存储名称。                                                                             |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 筛选器删除成功；响应包含操作详情。              |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。      |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                          |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                     |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                      |

## 如何使用 DeleteWorksheetFilter API（配合 SDK）

### DeleteWorksheetFilter API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

使用 SDK 是加快开发效率的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}