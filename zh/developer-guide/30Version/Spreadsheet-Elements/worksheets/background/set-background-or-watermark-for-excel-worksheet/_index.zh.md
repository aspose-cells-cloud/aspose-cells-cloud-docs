---
title: "为 Excel 工作表设置背景"
ArticleTitle: "为 Excel 工作表设置背景 – Aspose.Cells Cloud API 指南"
second_title: "文档"
linktitle: "添加"
type: docs
url: /zh/worksheets/background/add/
aliases: [  /zh/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, 工作表, 背景, REST API, SDK, 添加图像"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表添加背景图像（PNG、JPEG、BMP）。包括端点、必需参数、认证步骤、cURL 示例及 SDK 代码示例。"
weight: 180
---

此 REST API 可为工作表添加背景图像。

## 安全性与认证
Aspose.Cells Cloud API 是安全的，需要采用 [JWT 令牌认证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **请求参数**

| 参数名         | 类型   | 位置   | 描述                                                     |
| -------------- | ------ | ------ | -------------------------------------------------------- |
| name           | string | path   | Excel 工作簿的名称。                                     |
| sheetName      | string | path   | 应用图像的工作表名称。                                   |
| imageFile      | file   | body   | 用作背景的二进制图像文件（PNG、JPEG、BMP 等）。          |
| folder         | string | query  | 工作簿所在的存储文件夹。                                 |
| storageName    | string | query  | Aspose Cloud 存储的名称。                                |

**支持的格式与限制**

- 接受的图像扩展名：**PNG、JPEG、BMP、GIF**。
- 最大文件大小：**5 MB**。
- 图像将平铺以填充整个工作表背景。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

_可能的错误响应_

| HTTP 状态码 | 描述                                         |
| ----------- | -------------------------------------------- |
| 400         | 请求错误 – 参数缺失或无效。                   |
| 401         | 未授权 – JWT 令牌无效或已过期。               |
| 404         | 未找到 – 工作簿或工作表不存在。               |
| 500         | 服务器内部错误 – 服务器上出现意外情况。       |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 可处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}