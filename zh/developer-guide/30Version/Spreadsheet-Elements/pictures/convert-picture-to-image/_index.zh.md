---
title: "Aspose.Cells Cloud API – 从工作表获取图片"
second_title: "文档"
linktype: "文档"
url: /zh/pictures/get/
aliases: [  /zh/convert-picture-to-image/ ]
keywords: "Aspose.Cells, 获取图片, API, Excel, 云, REST"
description: "通过 Aspose.Cells Cloud REST API 从 Excel 工作表中检索特定图片。包含端点、参数、身份验证步骤、响应码及代码示例。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – 从工作表获取图片"
---

此 REST API 可根据图片的从零开始的索引号，从 Excel 工作表中获取图片。

## REST API

调用此端点时，您必须在 **Authorization** 请求头中包含有效的 JWT 访问令牌。令牌需通过 Aspose.Cells Cloud 身份验证流程获取，并需要具备访问文件的相应作用域（scopes）。有关获取令牌的详细信息，请参阅全局 **身份验证** 指南。

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### 请求参数

| 参数名称       | 类型    | 位置 | 描述                                                                                      |
| -------------- | ------- | ---- | ----------------------------------------------------------------------------------------- |
| name           | string  | 路径 | Excel 文档的名称。                                                                        |
| sheetName      | string  | 路径 | 工作表的名称。                                                                            |
| pictureIndex   | integer | 路径 | 图片的从零开始的索引。                                                                    |
| format         | string  | 查询 | 目标导出格式（例如：png、jpg、bmp、gif、tiff）。若省略此参数，则图片将以原始格式返回。     |
| folder         | string  | 查询 | 包含文档的文件夹路径。                                                                    |
| storageName    | string  | 查询 | 存储位置的名称。                                                                          |

### 错误响应

| HTTP 状态码 | 描述                                       |
| ----------- | ------------------------------------------ |
| 401         | 未授权 – 缺少或无效的令牌。                |
| 404         | 未找到 – 指定的文件、工作表或页边距索引不存在。 |
| 400         | 请求错误 – 请求语法错误或参数无效。         |
| 500         | 服务器内部错误 – 遇到意外情况。             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# 响应体中返回二进制图像数据（PNG）
# 示例：base64 编码片段
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 将处理底层细节，让您专注于项目本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}