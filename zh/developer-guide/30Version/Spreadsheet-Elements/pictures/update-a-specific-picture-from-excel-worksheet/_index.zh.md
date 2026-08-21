---
title: "更新 Excel 文件中的图片"
second_title: "文档"
linktitle: "更新"
type: docs
url: /pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud, Excel, 更新图片, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中的图片。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
ArticleTitle: "使用 Aspose.Cells Cloud REST API 更新 Excel 文件中的图片"
weight: 70
---

此 REST API 用于根据图片索引更新 Excel 工作表中的图片。

**前置条件**：您必须拥有有效的 Aspose Cloud JWT 令牌、存储于 Aspose Cloud 存储中的目标 Excel 文件，并使用 API 版本 3.0 或更高版本。

## PostWorksheetPicture API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **安全与身份认证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

### **请求参数**

| 参数名         | 类型   | 位置   | 描述                                             |
| -------------- | ------ | ------ | ------------------------------------------------ |
| name           | string | path   | Excel 文档的名称。                               |
| sheetName      | string | path   | 包含目标图片的工作表名称。                       |
| pictureIndex   | integer| path   | 待更新图片的从零开始的索引。                     |
| picture        | object | body   | 描述待更新图片属性的 JSON 对象。                 |
| folder         | string | query  | 存放文档的文件夹路径。                           |
| storageName    | string | query  | 存储服务的名称。                                 |

**注意**：图片索引为从零开始计数。支持的图像格式包括 JPEG、PNG、BMP 和 GIF，单张图片最大尺寸为 10 MB。

### 错误响应

| HTTP 状态码 | 描述                                                   |
| ----------- | ------------------------------------------------------ |
| 401         | 未授权 — 缺少或无效的令牌。                            |
| 404         | 未找到 — 指定的文件、工作表或图片索引不存在。         |
| 400         | 请求错误 — 请求语法格式错误或参数无效。                |
| 500         | 内部服务器错误 — 遇到意外情况。                        |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，让您能专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*另请参见*：插入图片、删除图片、获取图片、清除图片 — Aspose.Cells Cloud API 中其他与图片相关的操作。