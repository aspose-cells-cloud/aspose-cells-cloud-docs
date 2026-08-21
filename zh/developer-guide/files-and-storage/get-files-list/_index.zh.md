---
title: "Aspose.Cells Cloud API – 获取文件列表（文件夹内容）"
description: "从 Aspose.Cells Cloud 存储中的指定文件夹中检索文件和子文件夹列表。"
keywords:
  - Aspose.Cells
  - API
  - 获取文件列表
  - 云存储
  - Excel
  - REST
type: docs
weight: 100
---

**获取文件列表** 操作返回 Aspose.Cells Cloud 存储中指定文件夹内所存储的文件和子文件夹集合。  
这是浏览基于云的 Excel 工作簿、归档文件及其他受支持文件类型的主要入口点。

## Aspose.Cells Cloud API – 获取文件列表（文件夹内容）

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 名称             | 位置   | 类型    | 是否必需 | 描述                                                       |
| ---------------- | ------ | ------- | -------- | ---------------------------------------------------------- |
| **path**         | 路径   | 字符串  | 是       | 云存储中文件夹的路径。                                     |
| **storageName**  | 查询参数 | 字符串  | 否       | 要使用的存储名称；若省略，则使用默认存储。                |
| **pageSize**     | 查询参数 | 整数    | 否       | 每页返回的最大项数（默认值：100）。                        |
| **pageNumber**   | 查询参数 | 整数    | 否       | 要检索的页码（从 1 开始计数，默认值：1）。                 |

- **Value** – `StorageFile` 对象数组。每个对象包含以下字段：
  - `Name` – 文件或文件夹名称。
  - `IsFolder` – 若该项为文件夹，则值为 `true`。
  - `Size` – 大小（单位：字节）；文件夹大小始终为 `0`。
  - `ModifiedDate` – 最后修改时间（ISO 8601 格式）。

### **响应**

**HTTP 状态码**

| HTTP 状态码 | HTTP 状态             | 描述                                                   |
| ----------- | --------------------- | ------------------------------------------------------ |
| 200         | OK（成功）            | Web API 调用成功；响应中包含操作详情。                 |
| 400         | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。           |
| 401         | Unauthorized（未授权） | JWT 令牌无效或缺失。                                   |
| 413         | Payload Too Large（载荷过大） | 上传的文件超出大小限制。                             |
| 500         | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。                           |
|             |                       |                                                        |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您能够专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：