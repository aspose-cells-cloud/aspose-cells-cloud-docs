---
title: "在 Excel 文件中添加图片"
second_title: "文档"
linktype: "添加"
type: docs
url: /pictures/add/
aliases: [/add-pictures-to-excel-worksheet/]
keywords: "Aspose.Cells, Excel, 添加图片, REST API"
description: "使用 Aspose.Cells Cloud REST API 将图像添加到 Excel 工作表。适用于 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift 的 SDK 简化了跨平台集成。"
weight: 20
ArticleTitle: "向 Excel 工作表添加图片 – Aspose.Cells Cloud API"
---

此 REST API 可向 Excel 工作表添加新图片。  
**前置条件：** 您必须拥有有效的 Aspose Cloud 认证令牌、存储于受支持存储中的现有工作簿，以及修改该工作表的相应权限。

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称          | 类型     | 位置   | 描述                                                                                     |
| ----------------- | -------- | ------ | ---------------------------------------------------------------------------------------- |
| name              | string   | path   | 工作簿名称。                                                                             |
| sheetName         | string   | path   | 工作表名称。                                                                             |
| picture           | object   | body   | 图片对象（二进制数据）。                                                                 |
| upperLeftRow      | integer  | query  | 图片左上角所在行的从零开始索引。                                                         |
| upperLeftColumn   | integer  | query  | 图片左上角所在列的从零开始索引。                                                         |
| lowerRightRow     | integer  | query  | 图片区域右下角所在行的从零开始索引。                                                     |
| lowerRightColumn  | integer  | query  | 图片区域右下角所在列的从零开始索引。                                                     |
| picturePath       | string   | query  | 图片文件路径；若省略，则图片数据必须在请求体中提供。                                     |
| folder            | string   | query  | 包含工作簿的文件夹。                                                                     |
| storageName       | string   | query  | 存储服务的名称。                                                                         |

**请求体说明：** 当省略 `picturePath` 时，请通过 `multipart/form-data` 格式将二进制图像数据发送至请求体。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                               |
| ------ | ---------------- | -------------------------------------------------- |
| 200    | OK（成功）       | 筛选器已成功应用；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺失或无效参数（例如，不支持的文件类型）。       |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                         |

**示例 200 响应模式**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**说明：** 图片最大尺寸为 10 MB；超过此限制的文件将被拒绝，并返回 `400 Bad Request` 响应。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
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
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能够专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**说明：** 支持的图片格式包括 PNG、JPEG、BMP 和 GIF。图片最大尺寸为 10 MB；超过此限制的文件将被拒绝，并返回 `400 Bad Request` 响应。