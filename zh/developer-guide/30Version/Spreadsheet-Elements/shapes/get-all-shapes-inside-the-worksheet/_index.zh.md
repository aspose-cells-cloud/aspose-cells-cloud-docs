---
title: "获取 Excel 工作表中的所有形状"
second_title: "文档"
linktitle: "获取全部"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, 云 API, Excel 形状, 获取形状, REST, SDK"
description: "使用 Aspose.Cells Cloud REST API 从工作表中检索所有形状（图表、图片、文本框）。包含 cURL 示例、SDK 代码片段、身份验证步骤和错误处理。"
ArticleTitle: "获取 Excel 工作表中的所有形状"
weight: 10
---

此 REST API 可用于检索 Excel 工作表中的所有形状。

## 安全与身份验证
Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### 请求参数

| 参数名称        | 类型   | 位置   | 描述                                                                                       |
| --------------- | ------ | ------ | ------------------------------------------------------------------------------------------ |
| **name**        | string | path   | Excel 文件的名称。                                                                         |
| **sheetName**   | string | path   | 工作表的名称。                                                                             |
| **folder**      | string | query  | 存放文档的文件夹。                                                                         |
| **storageName** | string | query  | 要使用的存储服务的名称。                                                                   |
| **include**     | string | query  | 设置为 `details` 以返回完整形状属性；否则仅返回 `link` 对象。                              |

> **可选**：若文件位于根存储中，则可省略 `folder`、`storageName` 和 `include`。

您可以使用 cURL 命令行工具访问 Aspose.Cells Web 服务。以下示例演示了一个包含可选查询参数的请求。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 响应字段

`Shapes` 对象包含一个 `Shape` 项列表。每个形状包含以下属性（当使用 `include=details` 标志时；否则仅返回 `link` 对象）。

| 属性   | 类型   | 描述                                                       |
| ------ | ------ | ---------------------------------------------------------- |
| **Name**   | string | 分配给形状的名称（例如 “Chart 1”）。                         |
| **Type**   | string | 形状类型（例如 `Chart`、`Picture`、`TextBox`）。             |
| **Top**    | number | 从工作表上边缘到形状顶部的距离（以磅为单位）。               |
| **Left**   | number | 从工作表左边缘到形状左侧的距离（以磅为单位）。               |
| **Width**  | number | 形状的宽度（以磅为单位）。                                   |
| **Height** | number | 形状的高度（以磅为单位）。                                   |
| **Link**   | object | 超链接信息（`Href`、`Rel`、`Type`、`Title`）。               |

## 错误处理

| HTTP 状态码 | 描述                           | 示例错误响应体                                                        |
| ----------- | ------------------------------ | --------------------------------------------------------------------- |
| **400**     | 请求错误 — 参数格式不正确。    | `{ "Code": 400, "Message": "Invalid parameter value." }`              |
| **401**     | 未授权 — 缺少或无效的令牌。    | `{ "Code": 401, "Message": "Access token is missing or invalid." }`  |
| **404**     | 未找到 — 工作簿或工作表不存在。| `{ "Code": 404, "Message": "File or worksheet not found." }`         |
| **500**     | 服务器内部错误 — 意外情况。    | `{ "Code": 500, "Message": "An unexpected error occurred." }`        |

成功请求将返回 **HTTP 200** 状态码，并附带一个包含形状列表的 `Shapes` 对象，如上文响应示例所示。

该 API 对每个 JWT 令牌的请求频率限制为 **每分钟 150 次**。超出限制时将返回 **HTTP 429** 状态码，并附带 `Retry-After` 响应头，指示重试时间。

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 可处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}