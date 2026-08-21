---
title: "从工作表中删除图表"
type: docs
url: /zh/charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "删除图表"
  - "工作表"
  - "Excel"
  - "云 SDK"
  - "图表删除"
  - "API 参考"
description: "使用 Aspose.Cells Cloud REST API 按其从零开始的索引从工作表中删除图表。"
ArticleTitle: "使用 Aspose.Cells Cloud REST API 从工作表中删除图表"
---

此 REST API 根据索引删除工作表中的图表。

有关相关操作，请参阅 **[添加图表](#)** 和 **[获取图表](#)** 页面。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### 安全与认证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的认证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称     | 类型    | 位置 | 描述                               |
| ------------ | ------- | ---- | ---------------------------------- |
| name         | string  | path | 工作簿名称。                       |
| sheetName    | string  | path | 工作表名称。                       |
| chartIndex   | integer | path | 要删除的图表的从零开始的索引。     |
| folder       | string  | query | 包含工作簿的文件夹。              |
| storageName  | string  | query | 要使用的存储名称。                |


### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义         | 描述                                               |
|--------|--------------|----------------------------------------------------|
| 200    | OK（成功）   | 成功应用筛选；响应包含操作详情。                   |
| 400    | 请求错误     | 缺少或无效的参数（例如，不支持的文件类型）。       |
| 401    | 未授权       | JWT 令牌无效或缺失。                               |
| 413    | 负载过大     | 上传的文件超出大小限制。                           |
| 500    | 服务器内部错误 | 服务器发生意外错误。                               |

## 如何使用 PutWorksheetAddChart API（SDK）

### PutWorksheetAddChart API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器中执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

API 返回以下状态码：

| 状态码 | 描述                             |
|--------|----------------------------------|
| 200    | 成功删除图表                     |
| 400    | 请求错误（例如，索引无效）       |
| 401    | 未授权（缺少或无效的 JWT 令牌）  |
| 404    | 工作簿、工作表或图表未找到       |
| 500    | 服务器错误                       |

**错误处理：** 有关详细错误信息，请参阅 OpenAPI 规范中的通用错误模型。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 抽象了底层细节，让您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}