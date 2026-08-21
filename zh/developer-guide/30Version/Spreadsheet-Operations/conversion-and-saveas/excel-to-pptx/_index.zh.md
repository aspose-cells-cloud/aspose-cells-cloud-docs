---
title: "使用 Aspose.Cells Cloud API v3.0 将 Excel 转换为 PPTX"
second_title: "文档"
linktitle: "Excel 转 PPTX"
type: docs
url: /zh/convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, 转换, REST API, 云"
description: "了解如何使用 Aspose.Cells Cloud REST API v3.0 将 Excel 工作簿转换为 PPTX 演示文稿。包含 cURL 请求示例、SDK 代码示例、身份验证与错误处理方法。"
weight: 90
ArticleTitle: "使用 Aspose.Cells Cloud API v3.0 将 Excel 转换为 PPTX"
---

此 REST API 可将电子表格文件转换为 PPTX 格式。

## PostConvertWorkbookToPptx API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 查询参数

| 参数名称                | 类型   | 描述                                                         |
| ----------------------- | ------ | ------------------------------------------------------------ |
| `password`              | string | 打开 Excel 工作簿所需的密码。                                |
| `storageName`           | string | 源文件所在的存储名称。                                       |
| `checkExcelRestriction` | bool   | 指示在修改与单元格相关的对象时是否强制执行 Excel 文件限制。 |

### 请求体参数

| 参数名称   | 类型      | 描述                                       |
| ---------- | --------- | ------------------------------------------ |
| `datafile` | data file | 包含在多部分请求体第一部分中的 Excel 文件。 |

**示例多部分请求体（简化版）：**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<input.xlsx 的二进制内容>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### 响应

API 返回一个 **FileInfo** 对象，其中包含生成的 pptx 文件。

| 字段            | 类型   | 描述                             |
| --------------- | ------ | -------------------------------- |
| **Filename**    | string | pptx 文件名（例如 `example.pptx`）。 |
| **FileSize**    | int    | 文件大小（单位：字节）。         |
| **FileContent** | string | pptx 文件内容（Base64 编码）。   |

[FileInfo](/cells/file-info/)

**HTTP 状态码**

| 状态码 | 含义             | 描述                                               |
| ------ | ---------------- | -------------------------------------------------- |
| 200    | OK（成功）       | 筛选操作成功完成；响应中包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求实体过大） | 上传文件大小超过限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                         |

*说明：* 此端点支持常见的 Excel 格式（`.xlsx`、`.xls`、`.xlsm`）。最大文件大小限制为 50 MB。若工作簿包含宏或受保护工作表，而未提供相应参数，则转换可能受限。

## 如何使用 SDK 调用 PostConvertWorkbookToPptx API

### PostConvertWorkbookToPptx API 规范

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 抽象了底层细节，让您专注于项目本身。完整的 Aspose.Cells Cloud SDK 列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud" rel="noopener noreferrer")。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现此功能的其他 API

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – 将 Excel 文件转换为 PDF。
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – 将 Excel 文件转换为 PNG 图片。
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – 将 Excel 文件转换为 SVG 格式。