---
title: "从 Excel 工作表中按索引获取形状"
second_title: "文档"
linktitle: "获取"
type: docs
url: /zh/shapes/get/
aliases: [/zh/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, Excel 形状 API, 按索引获取形状, 工作表形状, REST API, 形状检索, Aspose.Cells SDK"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表中按索引检索形状（包括其图像数据或元数据）。包含请求语法、参数、响应详情及 SDK 示例。"
weight: 20
ArticleTitle: "从 Excel 工作表中按索引获取形状 – Aspose.Cells Cloud 文档"
---

此 REST API 用于从 Excel 工作表中检索形状（包括其图像数据或元数据）。

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**前提条件**  
- 有效的 Aspose Cloud 访问令牌（Bearer JWT）。  
- 工作簿必须存储在您的 Aspose Cloud 存储中或指定的文件夹中。  

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名         | 类型    | 位置 | 描述                                           |
| -------------- | ------- | ---- | ---------------------------------------------- |
| name           | string  | path | Excel 文档的名称。                             |
| sheetName      | string  | path | 包含该形状的工作表名称。                       |
| shapeindex     | integer | path | 形状在工作表中的从零开始的索引。               |
| folder         | string  | query| 存储文档的文件夹路径。                         |
| storageName    | string  | query| 存储服务的名称。                               |

**注意：** `shapeindex` 为从零开始的索引，第一个形状的索引为 0。如果您未使用默认存储，请确保工作簿已存储在指定的 `folder` 和 `storageName` 中。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape)定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 修正后的端点和路径
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**可能的 HTTP 状态码**

| 状态码 | 描述 |
|--------|------|
| **200 OK** | 成功检索到该形状。 |
| **400 Bad Request** | 请求格式错误或缺少必需参数。 |
| **401 Unauthorized** | 身份验证失败或令牌缺失/无效。 |
| **404 Not Found** | 指定的工作簿、工作表或形状索引不存在。 |
| **500 Internal Server Error** | 发生了意外的服务器错误。 |

**常见错误：** 使用错误的基础域名（`api.aspose.com`）或已弃用的 `/autoshapes/` 路径段会导致 404 错误。请始终使用 `/shapes/` 路径段和 `api.aspose.cloud` 域名。

## 云 SDK 开发工具包

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

有关相关操作，请参阅 **[添加形状](/zh/shapes/add/)** 和 **[更新形状](/zh/shapes/update/)** 的文档。