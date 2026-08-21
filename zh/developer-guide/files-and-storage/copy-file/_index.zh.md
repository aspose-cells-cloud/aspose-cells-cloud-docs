---
title: "Aspose.Cells Cloud 文件复制 API — 用于在云端快速复制和批量操作 Excel 文件的接口"
secondtitle: "文档"
articletitle: "基于云端的 Excel 文件管理解决方案 — Aspose.Cells 复制文件 API 批量复制功能详解"
linktitle: "复制文件"
type: docs
url: /zh/copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel 文件复制, 云存储, REST API"
description: "了解如何使用 Aspose.Cells Cloud CopyFile API 高效地复制 Excel 文件，并在不同存储位置之间进行管理。"
weight: 100
---

**copyFile** API 允许用户将 Excel 文件从指定的源路径复制到目标路径，并支持多种存储选项。

## **Excel API：复制文件**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **安全与身份验证**

Aspose.Cells Cloud API 具有安全性，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **copyFile** API 的请求参数如下：

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                   |
| ---------------- | ------ | -------------------------- | -------------------------------------- |
| srcPath          | 字符串 | 路径（Path）               | 要复制的文件的源路径。                 |
| destPath         | 字符串 | 查询（Query）              | 文件将被保存到的目标路径。             |
| srcStorageName   | 字符串 | 查询（Query）              | 源存储的名称。                         |
| destStorageName  | 字符串 | 查询（Query）              | 目标存储的名称。                       |
| versionId        | 字符串 | 查询（Query）              | 可选参数，要复制的文件版本 ID。        |

### **响应**

操作成功时无内容返回。常见的 HTTP 状态码如下：

**HTTP 状态码**

| 状态码 | 含义              | 描述                                         |
| ------ | ----------------- | -------------------------------------------- |
| 200    | OK（成功）        | 筛选条件已成功应用；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺失或无效参数（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求实体过大） | 上传的文件大小超出限制。              |
| 500    | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                  |

## 如何结合 SDK 使用复制文件 API？

### 复制文件 API 规范

[复制文件 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) 提供了一个公开可访问的编程接口，可直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
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

使用 SDK 是开发效率最高的方式，因为它屏蔽了底层细节，使您能以最少的代码完成工作，例如将电子表格中的数据转换为图像。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：