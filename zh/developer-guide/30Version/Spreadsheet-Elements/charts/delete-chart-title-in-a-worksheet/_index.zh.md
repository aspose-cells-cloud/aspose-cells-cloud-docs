---
title: "删除工作表中的图表标题"
type: docs
url: /zh/zh-cn/charts/delete-chart-title/
aliases: [  /zh/delete-chart-title-in-a-worksheet/ ]
weight: 150
keywords: "Aspose.Cells, 云 API, 删除图表标题, Excel, REST, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v4.0）删除 Excel 工作表中的图表标题。包含 cURL、SDK 示例及错误处理。"
---

此 REST API 用于删除图表的标题。

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### 安全与身份验证

Aspose.Cells Cloud API 安全可靠，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称     | 类型     | 位置   | 描述                       |
| ------------ | -------- | ------ | -------------------------- |
| name         | string   | path   | 工作簿文件名。             |
| sheetName    | string   | path   | 工作表名称。               |
| chartIndex   | integer  | path   | 图表的从零开始的索引。     |
| folder       | string   | query  | 包含工作簿的文件夹。       |
| storageName  | string   | query  | 存储名称。                 |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                     |
| ------ | ---------------- | ---------------------------------------- |
| 200    | OK（成功）       | 成功应用筛选器；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                     |

## 如何使用 SDK 调用 DeleteWorksheetChartTitle API

### DeleteWorksheetChartTitle API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何发起调用，包括用于身份验证所需的 **Bearer JWT** 令牌。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
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

使用 SDK 是加速开发的最佳方式。SDK 可处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}