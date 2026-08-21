---
title: "获取图表第二值轴"
type: docs
url: /zh/charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, 图表第二值轴, Excel, REST API, 云服务, API, Excel 图表轴
description: 使用 Aspose.Cells Cloud REST API 获取 Excel 工作表中指定图表的第二值轴。
ArticleTitle: "获取图表第二值轴 – Aspose.Cells Cloud API"
---

此 REST API 用于获取图表的第二值轴。

## GetChartSecondValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **安全与认证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### 请求参数

| 参数名称       | 类型    | 位置   | 描述                               |
| -------------- | ------- | ------ | ---------------------------------- |
| name           | string  | path   | Excel 文件的名称。                 |
| sheetName      | string  | path   | 包含图表的工作表名称。             |
| chartIndex     | integer | path   | 图表的从零开始的索引。             |
| folder         | string  | query  | 文件所在的文件夹。                 |
| storageName    | string  | query  | Aspose Cloud 存储空间的名称。      |

**前置条件**：每个请求的 `Authorization` 请求头中必须提供通过 Aspose Cloud OAuth2 流程获取的有效 JWT 访问令牌。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。所有 Aspose Cloud 端点均需使用 HTTPS 协议。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "第二值轴"
  }
}
```

**响应字段说明**

- **Code** – 操作的 HTTP 状态码（例如：`200` 表示成功）。  
- **Status** – 状态的文本描述（`"OK"` 表示成功）。  
- **Axis** – 包含第二值轴详细信息的对象：  
  - **AxisId** – 轴的标识符。  
  - **IsVisible** – 布尔值，指示该轴是否显示。  
  - **MinimumScale** – 轴上显示的最小值。  
  - **MaximumScale** – 轴上显示的最大值。  
  - **MajorUnit** – 主刻度线之间的间隔。  
  - **MinorUnit** – 次刻度线之间的间隔。  
  - **Title** – 轴的标题文本。

**错误响应（非 200 状态码）**

- `400 Bad Request` – 参数无效或请求格式错误。  
- `401 Unauthorized` – 缺少或无效的 JWT 令牌。  
- `404 Not Found` – 指定的文件、工作表或图表不存在。  
- `500 Internal Server Error` – 服务器内部意外错误。

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包系列

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能够专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 代码仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl 示例占位符 -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go 示例占位符 -->

{{< /tab >}}

{{< /tabs >}}
---