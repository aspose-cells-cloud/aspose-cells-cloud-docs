---
title: "从工作表中删除所有图表"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, 云, 删除, 所有图表, 工作表, REST API, DELETE, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）删除工作表中的所有图表。内容包括端点、参数、cURL 示例、SDK 代码片段、认证步骤和错误处理。"
ArticleTitle: "使用 Aspose.Cells Cloud API 从工作表中删除所有图表"
---

此 REST API 用于删除指定工作表中的所有图表。

**背景说明** – 在需要重置工作表的视觉布局、替换过时的可视化图表，或在不保留先前图表数据的前提下为工作簿重复使用做准备时，删除工作表中的所有图表非常有用。

在调用 API 之前，请确保满足以下先决条件：

- 已获取有效的 JWT 令牌用于身份验证。  
- 工作簿文件存在于指定的存储位置及文件夹中。  
- 您正在使用 API 的 **v3.0** 版本。

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **安全与认证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 位置 | 描述                     |
|------------|------|------|--------------------------|
| name       | string | path | 工作簿文件名。           |
| sheetName  | string | path | 工作表名称。             |
| folder     | string | query| 工作簿所在的文件夹。     |
| storageName| string | query| 存储名称。               |

**请求头**

| 请求头          | 描述                     |
|----------------|--------------------------|
| Authorization  | Bearer `<jwt token>`     |
| Accept         | `application/json`       |
| Content-Type   | `application/json`（无请求体）|

**请求体**

DELETE 操作**不需要**请求体。

**响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义                | 描述                                   |
|-------|---------------------|----------------------------------------|
| 200   | OK（成功）          | 成功应用筛选条件；响应包含操作详情。     |
| 400   | Bad Request（错误请求）| 缺失或无效的参数（例如：不支持的文件类型）。 |
| 401   | Unauthorized（未授权） | JWT 令牌无效或缺失。                    |
| 413   | Payload Too Large（请求体过大）| 上传的文件超过大小限制。              |
| 500   | Internal Server Error（服务器内部错误）| 服务器发生意外错误。             |

*示例错误响应*

```json
// 400 Bad Request（错误请求）
{
    "Code": 400,
    "Message": "Invalid parameter: 'sheetName' is required."
}

// 401 Unauthorized（未授权）
{
    "Code": 401,
    "Message": "Authentication failed. Invalid JWT token."
}

// 413 Payload Too Large（请求体过大）
{
    "Code": 413,
    "Message": "The request payload exceeds the maximum allowed size."
}

// 500 Internal Server Error（服务器内部错误）
{
    "Code": 500,
    "Message": "An unexpected error occurred on the server."
}
```

## 如何使用 SDK 调用 DeleteWorksheetClearCharts API

### DeleteWorksheetClearCharts API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
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

### 使用 Aspose.Cells Cloud SDK

当您需要**删除工作表中的所有图表**时，使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---