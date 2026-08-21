---
title: "Excel 工作表中取消合并单元格"
type: docs
url: /zh/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, 取消合并单元格, REST API, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表中取消合并单元格，包含请求示例、响应格式以及多种编程语言的 SDK 代码示例。"
ArticleTitle: "Excel 工作表中取消合并单元格"
---

此 REST API 可用于取消 Excel 文件中的单元格合并。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## 安全与身份验证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

**请求参数**

| 参数名称        | 类型    | 位置   | 描述                                     |
|----------------|---------|--------|------------------------------------------|
| name           | string  | path   | 工作簿文件的名称。                        |
| sheetName      | string  | path   | 工作表的名称。                           |
| startRow       | integer | query  | 要取消合并的第一行的从零开始的索引。       |
| startColumn    | integer | query  | 要取消合并的第一列的从零开始的索引。       |
| totalRows      | integer | query  | 要包含在取消合并操作中的行数。             |
| totalColumns   | integer | query  | 要包含在取消合并操作中的列数。             |
| folder         | string  | query  | 工作簿所在的文件夹路径。                   |
| storageName    | string  | query  | 存储服务的名称。                           |

## **响应**

返回 `CellCloudResponse`。

- **响应字段概览**

| 字段         | 类型    | 描述         |
| ------------ | ------- | ------------ |
| `Status`     | string  |              |
| `Code`       | integer | 200, 400, 401, 500,... |

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                   |
|--------|------------------|----------------------------------------|
| 200    | OK（请求成功）   | 成功应用筛选；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                   |

## 如何使用 SDK 调用 PostWorksheetUnmerge API

### PostWorksheetUnmerge API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) 定义了一个公开可访问的编程接口，您可直接通过网页浏览器进行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
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

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}