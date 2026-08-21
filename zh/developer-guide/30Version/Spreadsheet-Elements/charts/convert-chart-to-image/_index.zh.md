---
title: "将 Excel 图表转换为图像 – Aspose.Cells Cloud REST API"
type: docs
url: /zh/charts/to-image/
aliases: [  /zh/convert-charts-to-image/ ]
weight: 50
keywords: "Aspose.Cells Cloud, 图表转图像, Excel 图表转换, REST API, 图像格式, PNG, JPEG, BMP, TIFF, GIF"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel 图表对象转换为 PNG、JPEG、BMP、TIFF 或 GIF 图像。内容包括端点详情、参数说明、cURL 示例、SDK 代码片段、响应示例及错误处理。"
ArticleTitle: "将 Excel 图表转换为图像 – Aspose.Cells Cloud REST API"
---

本 REST API 演示如何使用 **Aspose.Cells Cloud** 将 **Excel 图表** 转换为图像。

## PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

支持的图像格式包括 `png`、`jpeg`、`bmp`、`tiff` 和 `gif`。

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名         | 类型     | 位置   | 描述                 |
| -------------- | -------- | ------ | -------------------- |
| name           | string   | path   | 文档名称。           |
| sheetName      | string   | path   | 工作表名称。         |
| chartNumber    | integer  | path   | 图表编号。           |
| format         | string   | query  | 导出的文件格式。     |
| folder         | string   | query  | 文档所在文件夹。     |
| storageName    | string   | query  | 存储空间名称。       |

### **响应说明**

该端点将以二进制流（例如 `byte[]`）形式返回所请求格式的图像文件。响应头 `Content-Type` 与所选图像格式一致，例如 `image/png`、`image/jpeg` 等。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 过滤操作成功执行；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（负载过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                           |

## 如何结合 SDK 使用 PutWorksheetAddChart API

### PutWorksheetAddChart API 规范

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，使您能够直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能够专注于项目核心任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

示例即将推出。

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}
---