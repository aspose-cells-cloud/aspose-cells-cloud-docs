---
title: "Aspose.Cells Cloud 文件夹复制 API —— 快速在云端复制文件夹"
second_title: "文档"
ArticleTitle: "基于云端的 Excel 文件管理解决方案 —— Aspose.Cells 复制文件夹 API 批量复制功能详解"
linktype: "docs"
url: /zh/copy-folder/
keywords: "复制文件夹, Aspose.Cells Cloud, REST API, 云存储, 电子表格管理"
description: "了解如何通过一次 REST 调用在 Aspose.Cells Cloud 存储中复制文件夹。内容包含接口端点、参数说明、示例请求、错误码及 SDK 示例代码。"
weight: 100
---

**CopyFolder** API 可将 Aspose.Cells Cloud 存储中的现有文件夹进行复制。该功能可用于创建备份、重新组织数据，或在不手动移动文件的前提下为后续处理准备文件夹层级结构。

## **Excel API：复制文件夹**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### CopyFolder API 接受以下参数

| 参数名称          | 是否必填 | 类型   | 位置（路径/查询） | 描述                                                               |
| ----------------- | -------- | ------ | ----------------- | ------------------------------------------------------------------ |
| `srcPath`         | 是       | 字符串 | 路径              | 待复制的源文件夹路径。                                             |
| `destPath`        | 是       | 字符串 | 查询参数          | 新建文件夹的目标路径。                                             |
| `srcStorageName`  | 否       | 字符串 | 查询参数          | 包含源文件夹的存储空间名称。                                       |
| `destStorageName` | 否       | 字符串 | 查询参数          | 文件夹应被复制到的目标存储空间名称。                               |

### 示例响应

成功调用将返回 **HTTP 200** 状态码，并附带空 JSON 正文：

```json
{}
```

**示例 cURL 请求**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP 状态码**

| 状态码 | 含义         | 描述                                           |
| ------ | ------------ | ---------------------------------------------- |
| 200  | OK（成功）   | 操作成功执行；响应包含操作详情。               |
| 400  | Bad Request  | 参数缺失或无效（例如不支持的文件类型）。       |
| 401  | Unauthorized | JWT 令牌无效或缺失。                           |
| 413  | Payload Too Large | 上传文件超出大小限制。                     |
| 500  | Internal Server Error | 服务器内部错误。                          |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

使用 SDK 是加速开发进程的最佳方式。SDK 将处理底层细节，使您能够专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}