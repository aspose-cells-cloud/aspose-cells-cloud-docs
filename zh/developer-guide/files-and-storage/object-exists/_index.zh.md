---
title: "Object Exists API — 检查 Aspose.Cells Cloud 中文件/文件夹是否存在"
second_title: "文档"
ArticleTitle: "Object Exists API — 验证 Aspose.Cells Cloud 中文件或文件夹是否存在"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, 云存储, 对象是否存在, 文件存在性, 文件夹存在性, API"
description: "使用 Object Exists API 快速验证 Aspose.Cells Cloud 存储中是否存在特定文件或文件夹。支持可选的存储名称和版本 ID，且适用于启用了版本控制的对象。"
weight: 100
---

**Object Exists API** 可帮助开发者判断 Aspose.Cells Cloud 存储中是否存在指定的文件或文件夹。该 API 返回一个布尔值，表示对象是否存在，以及该路径是否指向一个文件夹。

## **Excel API：Object Exists**

### Web API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ 为存储中文件或文件夹的完整路径。

### **安全性与身份验证**

Aspose.Cells Cloud API 具备安全性，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名         | 类型   | 位置   | 必填 | 描述                                                           |
| -------------- | ------ | ------ | ---- | -------------------------------------------------------------- |
| `path`         | string | Path   | 是   | 文件或文件夹的完整路径。                                       |
| `storageName`  | string | Query  | 否   | 存储名称；若省略，默认使用主存储。                             |
| `versionId`    | string | Query  | 否   | 文件的特定版本标识符（若启用了版本控制功能）。                 |

**HTTP 状态码**

| HTTP 状态码 | HTTP 状态描述         | 描述                                                             |
| ----------- | --------------------- | ---------------------------------------------------------------- |
| 200         | OK（请求成功）        | Web API 调用成功；响应包含操作详情。                             |
| 400         | Bad Request（请求错误） | 参数缺失或无效（例如不支持的文件类型）。                         |
| 401         | Unauthorized（未授权）  | JWT 令牌无效或缺失。                                             |
| 413         | Payload Too Large（请求体过大） | 上传的文件超出大小限制。                                       |
| 500         | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                                         |

### **响应**

成功调用后返回如下 JSON 数据体，包含两个字段：

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** — 若文件或文件夹存在则为 `true`，否则为 `false`。
- **IsFolder** — 若路径指向文件夹则为 `true`，若指向文件则为 `false`。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) 定义了一个公开可访问的编程接口，支持您直接通过网页浏览器发起 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过多种 SDK 调用 Aspose.Cells Web 服务。若 Gist 未加载成功，各标签页下方均提供静态示例。