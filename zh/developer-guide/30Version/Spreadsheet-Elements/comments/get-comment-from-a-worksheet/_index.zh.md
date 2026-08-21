---
title: "获取工作表注释 – Aspose.Cells Cloud API 文档"
type: docs
url: /zh/comments/get/
aliases: [  /zh/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, 工作表注释, API, GET, Excel"
description: "了解如何使用 Aspose.Cells Cloud API（v3.0）通过单元格名称获取工作表注释。包含请求 URL、参数、cURL 示例、响应详情及 SDK 代码片段。"
weight: 10
ArticleTitle: "获取工作表注释 – Aspose.Cells Cloud API 文档"
---

此 REST API 可通过**Aspose.Cells Cloud**按单元格名称获取工作表注释。

**前置条件**：调用此操作前，您必须在 `Authorization` 请求头中包含有效的 JWT 访问令牌（格式为 `Bearer <jwt token>`）。令牌可通过 [身份验证指南](/cells/authentication/) 中所述的 Aspose.Cells Cloud 身份验证流程获取。

## GetWorksheetComment API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 位置（URL 路径 / 查询字符串） | 描述                                               |
| ------------ | ------ | ----------------------------- | -------------------------------------------------- |
| name         | string | URL 路径                      | Excel 文件的名称。                                 |
| sheetName    | string | URL 路径                      | 包含注释的工作表名称。                             |
| cellName     | string | URL 路径                      | 要获取注释的单元格地址（例如 **A1**）。            |
| folder       | string | 查询字符串                    | 文档所在的文件夹路径。                             |
| storageName  | string | 查询字符串                    | 存储服务的名称。                                   |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应说明**：API 返回一个 JSON 对象，其中包含一个 `Comment` 对象，字段如下：

| 字段名                      | 类型    | 描述                                     |
| --------------------------- | ------- | ---------------------------------------- |
| `CellName`                  | string  | 单元格地址（例如 **A1**）。              |
| `Author`                    | string  | 注释作者姓名。                           |
| `HtmlNote`                  | string  | 注释的 HTML 格式内容（若存在）。         |
| `Note`                      | string  | 注释的纯文本内容。                       |
| `AutoSize`                  | boolean | 是否自动调整注释框大小。                 |
| `IsVisible`                 | boolean | 注释是否可见。                           |
| `Width`                     | integer | 注释框宽度（以字符数为单位）。           |
| `Height`                    | integer | 注释框高度（以字符数为单位）。           |
| `TextHorizontalAlignment`   | string  | 文本水平对齐方式（例如 **Bottom**）。    |
| `TextOrientationType`       | string  | 文本方向（例如 **TopToBottom**）。       |
| `TextVerticalAlignment`     | string  | 文本垂直对齐方式（例如 **Bottom**）。    |

## 常见错误

- **401 未授权（Unauthorized）** – 请确认 JWT 令牌有效、未过期，并正确放置于 `Authorization` 请求头中。
- **404 未找到（Not Found）** – 请确认文件名、工作表名和单元格地址正确，并且文件存在于指定文件夹/存储中。
- **500 内部服务器错误（Internal Server Error）** – 请检查请求载荷数据格式是否正确，并确认服务是否正常运行。

**HTTP 状态码**

| 状态码 | 含义           | 描述                                     |
| ------ | -------------- | ---------------------------------------- |
| 200    | OK（成功）     | 筛选器应用成功；响应包含操作详情。       |
| 400    | Bad Request    | 缺失或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized   | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large | 上传文件超过大小限制。                |
| 500    | Internal Server Error | 服务器内部错误。                    |

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加速开发的最佳方式。SDK 能自动处理底层细节，让您专注于项目核心任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}