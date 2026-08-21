---
title: "获取 Excel 工作簿中的命名区域"
second_title: "文档"
linktitle: "命名"
type: docs
url: /zh/ranges/get/name/
aliases: [  /zh/get-named-ranges-inside-the-workbook/ ]
keywords: "命名区域, Excel, Aspose.Cells, 云 API, 工作表"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作簿中检索命名区域。包含请求详情、示例 cURL 命令以及多种编程语言的 SDK 示例。"
ArticleTitle: "获取 Excel 工作簿中的命名区域 – Aspose.Cells Cloud API"
weight: 10
---

此 REST API 返回工作表中定义的命名区域信息。

**背景知识** – *命名区域* 是用户自定义的标识符，用于引用工作表中的特定单元格或单元格区域。命名区域可简化公式创建、提升可读性，并支持以编程方式访问工作簿中频繁使用的区域。

**前置条件** – 访问 Aspose.Cells Cloud API 需要有效的 JWT 访问令牌。您可通过 OAuth 2.0 令牌端点，使用您的 Aspose Cloud 客户端 ID 和客户端密钥进行身份验证来获取该令牌。在每个请求的 `Authorization: Bearer <jwt token>` 标头中包含该令牌。

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，要求进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名         | 类型   | 位置       | 描述                             |
| -------------- | ------ | ---------- | -------------------------------- |
| name           | string | 路径参数   | Excel 文档的名称。               |
| folder         | string | 查询字符串 | 包含该文档的文件夹路径。         |
| storageName    | string | 查询字符串 | 文档所在的存储空间名称。         |

**HTTP 状态码**

| 状态码 | 含义                 | 描述                                     |
|--------|----------------------|------------------------------------------|
| 200    | OK（成功）           | 过滤器应用成功；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求体过大） | 上传文件超过大小限制。                   |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                    |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具调用 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 获取命名区域。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应模型**

| 字段名         | 类型    | 描述                                         |
|----------------|---------|----------------------------------------------|
| `ColumnCount`  | integer | 区域中的列数。                               |
| `ColumnWidth`  | number  | 每列的宽度（单位：点）。                     |
| `FirstColumn`  | integer | 区域中第一列的从零开始索引。                 |
| `FirstRow`     | integer | 区域中第一行的从零开始索引。                 |
| `Name`         | string  | 区域的用户自定义名称。                       |
| `RefersTo`     | string  | 定义单元格引用的公式（例如 `=Sheet1!$B$10:$H$10`）。 |
| `RowCount`     | integer | 区域中的行数。                               |
| `RowHeight`    | number  | 每行的高度（单位：点）。                     |
| `Worksheet`    | string  | 包含该区域的工作表名称。                     |

## 云 SDK 开发工具包家族

使用 SDK 是集成该功能的最快方式。SDK 会处理底层细节，让您专注于业务逻辑。如需获取 Aspose.Cells Cloud SDK 的完整列表，请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}