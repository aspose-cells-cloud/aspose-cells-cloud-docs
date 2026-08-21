---
title: "向 Excel 工作表添加形状"
second_title: "文档"
linktitle: "添加"
type: docs
url: /zh/shapes/add/
aliases: [  /zh/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells, 添加形状, Excel, REST API, 云 SDK, shapeDTO, 绘图类型"
description: "了解如何使用 Aspose.Cells Cloud REST API v3.0 向 Excel 工作表添加形状（如圆弧、线条、矩形等）。包含请求语法、必需参数、身份验证步骤及示例 SDK 代码。"
weight: 30
ArticleTitle: "使用 Aspose.Cells Cloud API 向 Excel 工作表添加形状"
---

此 REST API 可向 Excel 工作表添加形状。  
该端点属于 **API 版本 v3.0**；请确保您使用通过 Aspose Cloud OAuth2 流程（client-id/client-secret）获取的 JWT 访问令牌，并将其包含在 `Authorization: Bearer <token>` 请求头中。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **请求参数**

| 参数名             | 类型     | 位置   | 描述                                                                                      |
| ------------------ | -------- | ------ | ----------------------------------------------------------------------------------------- |
| name               | string   | path   | 文档名称。                                                                                |
| sheetName          | string   | path   | 工作表名称。                                                                              |
| shapeDTO           | object   | body   | 描述待添加形状的 JSON 对象（完整架构请参见 OpenAPI 规范）。                               |
| drawingType        | string   | query  | 形状对象类型（如 `arc`、`line`、`rectangle`）。                                           |
| upperLeftRow       | integer  | query  | 形状左上角所在的行索引。                                                                  |
| upperLeftColumn    | integer  | query  | 形状左上角所在的列索引。                                                                  |
| top                | integer  | query  | 形状顶部边缘与其起始位置之间的垂直偏移量（单位：像素）。                                  |
| left               | integer  | query  | 形状左侧边缘与其起始位置之间的水平偏移量（单位：像素）。                                  |
| width              | integer  | query  | 形状宽度（单位：像素）。                                                                  |
| height             | integer  | query  | 形状高度（单位：像素）。                                                                  |
| folder             | string   | query  | 包含该文档的文件夹路径。                                                                  |
| storageName        | string   | query  | 存储空间名称。                                                                            |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
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
  "ShapeId": 5
}
```

_成功响应将返回 HTTP 状态码、状态文本以及新创建形状的标识符（`ShapeId`）。_

{{< /tab >}}

{{< /tabs >}}

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 筛选器应用成功；响应包含操作详情。             |
| 400    | Bad Request      | 参数缺失或无效（如不支持的文件类型）。         |
| 401    | Unauthorized     | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large| 上传文件超出大小限制。                         |
| 500    | Internal Server Error | 服务器内部意外错误。                      |

典型错误响应包括：

- **400 Bad Request** – 参数缺失或无效。  
- **401 Unauthorized** – JWT 令牌无效或缺失。  
- **404 Not Found** – 指定的工作表或文档不存在。

每个错误均以 JSON 对象形式返回，包含 `Code` 和 `Message` 字段。

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务本身。如需了解 Aspose.Cells Cloud SDK 的完整列表，请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}