---
title: "Aspose.Cells Cloud API – 获取磁盘使用情况 | 实时存储指标"
second_title: "文档"
ArticleTitle: "基于云端的 Excel 文件管理解决方案 – 快速检索云端磁盘使用情况的接口"
linktype: "获取磁盘使用情况"
type: docs
url: /zh/get-disk-usage/
keywords: "Aspose Cells, 云 API, 磁盘使用情况, 存储指标, Excel, REST"
description: "获取 Aspose.Cells Cloud 的实时磁盘使用情况。了解 GET /v4.0/cells/storage/disk 端点、所需的身份验证方式以及示例响应。"
weight: 100
---

**获取磁盘使用情况**操作返回您 Aspose.Cells Cloud 账户的实时存储指标。通过此端点可监控已用空间与总磁盘空间。

- 检索 Aspose Cloud 环境中 Excel API 的当前磁盘使用情况。
- 允许开发人员监控其应用程序所消耗的存储空间。
- 有助于主动管理存储限制并控制成本。

## Excel API：GetDiskUsage

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名         | 类型   | 位置   | 描述                               | 必填项 |
| -------------- | ------ | ------ | ---------------------------------- | ------ |
| storageName    | String | Query  | 要检索使用情况的存储空间名称。     | 可选   |

### **响应**

```json
{
  "Name": "DiskUsage",
  "Description": ["用于磁盘空间信息的类。"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["应用程序已使用的磁盘空间量。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["可用的总磁盘空间。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义         | 描述                                   |
| ------ | ------------ | -------------------------------------- |
| 200    | OK（成功）   | 过滤器应用成功；响应包含操作详情。     |
| 400    | Bad Request  | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large | 上传的文件超出大小限制。         |
| 500    | Internal Server Error | 服务器内部错误。               |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage)定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}