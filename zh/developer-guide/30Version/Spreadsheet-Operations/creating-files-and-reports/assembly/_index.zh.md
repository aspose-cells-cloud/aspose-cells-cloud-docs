---
title: "组装数据以创建 Excel 报表"
second_title: "文档"
linktitle: "组装数据"
type: docs
url: /zh/assembly-data-for-the-creation-of-an-excel-report/
aliases: [  /zh/assembly/ ]
keywords: "Aspose.Cells, Excel 报表, 数据组装, 云 API, REST, SDK, cURL, PDF, ODS"
description: "了解如何使用 Aspose.Cells Cloud 的 Assembly API 将数据合并到 Excel（XLSX、PDF、ODS）报表中。内容包括端点、参数、cURL 示例代码、SDK 代码、认证指南及错误处理。"
weight: 40
---

此 REST API 可将数据**组装到** Excel 文件中。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **安全性与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数


| 参数名         | 类型   | 位置                    | 描述                                               |
| -------------- | ------ | ----------------------- | -------------------------------------------------- |
| file           | file   | formData (multipart body) | 要上传的电子表格文件。                             |
| DataSource     | string | query string            | 提供组装所需数据的数据源标识符。                   |
| format         | string | query string            | 所需输出格式（例如：`xlsx`、`pdf`）。              |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[file2 name]",
    "Filesize" : [file size],
    "FileContent" : "[Base64String]"
}
```

**HTTP 状态码**

| 状态码 | 含义            | 描述                                           |
|--------|-----------------|----------------------------------------------|
| 200    | OK（成功）       | 成功应用筛选；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如：不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                          |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                           |

## 如何结合 SDK 使用 PostAssemble API

### PostAssemble API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是对接 API 的最快开发方式。SDK 抽象了底层细节，让您专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}