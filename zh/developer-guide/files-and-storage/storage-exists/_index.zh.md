---
title: "检查存储是否存在 – Aspose.Cells Cloud API (v4.0)"
second_title: "文档"
ArticleTitle: "基于云的 Excel 文件管理 – 检查存储是否存在"
linktype: "docs"
url: /zh/storage-exists/
keywords: "Aspose.Cells, 存储是否存在, 云存储 API, REST, Excel"
description: "验证 Aspose.Cells Cloud 中存储容器是否存在。了解 GET /v4.0/cells/storage/{storageName}/exist 接口、所需参数、响应格式，并查看 C#、Java、Python 等语言的 SDK 示例。"
weight: 100
---

`storageExists` API 用于检查指定存储在 Aspose.Cells 云服务中是否存在。此功能对于确保依赖存储的所有操作能够无错误执行至关重要。

**摘要** – `storageExists` 接口可帮助您确认 Aspose.Cells Cloud 中特定存储容器是否可用。建议在执行文件相关操作前调用该接口，以避免运行时错误。

## 检查存储是否存在（storageExists）

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### 安全性与身份验证

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 位置 | 描述                             |
| ------------ | ------ | ---- | -------------------------------- |
| storageName  | 字符串 | 路径 | 要检查是否存在的存储名称。       |

### 响应

```json
{
  "Name": "StorageExist",
  "Description": ["指示指定存储是否存在。"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "指示存储是否存在。",
        "若存储存在则返回 true；否则返回 false。"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                   |
| ------ | -------------- | -------------------------------------- |
| 200    | 成功 (OK)      | 筛选条件应用成功；响应包含操作详情。   |
| 400    | 请求错误       | 缺少或无效参数（例如不支持的文件类型）。|
| 401    | 未授权         | JWT 令牌无效或缺失。                   |
| 413    | 请求实体过大   | 上传文件超出大小限制。                 |
| 500    | 服务器内部错误 | 发生意外服务器错误。                   |

## 如何使用 SDK 调用 storage exists API？

### OpenAPI 规范

<a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许开发者直接从 Web 浏览器无缝调用 REST API。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells 云服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最高效方式。SDK 封装了底层实现细节，使开发者能专注于项目任务本身。如需了解可用 Aspose.Cells Cloud SDK 的完整列表，请访问 <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">GitHub 仓库</a>。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 云服务 API：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}