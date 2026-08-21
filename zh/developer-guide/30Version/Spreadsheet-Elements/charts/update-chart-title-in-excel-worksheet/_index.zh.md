---
title: "更新 Excel 工作表中的图表标题"
type: docs
url: /zh/charts/title/update/
aliases: [/zh/update-chart-title-in-excel-worksheet/]
weight: 160
keywords: Excel, Aspose.Cells, REST API, 图表标题, 更新, 云 SDK
description: 了解如何使用 Aspose.Cells Cloud REST API、cURL 和 various SDK 更新 Excel 工作表中的图表标题。
ArticleTitle: "更新 Excel 工作表中的图表标题 – Aspose.Cells Cloud 文档"
---

此 REST API 用于更新图表标题。

**前提条件：** 您必须拥有有效的 Aspose Cloud 账户，并获取用于身份验证的 JWT 令牌。典型步骤包括：

- 注册 Aspose Cloud 账户。  
- 通过身份验证端点生成 JWT 令牌。  
- 确保目标工作簿存储在受支持的云存储中（默认或自定义存储）。

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

所有 API 调用必须通过 **HTTPS** 发起，以避免混合内容警告。

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型     | 位置   | 描述                       |
| ------------ | -------- | ------ | -------------------------- |
| name         | string   | path   | 工作簿名称。               |
| sheetName    | string   | path   | 工作表名称。               |
| chartIndex   | integer  | path   | 图表的从零开始的索引。     |
| title        | string   | body   | 新的图表标题。             |
| folder       | string   | query  | 工作簿所在文件夹。         |
| storageName  | string   | query  | 存储名称。                 |

### 响应状态码

| 状态码 | 描述                                           |
| ------ | ---------------------------------------------- |
| 200    | 成功 – 图表标题已成功更新。                    |
| 400    | 请求错误 – 缺少或参数无效。                    |
| 401    | 未授权 – JWT 令牌无效或缺失。                  |
| 404    | 未找到 – 未找到工作簿、工作表或图表。          |
| 500    | 服务器内部错误 – 出现意外的服务器状态。        |

**注意：** `chartIndex` 为从零开始的索引；工作表上的第一个图表通过 `0` 引用。

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Stock exchange"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}