---
title: "为工作簿添加背景图片"
second_title: "文档"
linktitle: "添加"
type: docs
url: /zh/add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, 添加背景图片, Excel API, REST, 云 SDK, cURL, 工作簿背景"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作簿添加背景图片。包含所需参数、身份验证详情、完整的 cURL 示例以及错误处理信息。"
weight: 160
---

## REST API

此 REST API 可为 Excel 工作簿添加**背景图片**。

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 查询参数

| 参数名称       | 类型   | 描述                                       |
| -------------- | ------ | ------------------------------------------ |
| `picPath`      | string | 用作背景的图片文件路径。                   |
| `folder`       | string | 包含原始工作簿的文件夹。                   |
| `storageName`  | string | 文件所在的存储空间名称。                   |

### 请求体参数

| 参数名称 | 类型 | 描述                                       |
| -------- | ---- | ------------------------------------------ |
| `datafile` | file | 将应用背景图的工作簿文件。                 |

**路径参数** – URL 中的 `{name}` 表示**工作簿文件名**（例如：`Book1.xlsx`）。

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                           |
|--------|--------------------|------------------------------------------------|
| 200    | OK（请求成功）     | 背景图成功应用；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。                         |

## 如何使用 PutWorkbookBackground API（通过 SDK）

### PutWorkbookBackground API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器发起 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了完整的请求过程，包括多部分文件上传标志及必需的身份验证请求头。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式。SDK 将底层细节抽象化，让您专注业务逻辑。查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

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