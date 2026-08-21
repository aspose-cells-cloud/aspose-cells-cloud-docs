---
title: "Aspose.Cells Cloud 获取文件版本 API — 快速检索文件版本历史记录"
second_title: "文档"
ArticleTitle: "基于云的 Excel 管理 — 在 Aspose.Cells Cloud 中快速检索文件版本历史记录"
linktitle: "获取文件版本"
type: docs
url: /zh/get-file-versions/
keywords: "Aspose Cells API，文件版本，电子表格版本控制，云存储 API，REST，Excel 文件历史记录"
description: "获取存储在 Aspose.Cells Cloud 中任意 Excel 文件的完整版本历史记录列表。支持存储位置选择、身份验证及详细错误代码说明。"
weight: 100
---

获取存储在 Aspose.Cells Cloud 中特定电子表格的完整版本记录列表。该端点使开发者能够跟踪变更、审计修改，并直接从云存储中实现版本控制工作流。

**GetFileVersions** API 可返回 Aspose.Cells Cloud 中指定电子表格的所有版本记录，帮助您为每个文件保留完整的变更历史记录。

## **Excel API：获取文件版本**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **GetFileVersions** API 的请求参数如下：

| 参数名称       | 类型   | 位置 | 描述                                                                   |
| -------------- | ------ | ---- | ---------------------------------------------------------------------- |
| `path`         | 字符串 | 路径 | **必填。** 需要检索版本的文件完整路径。                               |
| `storageName`  | 字符串 | 查询 | 可选。包含该文件的存储空间名称；若未指定，则使用默认存储空间。        |

### **响应**

```json
{
  "Name": "FileVersions",
  "Description": [
    "包含指定文档的文件版本列表。"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["文件版本详细信息的集合。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

成功时，API 返回 **HTTP 200 OK**，响应体为包含 `Value` 数组的 JSON 数据，数组中为文件版本对象（如上所示）。

**HTTP 状态码**

| 状态码 | 含义           | 描述                                   |
| ------ | -------------- | -------------------------------------- |
| 200    | OK（成功）     | 筛选成功；响应包含操作详细信息。       |
| 400    | Bad Request    | 缺少或参数无效（例如不支持的文件类型）。|
| 401    | Unauthorized   | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large | 上传文件超出大小限制。              |
| 500    | Internal Server Error | 服务器内部错误。                  |

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) 提供了完整的编程接口，可直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

利用 SDK 可简化开发流程，将底层复杂性抽象化，让开发者专注于核心功能。您可在 [GitHub 仓库](https://github.com/aspose-cells-cloud) 中查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何在多种编程语言中与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}