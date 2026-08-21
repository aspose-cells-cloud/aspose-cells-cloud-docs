---
title: "Aspose.Cells Cloud – 删除文件 API"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud – 删除文件 API"
linktitle: "删除文件"
type: docs
url: /zh/delete-file/
keywords: "Aspose Cells, 删除文件 API, Excel 云存储, REST API, 文件管理"
description: "使用 RESTful 删除文件 API 从 Aspose.Cells Cloud 存储中删除 Excel 文件。包含端点、参数、身份验证和示例代码。"
weight: 100
---

**deleteFile** API 可从云存储中删除指定文件，帮助您高效地管理资源和数据。

## **Excel API：删除文件**

### Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名称      | 类型   | 位置 | 描述                                                                 |
| :------------ | :----- | :--- | :------------------------------------------------------------------- |
| `path`        | string | Path | 应删除文件的 URL 编码路径。                                         |
| `storageName` | string | Query| 文件所在的存储名称。若使用默认存储则可省略。                         |
| `versionId`   | string | Query| 要删除的特定文件版本标识符。若省略，则删除最新版本。                 |

### 响应描述

成功请求返回 **HTTP 200**，响应体为空。不返回 JSON 负载。

```json
{}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                             |
| ------ | -------------- | ------------------------------------------------ |
| 200    | OK（成功）     | 过滤器应用成功；响应包含操作详情。               |
| 400    | Bad Request    | 缺失或无效的参数（例如不支持的文件类型）。        |
| 401    | Unauthorized   | 无效或缺失 JWT 令牌。                            |
| 413    | Payload Too Large | 上传文件超过大小限制。                           |
| 500    | Internal Server Error | 服务器内部错误。                               |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 可管理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务。