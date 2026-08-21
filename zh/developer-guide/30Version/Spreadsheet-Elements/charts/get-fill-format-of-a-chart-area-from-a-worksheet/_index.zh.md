---
title: "获取图表区域填充格式 – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /zh/charts/chart-area/fill-format/get/
aliases: [  /zh/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Chart Area"
  - "Fill Format"
  - "REST API"
  - "Excel"
description: "通过 Aspose.Cells Cloud API 获取 Excel 工作表中图表区域的填充格式（颜色、图案、渐变）。包含 cURL 示例、SDK 代码片段、认证步骤和响应详情。"
ArticleTitle: "获取图表区域填充格式 Aspose.Cells Cloud API v3.0"
---

本 REST API 用于获取**图表区域**的填充格式信息。

**前置条件**  
调用此接口前，您必须持有有效的 OAuth/JWT 访问令牌。请使用 Aspose.Cells Cloud 的认证流程获取令牌，并在 `Authorization` 请求头中以 `Bearer <jwt token>` 格式提供。若您使用的是 SDK，请在调用方法前确保 SDK 已配置好您的 `client_id` 和 `client_secret`。

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### 请求参数

| 参数名称     | 类型   | 位置   | 描述                         |
| ------------ | ------ | ------ | ---------------------------- |
| name         | string | path   | 工作簿名称。                 |
| sheetName    | string | path   | 工作表名称。                 |
| chartIndex   | integer| path   | 图表索引。                   |
| folder       | string | query  | 包含工作簿的文件夹路径。     |
| storageName  | string | query  | 存储空间名称。               |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具访问 Aspose.Cells Web 服务。下方示例展示了如何通过 cURL 调用此 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**说明**  
- 成功调用返回 HTTP 200 状态码，并附带填充格式详情。  
- HTTP 401 表示认证失败（令牌无效或缺失）。  
- HTTP 404 表示指定的工作簿、工作表或图表索引不存在。  
- HTTP 500 表示服务端错误；若问题持续存在，请重试请求或联系技术支持。

| 状态码 | 含义                                       |
|--------|--------------------------------------------|
| 200    | 成功 — 返回填充格式信息                    |
| 401    | 未授权 — 令牌无效或缺失                    |
| 404    | 未找到 — 工作簿、工作表或图表不存在        |
| 500    | 服务器内部错误                             |

相关操作请参见 **Get Chart Area Border**（获取图表区域边框）和 **Get Chart Title**（获取图表标题）接口。

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是加速开发进程的最佳方式。SDK 封装了底层细节，让您能专注于业务逻辑开发。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}