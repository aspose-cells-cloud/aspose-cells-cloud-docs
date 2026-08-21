---
title: "获取图表值轴"
type: docs
url: /zh/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, 图表值轴, REST API, Excel, 云 SDK, 获取图表值轴
description: "Aspose.Cells Cloud REST API - 从 Excel 工作表中检索图表的值轴。"
ArticleTitle: "获取图表值轴 - Aspose.Cells Cloud REST API"
---

此 REST API 用于获取图表的值轴。该 API 属于 **Aspose.Cells Cloud REST API** 的一部分，可操作存储于云端的 Excel 工作表。

有关相关操作，请参阅 **[获取图表分类轴](/charts/category-axis/get/)** 端点。

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型    | 位置   | 描述                                           |
| ------------ | ------- | ------ | ---------------------------------------------- |
| name         | string  | path   | Excel 文件的名称（包含扩展名）。               |
| sheetName    | string  | path   | 包含图表的工作表名称。                         |
| chartIndex   | integer | path   | 图表在工作表中的从零开始的索引。               |
| folder       | string  | query  | 文件所在的云端存储文件夹。                     |
| storageName  | string  | query  | 存储服务的名称（例如：Aspose Cloud）。         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
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
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "值",
    "Format": {
      "NumberFormat": "常规",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**可能的 HTTP 状态码**

| 状态码 | 描述                                         |
|--------|----------------------------------------------|
| 200    | 成功 — 返回值轴信息。                        |
| 400    | 请求错误 — 缺少或无效的必需参数。            |
| 401    | 未授权 — 缺少或无效的身份验证令牌。          |
| 404    | 未找到 — 指定的工作簿、工作表或图表不存在。  |
| 500    | 内部服务器错误 — 服务器上发生意外错误。      |

响应包含一个详细的 `ValueAxis` 对象，其属性包括 `Minimum`、`Maximum`、`MajorUnit`、`MinorUnit`、`Title` 和 `Format`。在完整实现中，可能还会提供额外的格式化详情。

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
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