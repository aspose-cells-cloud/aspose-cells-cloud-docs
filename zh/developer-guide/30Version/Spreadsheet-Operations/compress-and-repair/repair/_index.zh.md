---
title: "修复 Excel 文件"
second_title: "文档"
type: docs
linktitle: "修复 Excel 文件"
url: /zh/repair-excel-files/
keywords: "Aspose Cells, Excel 修复 API, 修复损坏的 XLSX, 电子表格恢复, 云 API"
description: "使用 Aspose.Cells Cloud REST API 修复损坏的 Excel 文件（XLS、XLSX、XLSM、XLSB、ODS）。上传一个或多个文件，选择输出格式，并以 Base64 编码形式接收修复后的文件。无需安装。"
weight: 39
---

此 REST API 允许您**修复** Excel 文件。

- 修复 XLS、XLSX、XLSM、XLSB、ODS 及其他电子表格格式。  
- 支持在单次请求中上传多个文件。

Aspose.Cells Cloud Excel 修复功能可在无需安装任何软件的情况下，在线从损坏的 Excel 文件中恢复数据。损坏的 Excel 文件难以打开，您可尝试使用 Aspose.Cells Cloud Excel 修复应用来恢复此类文件中的数据。

## REST API

**修复 Excel 文件** 端点用于修复损坏的电子表格文件，并返回修复后的内容。

```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型   | 位置                     | 描述 |
|----------|--------|--------------------------|------|
| file     | file   | formData (multipart)     | 待上传的文件 |
| format   | string | query                    | 所需的输出格式。若未指定（null），则默认输出格式与输入文件格式相同。 |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[合并后的文件名]",
    "Filesize" : [文件大小],
    "FileContent" : "[Base64字符串]"
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                   |
|--------|------------------|----------------------------------------|
| 200    | OK（成功）       | 修复操作成功；响应包含操作详情。        |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 发生意外的服务器端错误。           |

## 如何使用 SDK 调用 PostRepair API

### PostRepair API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64字符串--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64字符串--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

成功时，服务返回 HTTP 200 状态码，并附带 JSON 负载，其中包含 `Files` 数组。发生错误时，API 使用标准 HTTP 状态码：

- **400 Bad Request（错误请求）** — 参数无效或文件无法修复。  
- **401 Unauthorized（未授权）** — JWT 令牌缺失或无效。  
- **413 Payload Too Large（请求实体过大）** — 上传文件超出允许大小。  
- **500 Internal Server Error（内部服务器错误）** — 发生意外的服务器端故障。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}