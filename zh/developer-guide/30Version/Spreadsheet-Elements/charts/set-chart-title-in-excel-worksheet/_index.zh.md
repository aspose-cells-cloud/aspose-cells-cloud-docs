---
title: "Aspose.Cells Cloud API – 在 Excel 工作表中设置图表标题"
type: docs
url: /zh/chart/title/add/
aliases: [/zh/set-chart-title-in-excel-worksheet/]
weight: 30
keywords: "Aspose.Cells Cloud, 图表标题 API, Excel 图表标题, REST API, SDK 示例"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表中添加或更新图表标题。包含 cURL、SDK 示例、所需参数、身份验证步骤和错误处理。"
---

添加图表标题或使现有标题可见。

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名        | 类型     | 位置   | 描述                         |
| ------------- | -------- | ------ | ---------------------------- |
| name          | string   | path   | 工作簿名称。                 |
| sheetName     | string   | path   | 工作表名称。                 |
| chartIndex    | integer  | path   | 图表索引。                   |
| title         | string   | body   | 图表标题文本。               |
| folder        | string   | query  | 包含工作簿的文件夹。         |
| storageName   | string   | query  | 存储名称。                   |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
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

**错误响应**

| HTTP 状态码 | 示例载荷                                                                            | 描述                               |
| ----------- | ----------------------------------------------------------------------------------- | ---------------------------------- |
| 400         | `{ "Code": "400", "Message": "Invalid request payload." }`                         | 请求体格式错误或缺少必需字段。     |
| 401         | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | 承载令牌缺失、无效或已过期。       |
| 404         | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`          | 指定的资源不存在。                 |
| 500         | `{ "Code": "500", "Message": "Internal server error." }`                            | 服务器上发生意外错误。             |

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 抽象了底层细节，使您能够专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}

---