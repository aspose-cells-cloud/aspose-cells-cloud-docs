---
title: "Aspose.Cells Cloud 文件上传 API —— 云中快速上传文件的接口"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud 文件上传 API —— 云中快速上传文件的接口"
linktype: "上传文件"
type: docs
url: /zh/upload-file/
keywords: "Aspose.Cells, 文件上传, Excel API, 云存储, REST API"
description: "使用 Aspose.Cells Cloud API 上传文件的指南，涵盖请求参数、HTTP 状态码、错误处理及代码示例。"
weight: 100
---

**uploadFile** API 允许开发者将文件直接上传至云存储，以便后续使用 Aspose.Cells 进行处理。

## **Aspose Cells API：上传文件**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **uploadFile API 的请求参数**

| 参数名称     | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| :----------- | :----- | :-------------------------- | :------------------------------------------------------------------- |
| UploadFiles  | 文件   | FormData                    | 将文件上传至云存储。                                                 |
| path         | 字符串 | 路径                        | 云存储中的目标路径；指定文件应上传到的位置。                         |
| storageName  | 字符串 | 查询字符串                  | 文件将被上传到的存储空间名称。                                       |

### **响应**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["文件上传结果"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["已上传文件的文件名列表"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["错误列表。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

该 API 返回以下 HTTP 状态码：

| 状态码                        | 描述                         |
| ----------------------------- | ---------------------------- |
| **200 OK**                    | 文件上传成功。               |
| **400 Bad Request**           | 请求参数无效或请求格式错误。 |
| **401 Unauthorized**          | 缺少或无效的身份验证令牌。   |
| **403 Forbidden**             | 对指定存储空间权限不足。     |
| **500 Internal Server Error** | 服务器内部意外错误。         |

## 如何结合 SDK 使用文件上传 API？

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/UploadFile) 提供了 API 的详细说明，开发者可直接通过网页浏览器与其交互。

开发者可使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

利用 SDK 可提升开发效率，其自动处理底层细节，使开发者能专注于项目核心任务。访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**另请参阅**

- [下载文件 API](/download-file/) —— 从云存储中检索文件。
- [复制文件 API](/copy-file/) —— 在云存储内复制文件。
- [删除文件 API](/delete-file/) —— 从云存储中删除文件。