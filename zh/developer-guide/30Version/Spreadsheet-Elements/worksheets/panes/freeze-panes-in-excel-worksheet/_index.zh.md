---
title: "冻结 Excel 工作表中的窗格"
second_title: "文档"
linktitle: "冻结"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, 冻结窗格, Excel, REST API, 工作表"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表中冻结行和列。内容包括端点语法、必需参数、cURL 示例、身份验证指南、错误响应详情，以及多种编程语言的 SDK 代码示例。"
weight: 190
---

此 REST API **设置** Excel 工作表中的冻结窗格。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

请求参数如下：

| 参数名称       | 类型    | 位置   | 描述                                   |
| -------------- | ------- | ------ | -------------------------------------- |
| name           | string  | path   | 工作簿文件的名称。                     |
| sheetName      | string  | path   | 要冻结窗格的工作表名称。               |
| row            | integer | query  | 首个**未冻结**行的从零开始的索引。     |
| column         | integer | query  | 首个**未冻结**列的从零开始的索引。     |
| frozenRows     | integer | query  | 从顶部开始要冻结的行数。               |
| frozenColumns  | integer | query  | 从左侧开始要冻结的列数。               |
| folder         | string  | query  | 存储中工作簿所在的文件夹路径。         |
| storageName    | string  | query  | 存储服务的名称。                       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### 错误响应

| HTTP 状态码               | 代码 | 消息                        | 示例                                                       |
| ------------------------- | ---- | --------------------------- | ---------------------------------------------------------- |
| 400 Bad Request           | 400  | 参数无效                    | `{ "Code": 400, "Message": "Invalid frozenRows value" }`  |
| 401 Unauthorized          | 401  | 缺失或无效的 JWT 令牌       | `{ "Code": 401, "Message": "Invalid access token" }`      |
| 404 Not Found             | 404  | 工作簿或工作表未找到        | `{ "Code": 404, "Message": "File not found" }`            |
| 500 Internal Server Error | 500  | 意外服务器错误              | `{ "Code": 500, "Message": "Internal server error" }`     |

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}