---
title: "更新图表次坐标轴"
type: docs
url: /zh/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, 图表, 次坐标轴, REST API, 更新图表, Excel, 云 API"
description: "了解如何使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中图表的次坐标轴。"
ArticleTitle: "更新图表次坐标轴 – Aspose.Cells Cloud API"
---

此 REST API 用于更新图表的次坐标轴。

## PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名        | 类型     | 位置   | 描述                                             |
| ------------- | -------- | ------ | ------------------------------------------------ |
| name          | string   | path   | Excel 文件的名称。                               |
| sheetName     | string   | path   | 包含图表的工作表名称。                           |
| chartIndex    | integer  | path   | 要更新的图表的从零开始的索引。                   |
| axis          | object   | body   | 包含新设置的次坐标轴对象。                       |
| folder        | string   | query  | 文件所在的文件夹路径。                           |
| storageName   | string   | query  | 存储服务的名称。                                 |

**身份验证** – 该 API 需要有效的 OAuth 2.0 访问令牌。请按照[身份验证指南](https://docs.aspose.cloud/cells/authentication/)生成 JWT 令牌，并将该令牌以 `Authorization` 头的形式包含在请求中，如下方 cURL 示例所示。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis)定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* 坐标轴设置，例如 "Title": "新坐标轴标题", "IsVisible": true */
        }
      }'
```

*请将 `{name}`、`{sheetName}`、`{chartIndex}`、`{folder}` 和 `{storageName}` 替换为您的实际值。请求体中必须包含 `axis` 对象，并指定所需的设置。*

{{< /tab >}}

{{< tab tabNum="2" >}}

**成功响应（200）**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "新坐标轴标题",
      "IsVisible": true,
      /* 其他坐标轴属性 */
    }
  }
}
```

**错误响应**

| 状态码 | 描述                                       |
|--------|--------------------------------------------|
| 400    | 请求错误 – 缺少或无效的参数。              |
| 401    | 未授权 – 无效或缺失 JWT 令牌。             |
| 404    | 未找到 – 指定的文件、工作表或图表不存在。  |
| 500    | 服务器内部错误 – 服务器上出现意外情况。    |

```json
{
  "Code": 400,
  "Message": "无效的请求体。"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包家族

SDK 可简化开发过程，处理底层细节，让您专注于业务逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
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

**注意事项与最佳实践**

* `chartIndex` 参数为从零开始的索引，工作表中的第一个图表索引为 0。
* 该 API 支持 `.xlsx` 和 `.xls` 工作簿格式。
* 仅在 `axis` 对象中包含您需要修改的属性；未指定的属性将保留其现有值。
* 遵守速率限制规则（通常每个账户每分钟最多 100 个请求），以避免被限流。