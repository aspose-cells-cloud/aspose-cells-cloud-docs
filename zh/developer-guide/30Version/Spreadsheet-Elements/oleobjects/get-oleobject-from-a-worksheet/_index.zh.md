---
title: "从 Excel 工作表获取 OLE 对象 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "获取"
type: docs
url: /zh/oleobjects/get/
aliases: [/zh/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, ole object, excel, worksheet, get ole object, rest api"
description: "使用 Aspose.Cells Cloud REST API 从工作表中检索 OLE 对象（图像、图表或嵌入文件）。包含 HTTPS 端点、必需参数、示例 cURL 以及多种语言的 SDK 代码。"
ArticleTitle: "从 Excel 工作表获取 OLE 对象 – Aspose.Cells Cloud API"
weight: 10
---

此 REST API 可从 Excel 工作表中检索 **OLE 对象**。

## 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需要 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### 请求参数

| 参数名         | 类型    | 位置   | 描述                                         |
| -------------- | ------- | ------ | -------------------------------------------- |
| name           | string  | path   | 文档名称。                                   |
| sheetName      | string  | path   | 工作表名称。                                 |
| objectNumber   | integer | path   | 工作表内的对象编号。                         |
| format         | string  | query  | 对象导出的期望格式（例如 `png`、`jpeg`）。   |
| folder         | string  | query  | 包含文档的文件夹。                           |
| storageName    | string  | query  | 要使用的存储名称。                           |

### 存储选项

- **folder** – 指定工作簿所在的默认存储子文件夹。
- **storageName** – 若工作簿存储在其他位置，则覆盖默认存储名称。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具调用 Aspose.Cells Web 服务。以下示例演示如何请求将 OLE 对象作为 PNG 图像返回。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### 二进制图像响应

当 `format` 设置为图像类型（例如 `png`）时，API 返回二进制图像数据，并附带响应头：

```
Content-Type: image/png
```

（图像文件将直接流式传输到客户端。）

### JSON 元数据响应

若省略 `format` 或将其设置为 `json`，API 将返回一个 JSON 载荷，描述 OLE 对象信息：

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## 错误响应

| HTTP 状态码 | 错误代码     | 描述                           |
| ----------- | ------------ | ------------------------------ |
| 400         | BadRequest   | 缺少或无效的参数。             |
| 401         | Unauthorized | JWT 令牌无效或缺失。           |
| 404         | NotFound     | 未找到工作簿、工作表或 OLE 对象。 |
| 500         | ServerError  | 服务器意外错误。               |

**示例 404 响应**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "未在工作表 'Sheet1' 中找到编号为 0 的请求 OLE 对象。"
}
```

## 云 SDK 家族

使用 SDK 是集成 API 的最快方式。SDK 处理底层细节，让您专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}