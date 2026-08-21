---
title: "删除日期筛选器 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "删除日期筛选器"
type: docs
url: /zh/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, 删除日期筛选器, Excel 自动筛选, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 删除 Excel 工作表中的日期筛选器。内容包括 API 端点、参数、HTTPS cURL 示例、响应负载以及 SDK 代码示例。"
ArticleTitle: "删除日期筛选器 – Aspose.Cells Cloud API 文档"
---

此 REST API 用于删除 Excel 工作表中的日期筛选器。

**前提条件：** 确保您拥有有效的 JWT 令牌，工作簿已存储于 Aspose Cloud 存储中，并且您具备修改该工作表的相应权限。

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### 请求参数

| 参数名称             | 类型    | 位置   | 描述                                                                 |
|----------------------|---------|--------|----------------------------------------------------------------------|
| name                 | string  | 路径   | Excel 文件名称。                                                     |
| sheetName            | string  | 路径   | 工作表名称。                                                         |
| fieldIndex           | integer | 查询   | 应用筛选器的列的从零开始的索引。                                     |
| dateTimeGroupingType | string  | 查询   | 日期筛选器的分组类型（例如 Year、Month、Day）。                      |
| year                 | integer | 查询   | 筛选器的年份部分（默认值为 0）。                                     |
| month                | integer | 查询   | 筛选器的月份部分（默认值为 0）。                                     |
| day                  | integer | 查询   | 筛选器的日部分（默认值为 0）。                                       |
| hour                 | integer | 查询   | 筛选器的小时部分（默认值为 0）。                                     |
| minute               | integer | 查询   | 筛选器的分钟部分（默认值为 0）。                                     |
| second               | integer | 查询   | 筛选器的秒部分（默认值为 0）。                                       |
| folder               | string  | 查询   | 存储中文件所在的文件夹路径。                                         |
| storageName          | string  | 查询   | Aspose Cloud 存储的名称。                                            |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                         |
|--------|-------------------|----------------------------------------------|
| 200    | OK（成功）        | 筛选器已成功删除；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求体过大） | 上传文件超过大小限制。             |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。         |

API 返回标准 HTTP 状态码，指示删除操作的结果。

| 状态码 | 含义              | 描述                                         |
|--------|-------------------|----------------------------------------------|
| 200    | OK（成功）        | 日期筛选器已成功删除；响应包含操作状态。     |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求体过大） | 上传文件超过大小限制。             |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。         |

## 如何结合 SDK 使用 DeleteWorksheetDateFilter API

### DeleteWorksheetDateFilter API 规范

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器进行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
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

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能够专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}