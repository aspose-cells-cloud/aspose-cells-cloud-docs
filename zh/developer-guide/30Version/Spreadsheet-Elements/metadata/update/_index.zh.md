---
title: "更新元数据"
second_title: "文档"
linktitle: "无需使用存储更新"
type: docs
url: /zh/metadata/update/
keywords: "元数据, Excel, Aspose.Cells Cloud, REST API, 更新, 电子表格"
description: "Aspose.Cells Cloud REST API 支持更新 Excel 文件中的元数据。它支持多种 SDK（C#、Java、Python、Ruby、Go 等），便于在各种编程语言中实现无缝集成。"
weight: 35
ArticleTitle: "更新元数据 – Aspose.Cells Cloud API 文档"
---

此 REST API 可用于更新多个 Excel 文件中的**元数据**。

**前提条件：**有效的 Aspose Cloud 账户、有效的 JWT 访问令牌，以及需上传的 Excel 文件。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

### 请求参数

| 参数名称           | 类型   | 位置         | 描述                                       |
| ------------------ | ------ | ------------ | ------------------------------------------ |
| file               | file   | formData     | 待上传的 Excel 文件。                      |
| DocumentProperties | object | HTTP 请求体（JSON） | 要为 Excel 文件设置的文档属性。             |

**说明：**单次请求最多可上传 10 个文件。支持的格式包括 `.xlsx`、`.xls` 和 `.csv`。请求总大小不得超过 100 MB。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PostMetadata) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

该请求需在 **Authorization** 请求头中提供 Bearer JWT 令牌。请确保该令牌是使用您的 Aspose Cloud 客户端凭据生成的。

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您能够专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅：**  
- [获取元数据](/metadata/get/)  
- [删除元数据](/metadata/delete/)  
---