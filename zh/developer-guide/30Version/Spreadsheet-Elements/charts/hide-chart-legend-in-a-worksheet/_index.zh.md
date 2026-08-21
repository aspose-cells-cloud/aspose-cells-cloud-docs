---
title: "隐藏 Excel 工作表中的图表图例 — Aspose.Cells Cloud API"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, 隐藏图表图例, REST API, 云 SDK, 图表图例"
description: "了解如何使用 Aspose.Cells Cloud REST API 隐藏 Excel 工作表中的图表图例。内容包括 HTTPS 端点、所需身份验证、请求语法、响应详情、错误处理以及 SDK 示例。"
---

此 REST API 用于隐藏图表中的图例。**图表图例** 是用于标识图表中数据系列的框。

该 API 需要有效的 Aspose Cloud JWT 令牌，工作簿必须已上传至 Aspose Cloud 存储空间，且所使用的 API 版本为 **v3.0**。

## 安全与身份验证
Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### 请求参数

| 参数名称        | 类型    | 位置   | 描述                        |
| --------------- | ------- | ------ | --------------------------- |
| **name**        | string  | 路径   | 工作簿名称。                |
| **sheetName**   | string  | 路径   | 工作表名称。                |
| **chartIndex**  | integer | 路径   | 图表索引。                  |
| **folder**      | string  | 查询   | 工作簿所在文件夹（可选）。  |
| **storageName** | string  | 查询   | 存储空间名称（可选）。      |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) 定义了此公开可访问的编程接口。

您可以使用 cURL 命令行工具轻松调用该 API。以下示例演示了隐藏 `_Sample_Test_Book.xls_` 中图表 0 图例的请求。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

## 响应

| HTTP 状态码                   | 描述                             | 示例 JSON                                                     |
| ----------------------------- | -------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | 图例已成功隐藏。                 | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | 缺失或无效的 JWT 令牌。          | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | 工作簿、工作表或图表不存在。     | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | 服务器内部意外错误。             | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## 常见问题

**Q:** _如何使用 Aspose.Cells Cloud 隐藏图表图例？_  
**A:** 向 `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` 发送 `DELETE` 请求，并在 `Authorization` 请求头中包含有效的 JWT 令牌。收到 `200 OK` 响应表示操作成功。

**Q:** _隐藏图表图例 API 所需的身份验证方式是什么？_  
**A:** 需在请求头中包含 `Authorization: Bearer <jwt token>`。您可以通过 Aspose Cloud OAuth 流程获取该令牌。

**Q:** _如果图表索引无效，会收到什么错误响应？_  
**A:** 服务将返回 `404 Not Found`，响应体中包含 `Code: 404` 以及描述缺失图表的提示信息。

**Q:** _是否可以使用 HTTP 而非 HTTPS？_  
**A:** 不可以。所有 Aspose Cloud 端点均强制使用 HTTPS 以确保安全性。

## 云 SDK 家族

使用 SDK 是开发速度最快的途径。SDK 将底层细节抽象化，使您能专注于项目任务本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**即将推出** – Swift SDK 示例将在不久后添加。  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "隐藏 Excel 工作表中的图表图例 — Aspose.Cells Cloud API",
  "description": "分步指南：使用 Aspose.Cells Cloud REST API 隐藏 Excel 工作表中的图表图例。内容包括 HTTPS 端点、身份验证、请求语法、响应详情、错误处理以及 SDK 示例。",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "首页", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "图表", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "隐藏图表图例", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "使用 Aspose.Cells Cloud API 隐藏图表图例"
}
</script>