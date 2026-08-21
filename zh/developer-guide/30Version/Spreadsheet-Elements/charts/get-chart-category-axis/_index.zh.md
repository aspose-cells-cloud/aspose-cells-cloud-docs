---
title: "获取图表分类轴"
type: docs
url: /zh/charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, 图表分类轴, Excel, REST API, 云存储, OAuth2, API 文档"
description: "使用 Aspose.Cells Cloud REST API 获取 Excel 工作表中图表的分类轴。"
ArticleTitle: "获取图表分类轴 – Aspose.Cells Cloud API 文档"
---

此 REST API 用于获取图表的**分类轴**。  
要调用此接口，您必须提供有效的 OAuth 2.0 访问令牌，并且工作簿必须存储在 Aspose Cloud 存储中。

**前置条件**  
在使用此接口前，请确保满足以下条件：  

- 已获取有效的 OAuth 2.0 令牌，且该令牌可用于 Aspose Cloud 服务。  
- 工作簿文件已上传至 Aspose Cloud 存储（默认或指定文件夹）。  
- 您正在使用 **v3.0** 版本的 API，如请求 URL 所示。  
- 调用应用程序具有读取工作簿及其工作表的权限。

## GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**背景说明** – 从工作表中移除所有图表适用于需要重置工作表的视觉布局、替换过时的可视化图表，或在不保留之前图表数据的前提下准备工作簿以供复用的场景。

### **安全与认证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

### 请求参数

| 参数名称      | 类型     | 位置   | 描述                                               |
| ------------- | -------- | ------ | -------------------------------------------------- |
| name          | string   | path   | 工作簿文件的名称。                                 |
| sheetName     | string   | path   | 包含图表的工作表名称。                             |
| chartIndex    | integer  | path   | 请求其轴信息的图表的零基索引。                     |
| folder        | string   | query  | 工作簿所在存储的文件夹路径。                       |
| storageName   | string   | query  | 存储服务的名称（若非默认存储）。                   |

### **响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详细信息。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                          |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                    |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                      |

## 如何使用 SDK 调用 GetChartCategoryAxis API

### GetChartCategoryAxis API 规范

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，使您能够直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 了解 Aspose.Cells Cloud SDK 的完整列表。

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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