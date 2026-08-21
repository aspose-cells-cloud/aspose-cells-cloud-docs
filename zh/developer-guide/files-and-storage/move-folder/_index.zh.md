---
title: "Aspose.Cells Cloud 移动文件夹 API — 快速在云端移动文件夹"
second_title: "文档"
ArticleTitle: "基于云端的 Excel 文件管理 — 快速在云端移动文件夹"
linktitle: "移动文件夹"
type: docs
url: /move-folder/
keywords: "Aspose.Cells, 移动文件夹, 云存储, Excel API"
description: "了解如何通过 RESTful 移动文件夹 API，在 Aspose.Cells Cloud 存储中移动文件夹。内容包括端点、参数、示例 cURL 请求、错误代码以及 C#、Java、Python 等语言的 SDK 示例。"
weight: 100
---

该 API 可在 Aspose.Cells Cloud 存储内将文件夹从一个位置移动至另一位置，有助于对文件进行组织并高效管理云存储空间。

## **Excel API：移动文件夹**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**示例 cURL 请求**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **moveFolder** API 的请求参数如下：

| 参数名称         | 类型   | 位置   | 描述                                               |
| ---------------- | ------ | ------ | -------------------------------------------------- |
| srcPath          | string | Path   | 待移动文件夹的完整路径，例如 `FolderA/`。         |
| destPath         | string | Query  | 文件夹将被移至的目标路径，例如 `FolderB/`。       |
| srcStorageName   | string | Query  | （可选）源存储名称。                               |
| destStorageName  | string | Query  | （可选）目标存储名称。                             |

**参数说明**

- **srcPath** — 必填项。源文件夹路径。
- **destPath** — 必填项。目标文件夹路径。
- **srcStorageName** — 可选项。源存储的标识符。
- **destStorageName** — 可选项。目标存储的标识符。

### **响应**

成功时，API 返回空响应体，HTTP 状态码为 **200 OK**。错误将以包含 `error` 字段的 JSON 对象形式返回。

**HTTP 状态码**

| HTTP 状态码 | HTTP 状态描述        | 描述                                               |
| ----------- | -------------------- | -------------------------------------------------- |
| 200         | OK（成功）           | Web API 调用成功；响应包含操作详情。               |
| 400         | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。         |
| 401         | Unauthorized（未授权） | 无效或缺失的 JWT 令牌。                            |
| 413         | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                            |
| 500         | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                              |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) 定义了公开可访问的编程接口，支持您直接从网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

使用 SDK 是加速开发的最佳方式。SDK 将处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：