---
title: "Aspose.Cells Cloud 下载文件 API —— 云端快速下载文件的接口"
second_title: "文档"
articleTitle: "Aspose.Cells Cloud 下载文件 API —— 云端快速下载文件的接口"
linkTitle: "下载文件 API"
type: docs
url: /zh/download-file/
keywords: "Aspose.Cells, 下载文件 API, Excel 云存储, REST API, 文件下载, PDF, CSV, SDK"
description: "使用下载文件 API（v4.0）从 Aspose.Cells Cloud 存储中下载 Excel、PDF、CSV 及其他格式的文件。内容包括端点、参数、认证详情及代码示例。"
weight: 100
---

**DownloadFile** API 可让您从 Aspose.Cells Cloud 存储中检索文件。下载文件 API 是直接从云端访问 Excel 工作表、PDF、CSV 及其他支持格式的关键工具。

## **Excel API：下载文件**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **DownloadFile** API 的请求参数如下：

| 参数名        | 类型   | 位置（路径 / 查询） | 描述                                                     |
| ------------- | ------ | ------------------- | -------------------------------------------------------- |
| path          | String | Path                | 要下载的文件在虚拟路径中的位置。                         |
| storageName   | String | Query               | 从中检索文件的存储空间名称。                             |
| versionId     | String | Query               | 待下载文件的版本标识符（如适用）。                       |

### **响应**

API 返回一个**二进制文件流**。`Content-Type` 响应头与文件格式一致（例如，XLSX 文件为 `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`）。不会返回 JSON 数据体。

**HTTP 状态码**

| 状态码 | 含义            | 描述                                         |
| ------ | --------------- | -------------------------------------------- |
| 200    | OK（成功）      | 过滤器应用成功；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如，不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（请求体过大） | 上传的文件超出大小限制。                    |
| 500    | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。                       |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) 定义了公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}