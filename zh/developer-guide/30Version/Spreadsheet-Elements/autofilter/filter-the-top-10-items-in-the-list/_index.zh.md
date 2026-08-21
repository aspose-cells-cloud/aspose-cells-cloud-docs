---
title: "为 Excel 工作表添加前 10 项筛选器（Aspose.Cells Cloud）"
ArticleTitle: "为 Excel 工作表添加前 10 项筛选器 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "添加前 10 项筛选器"
type: docs
url: /zh/autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, 自动筛选, 前 10 项筛选器, Excel API"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表应用前 10 项自动筛选。内容包括接口端点、参数说明、基于 HTTPS 的 cURL 示例、认证详情、错误处理，以及 C#、Java、Python 等多种语言的 SDK 代码片段。"
weight: 65
---

此 REST API 可对列表中的**前 10 项**进行筛选。

> **前置条件**  
> • 使用 Aspose.Cells Cloud 认证机制获取有效的 JWT 令牌。  
> • 将 Excel 工作簿上传至您的 Aspose Cloud 存储空间（或指定其所在的存储空间/文件夹）。  
> • 明确需要筛选的工作表名称及单元格范围。

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### 请求参数

| 参数名         | 类型    | 位置   | 是否必需 | 默认值 | 描述                                                                 |
| -------------- | ------- | ------ | -------- | ------ | -------------------------------------------------------------------- |
| **name**       | string  | 路径   | 是       | —      | Excel 文件的名称。                                                  |
| **sheetName**  | string  | 路径   | 是       | —      | 包含数据的工作表名称。                                              |
| **range**      | string  | 查询   | 是       | —      | 应用筛选的单元格范围（例如 `A1:B10`）。                             |
| **fieldIndex** | integer | 查询   | 是       | —      | 筛选所依据列的从零开始的索引。                                      |
| **isTop**      | boolean | 查询   | 是       | `true` | 为 `true` 表示筛选前 N 项；为 `false` 表示筛选后 N 项。            |
| **isPercent**  | boolean | 查询   | 否       | `false`| 为 `true` 时，将 `itemCount` 视为百分比；为 `false` 时为绝对数量。  |
| **itemCount**  | integer | 查询   | 否       | `10`   | 筛选中包含的项目数量。                                              |
| **matchBlanks**| boolean | 查询   | 否       | `false`| 为 `true` 时，将空单元格包含在筛选结果中。                          |
| **refresh**    | boolean | 查询   | 否       | `false`| 为 `true` 时，在应用筛选后刷新筛选结果。                            |
| **folder**     | string  | 查询   | 否       | —      | 存储空间中 Excel 文件所在的文件夹。                                 |
| **storageName**| string  | 查询   | 否       | —      | Aspose Cloud 存储空间的名称。                                       |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**典型错误响应**

```json
{
    "Code":400,
    "Message":"Bad Request – 缺少或无效的参数。"
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – JWT 令牌无效或缺失。"
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – 上传的文件超出允许大小。"
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – 意外的服务器错误。"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                   |
|--------|----------------|----------------------------------------|
| 200    | OK（成功）     | 筛选器成功应用；响应包含操作详情。      |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（载荷过大） | 上传的文件超过大小限制。            |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。             |

## 如何结合 SDK 使用 PutWorksheetFilterTop10 API

### PutWorksheetFilterTop10 API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
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

使用 SDK 是最快捷的开发方式。SDK 将处理底层细节，让您专注于业务逻辑。您可访问 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}