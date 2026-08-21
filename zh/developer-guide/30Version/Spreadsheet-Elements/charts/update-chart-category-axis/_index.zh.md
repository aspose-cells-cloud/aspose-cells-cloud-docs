---
title: "更新图表分类轴"
type: docs
url: /charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, 图表, 分类轴, REST API, Excel, 云 SDK"
description: "使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中图表的分类轴。"
ArticleTitle: "更新图表分类轴 – Aspose.Cells Cloud API"
---

此 REST API 用于更新图表的分类轴。

## PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型    | 位置   | 描述                                       |
| ------------- | ------- | ------ | ------------------------------------------ |
| name          | string  | path   | Excel 文件的名称。                         |
| sheetName     | string  | path   | 包含图表的工作表名称。                     |
| chartIndex    | integer | path   | 待更新图表的零基索引。                     |
| axis          | object  | body   | 定义分类轴属性的 JSON 对象。               |
| folder        | string  | query  | 云存储中文件所在文件夹（可选）。           |
| storageName   | string  | query  | 存储名称（可选）。                         |

**请求体结构 – `axis` 对象**

| 属性                  | 类型    | 描述                                                                 |
|-----------------------|---------|----------------------------------------------------------------------|
| IsAutomaticMajorUnit  | boolean | 是否自动计算主刻度单位。                                             |
| MajorUnit             | number  | 当 `IsAutomaticMajorUnit` 为 `false` 时的主刻度单位值。              |
| IsAutomaticMinorUnit  | boolean | 是否自动计算次刻度单位。                                             |
| MinorUnit             | number  | 当 `IsAutomaticMinorUnit` 为 `false` 时的次刻度单位值。              |
| Title                 | object  | 轴标题设置（例如 `Text`、`Font`、`Visible`）。                       |
| TickLabelPosition     | string  | 刻度标签位置（例如 `Low`、`High`、`NextToAxis`）。                   |
| ...                   | ...     | 其他轴属性，请参阅 API 规范定义。                                    |

**HTTP 状态码**

| 状态码 | 含义               | 描述                                               |
|--------|--------------------|----------------------------------------------------|
| 200    | OK（成功）         | 筛选器应用成功；响应包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。           |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                             |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                               |

**前置条件 / 身份验证**

调用此接口前，您需从 Aspose.Cells Cloud 身份验证服务 (`/connect/token`) 获取 JWT 访问令牌，并在 `Authorization` 请求头中包含该令牌，如下例所示：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "分类轴",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**示例响应**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器发起 REST 交互。

### 注意事项

* 该接口仅支持 HTTPS；使用 HTTP 可能触发浏览器的混合内容警告。
* 所有占位符值（`{name}`、`{sheetName}`、`{chartIndex}`、`{folder}`、`{storageName}`）必须替换为实际标识符。
* 支持更新分类轴的图表类型，请参阅 API 参考文档。

## 云 SDK 开发工具包系列

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，使您能专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 云服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}