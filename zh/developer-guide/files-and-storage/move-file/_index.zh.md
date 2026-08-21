---
title: "Aspose.Cells Cloud 移动文件 API – 云端文件快速移动接口"
second_title: "文档"
ArticleTitle: "基于云端的 Excel 文件高效管理解决方案 —— 云端文件快速移动接口"
linktype: "move-file"
type: docs
url: /move-file/
keywords: "Aspose.Cells, 移动文件 API, 云存储, Excel API, 文件管理"
description: "如何使用 Aspose.Cells Cloud v4.0 移动文件 API 在云存储中移动文件 —— 接口端点、参数说明、示例及 SDK 链接。"
weight: 100
---

**moveFile** API 用于在 Aspose.Cells Cloud 存储中将文件从一个位置移动到另一个位置，帮助您高效组织文件并管理存储空间。

## **Excel API：移动文件**

### Web API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **moveFile** API 的请求参数如下：

| 参数名称          | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                      |
| ----------------- | ------ | --------------------------- | ----------------------------------------- |
| srcPath           | String | Path                        | 待移动文件的源路径。                      |
| destPath          | String | Query                       | 文件将被移动到的目标路径。                |
| srcStorageName    | String | Query                       | 源存储名称（如适用）。                    |
| destStorageName   | String | Query                       | 目标存储名称（如适用）。                  |
| versionId         | String | Query                       | 文件版本 ID（如适用）。                   |

### **响应**

成功请求将返回 **HTTP 200 OK**，响应体为空的 JSON 对象。

```json
{}
```

**HTTP 状态码**

| HTTP 状态码 | HTTP 状态描述        | 描述                                       |
|-------------|----------------------|--------------------------------------------|
| 200         | OK（成功）           | Web API 调用成功；响应包含操作详情。       |
| 400         | Bad Request（错误请求） | 缺失或无效参数（例如不支持的文件类型）。   |
| 401         | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413         | Payload Too Large（载荷过大） | 上传文件超过大小限制。                   |
| 500         | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                   |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/MoveFile) 定义了公开可访问的编程接口，支持您直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

使用 SDK 是加速开发进程的最佳方式。SDK 负责处理底层细节，让您专注于项目任务本身。请查看 [GitHub 代码仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：