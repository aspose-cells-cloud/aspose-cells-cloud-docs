---
title: "创建文件夹 – Aspose.Cells Cloud API | Excel 存储管理"
second_title: "文档"
ArticleTitle: "创建文件夹 – Aspose.Cells Cloud API"
linktype: "docs"
url: /create-folder/
keywords: "Aspose.Cells, Cloud API, 创建文件夹, 存储管理, Excel"
description: "通过简单的 PUT 请求在 Aspose.Cells Cloud 存储中创建新文件夹。查看请求格式、参数、响应及错误处理方式。"
weight: 100
---

**createFolder** 操作可在 Excel API 使用的云存储中指定位置创建新文件夹。这对于组织文件和维护结构化的目录层级至关重要。

## **Excel API：创建文件夹**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### **createFolder** API 的请求参数如下：

| 参数名          | 类型   | 位置 | 是否必填 | 默认值 | 描述                                                  |
| --------------- | ------ | ---- | -------- | ------ | ----------------------------------------------------- |
| `path`          | 字符串 | 路径 | 是       | –      | 要创建的文件夹路径（例如：`myFolder/subFolder`）。   |
| `storageName`   | 字符串 | 查询 | 否       | –      | 要使用的存储名称；若省略，则使用默认存储。           |

### 响应说明

```json
{}
```

成功时该操作不返回任何内容。典型 HTTP 状态码如下：

**HTTP 状态码**

| HTTP 状态码 | HTTP 状态描述     | 描述                                      |
| ----------- | ----------------- | ----------------------------------------- |
| 200         | OK（成功）        | Web API 调用成功；响应包含操作详情。     |
| 400         | Bad Request（错误请求） | 缺少或无效参数（例如：不支持的文件类型）。 |
| 401         | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413         | Payload Too Large（请求实体过大） | 上传文件超出大小限制。               |
| 500         | Internal Server Error（服务器内部错误） | 服务器发生意外错误。              |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
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

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会管理底层细节，让您专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}