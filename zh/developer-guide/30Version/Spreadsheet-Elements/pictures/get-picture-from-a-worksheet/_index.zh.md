---
title: "获取 Excel 工作表中的所有图片"
second_title: "文档"
linktitle: "获取全部"
type: docs
url: /pictures/get-all/
aliases: [/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel 工作表, 图片 API, 获取所有图片, REST API, SDK"
description: "通过 Aspose.Cells Cloud REST API 从 Excel 工作表中检索所有图片对象。"
ArticleTitle: "获取 Excel 工作表中的所有图片 - Aspose.Cells Cloud API"
weight: 10
---

此 REST API 用于从 Excel 工作表中检索所有图片信息。

**前提条件**  
调用此接口前，请确保您已具备以下条件：

- 有效的 Aspose Cloud JWT 访问令牌。  
- 目标 Excel 文件已上传至所选存储空间。  
- 正确的存储名称（若使用自定义存储空间）。  
- 包含图片的工作表名称。

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**注意：** 调用 API 时请使用 HTTPS（TLS 1.2 或更高版本），并在 `Authorization` 请求头中包含有效的 JWT 令牌。

### **安全与身份认证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

### **请求参数**

| 参数名称     | 类型   | 位置   | 描述                                   |
| ------------ | ------ | ------ | -------------------------------------- |
| name         | string | path   | Excel 文件的名称。                     |
| sheetName    | string | path   | 包含图片的工作表名称。                 |
| folder       | string | query  | 文件所在的文件夹路径。                 |
| storageName  | string | query  | 存储服务的名称。                       |

### 错误响应

| HTTP 状态码 | 描述                                       |
| ----------- | ------------------------------------------ |
| 401         | 未授权——缺少或令牌无效。                   |
| 404         | 未找到——指定的文件、工作表或分页索引不存在。 |
| 400         | 请求错误——请求语法错误或参数无效。         |
| 500         | 服务器内部错误——遇到意外情况。             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**成功响应**——成功调用将返回 HTTP 200 状态码，响应体为 JSON 格式，包含 `Pictures` 对象，其中列出了每张图片的资源链接。

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加速开发进程的最佳方式。SDK 封装了底层细节，使您能专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

您可直接从各语言的包管理器（如 .NET 的 NuGet、Java 的 Maven Central、PHP 的 Composer、Node.js 的 npm、Python 的 PyPI、Perl 的 CPAN 以及 Go 的 Go modules）下载 SDK。

*另请参阅：* 添加图片、删除图片、更新图片属性。