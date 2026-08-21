---
title: "删除 Excel 工作表背景"
second_title: "文档"
linktitle: "删除"
type: docs
url: /zh/worksheets/background/delete/
aliases: [  /zh/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, 删除工作表背景, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "使用 Aspose.Cells Cloud REST API 删除 Excel 工作表的背景图像。支持的 SDK 包括 C#、Java、PHP、Ruby、Node.js、Python、Perl 和 Go。"
weight: 210
ArticleTitle: "使用 Aspose.Cells Cloud API 删除 Excel 工作表背景"
---

此 REST API 用于删除工作表的背景图像。

**前提条件：** 您必须已将工作簿存储在 Aspose Cloud 存储中，并持有有效的 JWT 访问令牌以完成身份验证。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **请求参数**

| 参数名称      | 类型   | 位置   | 描述                                   |
| ------------- | ------ | ------ | -------------------------------------- |
| name          | string | path   | Excel 文件的名称。                     |
| sheetName     | string | path   | 要删除背景的工作表名称。               |
| folder        | string | query  | 文件所在的存储文件夹。                 |
| storageName   | string | query  | 存储名称（若非默认存储）。             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。所有请求都需要有效的 JWT 令牌；您可按照[身份验证指南](https://docs.aspose.cloud/cells/getting-started/)中的说明，通过 OAuth2 令牌端点获取该令牌。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
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

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 成功应用筛选器；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                           |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}