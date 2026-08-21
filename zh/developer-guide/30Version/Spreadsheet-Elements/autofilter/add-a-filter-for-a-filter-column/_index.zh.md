---
title: "在 Excel 工作表中添加筛选器"
second_title: "文档"
linktitle: "添加筛选器"
type: docs
url: /zh/autofilter/add-filter/
aliases: [  /zh/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, 云, Excel, 自动筛选, 添加筛选器, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表的列中添加自动筛选器。包含 cURL、SDK 示例和参数指南。"
weight: 60
ArticleTitle: "使用 Aspose.Cells Cloud 在 Excel 工作表中添加筛选器"
---

**先决条件：** 调用此 API 前，您必须获取有效的 JWT 令牌，确保目标工作簿已上传至指定存储空间，并拥有访问该文件的必要权限。建议使用 cURL 7.68 或更高版本以运行命令行示例。

此 REST API 可在 Excel 工作表的特定列上添加筛选器。

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型    | 位置   | 描述 |
|----------------|---------|--------|------|
| name           | string  | Path   | 工作簿名称。 |
| sheetName      | string  | Path   | 工作表名称。 |
| range          | string  | Query  | 包含筛选器的单元格范围（例如 `A1:B1`）。 |
| fieldIndex     | integer | Query  | 应用筛选器的列的从零开始的索引。 |
| criteria       | string  | Query  | 筛选条件（例如值或表达式）。 |
| matchBlanks    | boolean | Query  | 设置为 `true` 表示在筛选中包含空白单元格；否则为 `false`。 |
| refresh        | boolean | Query  | 设置为 `true` 表示应用后刷新筛选器；否则为 `false`。 |
| folder         | string  | Query  | 原始工作簿所在的文件夹。 |
| storageName    | string  | Query  | 存储服务的名称。 |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述 |
|--------|--------------------|------|
| 200    | OK（成功）         | 筛选器已成功应用；响应包含操作详细信息。 |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（负载过大） | 上传的文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。 |

## 如何使用 SDK 调用 PutWorksheetFilter API

### PutWorksheetFilter API 规范

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用此 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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

使用 SDK 是开发速度最快的方式。SDK 会处理底层细节，使您能专注于项目本身。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}