---
title: "无需使用存储导入数据 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "无需存储导入数据"
type: docs
url: /zh/import/without-using-storage/
aliases: [  /zh/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, 云 API, 无需存储导入数据, Excel 导入 API, REST 导入"
description: "了解如何使用 Aspose.Cells Cloud API 将数据导入 Excel 工作簿而无需使用存储。包含请求格式、参数、cURL 示例、SDK 代码及错误处理。"
weight: 10
ArticleTitle: "无需使用存储导入数据 – Aspose.Cells Cloud API"
---

Excel 数据导入可能较为复杂，因为多种因素会影响最终结果。在**导入**过程中，所有这些因素都应被考虑在内。Aspose.Cells Cloud 可轻松将多种格式和数据类型导入 Excel 文件，并确保专业级质量。

此 REST API 可将**数据**导入 Excel 文件。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称       | 类型          | 位置       | 描述                                                                                                                                     |
| -------------- | ------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| file           | 文件          | formData   | 待上传的 Excel 文件。                                                                                                                   |
| ImportOption   | ImportOption  | JSON 请求体 | JSON 对象，定义要导入的数据、其类型（如 `IntArray`、`DoubleArray`、`StringArray`）以及在工作表中的放置位置。                             |

**ImportOption** 参数的详细说明请参阅 **ImportData 选项参考** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter)。

**前提条件：**  
需预先生成有效的 JWT 令牌，且文件大小不得超过服务限制（通常为 100 MB）。支持的文件格式包括 XLS、XLSX、CSV 和 ODS。若偏好通过编程方式访问，请确保已安装相应 SDK。

### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义            | 描述                                     |
|--------|-----------------|------------------------------------------|
| 200    | OK（成功）      | 筛选器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。      |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                      |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                       |

**注意事项：**  
发送请求时，`-F` 标志会自动设置 `Content-Type: multipart/form-data` 请求头。对于大型负载，建议在导入前对数据进行压缩，并为临时性错误实现重试逻辑。

## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*`-F` 标志会自动设置 `Content-Type: multipart/form-data`。*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}