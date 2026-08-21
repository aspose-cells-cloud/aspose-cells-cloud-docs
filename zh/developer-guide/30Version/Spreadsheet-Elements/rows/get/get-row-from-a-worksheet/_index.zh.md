---
title: "从 Excel 工作表中获取行描述"
second_title: "Document"
linktitle: "行"
type: docs
url: /zh/rows/get/row/
aliases: [  /zh/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud、Excel 行 API、获取工作表行、REST API、.NET SDK、Java SDK、Python SDK"
description: "使用 Aspose.Cells Cloud REST API 获取 Excel 工作表中特定行的详细信息（如高度、样式、隐藏状态等）。包含 curl 示例、SDK 代码片段和错误处理。"
weight: 10
ArticleTitle: "从 Excel 工作表中获取行描述 – Aspose.Cells Cloud API"
---

**前置条件：**  
- 获取有效的 JWT 访问令牌，并将其包含在 `Authorization: Bearer <jwt token>` 请求头中。  
- 确保工作簿已存储于 Aspose Cloud 存储中，或指定其所在文件夹路径。  
- 使用 API 版本 **v3.0**，如端点 URL 所示。

该 REST API 可根据行索引检索 Excel 工作表中的行数据。

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称      | 类型    | 位置   | 描述                                   |
| ------------- | ------- | ------ | -------------------------------------- |
| name          | string  | path   | 工作簿文件的名称。                     |
| sheetName     | string  | path   | 工作簿内工作表的名称。                 |
| rowIndex      | integer | path   | 要检索行的从零开始的索引。             |
| folder        | string  | query  | 包含工作簿的文件夹路径。               |
| storageName   | string  | query  | 工作簿所在存储的名称。                 |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) 定义了一个公开可用的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。请在请求头中包含 `Authorization: Bearer <jwt token>` 以完成身份验证。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**响应架构**

| 属性              | 类型    | 描述                                               |
|-------------------|---------|----------------------------------------------------|
| `GroupLevel`      | integer | 行的分级层级（用于分组）。                         |
| `Height`          | number  | 行高（单位为磅）。                                 |
| `Index`           | integer | 返回的行的从零开始的索引。                         |
| `IsBlank`         | boolean | 是否该行不包含任何数据。                           |
| `IsHeightMatched` | boolean | 行高是否与默认行高一致。                           |
| `IsHidden`        | boolean | 行是否处于隐藏状态。                               |
| `Style`           | object  | 包含该行样式信息的对象。                           |
| `link`            | object  | 指向该行资源的超链接引用。                         |
| `Code`            | integer | 响应的 HTTP 状态码。                               |
| `Status`          | string  | 状态的文本描述（例如，“OK”）。                     |

{{< /tab >}}

{{< /tabs >}}

**说明 / 错误处理：** 该 API 可能返回以下 HTTP 状态码：

- **200** – 成功；返回行数据。  
- **401** – 未授权；JWT 令牌缺失或无效。  
- **404** – 未找到；指定的工作簿、工作表或行不存在。  
- **500** – 服务器内部错误；发生意外情况。

| 状态码 | 描述                             | 解决方案                             |
|--------|----------------------------------|--------------------------------------|
| 200    | 成功 — 返回行数据。              | —                                    |
| 401    | 未授权 — 缺失或无效的 JWT 令牌。  | 提供有效的 JWT 令牌。                |
| 404    | 未找到 — 工作簿、工作表或行缺失。 | 核实文件名、工作表名及行索引。       |
| 500    | 服务器内部错误 — 意外情况。      | 联系 Aspose 技术支持。               |

完整错误码列表，请参阅 Aspose.Cells Cloud [错误码文档](https://docs.aspose.cloud/cells/)。

## 云 SDK 家族

使用 SDK 是开发的最快方式。SDK 抽象了底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}