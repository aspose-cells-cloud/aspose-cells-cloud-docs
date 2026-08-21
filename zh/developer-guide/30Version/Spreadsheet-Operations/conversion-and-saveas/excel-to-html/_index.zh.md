---
title: 将 Excel 转换为 HTML  
description: 使用 Aspose.Cells Cloud API v3.0 将 Excel 工作簿转换为 HTML 文件。  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# 将 Excel 转换为 HTML  

Aspose.Cells Cloud 提供了一个功能强大的 REST 端点，可将 Excel 工作簿（XLS、XLSX、CSV 等）转换为 HTML 文档。该操作将返回一个 **FileInfo** 对象，其中包含生成的 HTML 文件（文件名、大小和 Base64 编码的内容）。

---

## 前提条件

| 要求 | 满足方式 |
|------|----------|
| **Aspose Cloud 账户** | 在 [aspose.cloud](https://www.aspose.cloud) 注册账户。 |
| **JWT 访问令牌** | 通过 OAuth 2.0 的 `POST /connect/token` 端点获取承载令牌（bearer token）。 |
| **存储（可选）** | 如果希望 API 从特定存储读取或写入文件，请先创建该存储（例如 Amazon S3、Azure Blob 或 Aspose Cloud 存储）。 |
| **cURL / SDK** | 任意支持 multipart/form-data 的 HTTP 客户端（如 cURL、Postman 或 Aspose.Cells SDK）。 |

---

## 身份验证

所有 Aspose.Cells Cloud 请求均需使用 **JWT 令牌身份验证**。

```http
Authorization: Bearer <access-token>
```

令牌必须包含在每个请求的 `Authorization` 请求头中。

---

## 端点

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **注意**：请求必须以 `multipart/form-data` 格式发送。Excel 文件必须作为 multipart 正文的第一个部分提供。

---

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌身份验证</a>。

## 请求参数  

### 查询参数  

| 名称 | 类型 | 必填 | 默认值 | 描述 |
|------|------|------|--------|------|
| `password` | string | 否 | – | 打开受保护工作簿所需的密码。 |
| `storageName` | string | 否 | – | 源文件所在存储的名称。 |
| `checkExcelRestriction` | boolean | 否 | `true` | 设置为 `true` 时，服务将验证 Excel 特定限制（例如受保护工作表）。 |
| `region` | string | 否 | – | 工作簿的区域设置（例如 `zh-CN`）。 |
| `FontsLocation` | string | 否 | – | 包含渲染所需自定义字体的文件夹 URL 或路径。 |

### 表单数据（multipart）  

| 名称 | 类型 | 必填 | 描述 |
|------|------|------|------|
| **File** | file | **是** | 要转换的 Excel 工作簿。必须作为 multipart 请求的第一个部分提供。 |

---

## 请求示例（cURL）

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## 成功响应  

**状态码：** `200 OK`

| 字段 | 类型 | 描述 |
|------|------|------|
| `Filename` | string | 生成的 HTML 文件名（例如 `example.html`）。 |
| `FileSize` | int | HTML 文件大小（单位：字节）。 |
| `FileContent` | string | Base64 编码的 HTML 内容。 |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

响应结构由 **FileInfo** 模型定义：[/cells/file-info](/cells/file-info/)。

---

## 错误响应  

| 状态码 | 含义 | 示例载荷 |
|--------|------|----------|
| `400` | 请求无效 – 缺少或无效的参数 | ```json { "Code": "BadRequest", "Message": "必须提供 'File' 部分。" } ``` |
| `401` | 未授权 – 无效或缺失的 JWT 令牌 | ```json { "Code": "InvalidToken", "Message": "访问令牌缺失或已过期。" } ``` |
| `404` | 未找到 – 在指定存储中未找到源文件 | ```json { "Code": "FileNotFound", "Message": "文件 'my.xlsx' 不存在于存储 'MyStorage' 中。" } ``` |
| `413` | 载荷过大 – 上传的文件超过允许的大小 | ```json { "Code": "RequestEntityTooLarge", "Message": "上传的文件超过 100 MB 限制。" } ``` |
| `429` | 请求过多 – 超出速率限制 | ```json { "Code": "TooManyRequests", "Message": "超出每分钟 60 次调用的速率限制。" } ``` |
| `500` | 服务器内部错误 – 意外服务器条件 | ```json { "Code": "InternalError", "Message": "发生意外错误。请稍后重试。" } ``` |

---

## 速率限制  

| 限制项 | 描述 |
|--------|------|
| **每账户每分钟 60 个请求**（默认） | 超出限制将返回 `429 Too Many Requests`。请调整客户端逻辑，或通过 Aspose Cloud 门户申请更高配额。 |

---

## SDK 支持  

Aspose 提供了针对多种编程语言的官方 SDK，封装了该端点的功能。以下示例展示了使用官方 SDK 实现相同转换的方式。

| 语言 | 示例 |
|------|------|
| C# | <details><summary>查看示例</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java | <details><summary>查看示例</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python | <details><summary>查看示例</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js | <details><summary>查看示例</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go | <details><summary>查看示例</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP | <details><summary>查看示例</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby | <details><summary>查看示例</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl | <details><summary>查看示例</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

有关支持的 SDK 完整列表和安装说明，请参阅 **Aspose.Cells Cloud SDKs** 仓库：<https://github.com/aspose-cells-cloud>。

---

## 相关端点  

| 端点 | 描述 |
|------|------|
| `POST /cells/{name}/saveAs` | 将现有 Excel 文件直接另存为 HTML（或其他格式）至存储中。 |
| `PUT /cells/convert` | 转换工作簿为 HTML 并提供额外的转换选项；结果将返回于响应体中。 |
| `GET /cells/{name}` | 检索已存储为 HTML（或其他格式）的工作簿，支持可选查询参数。 |

---

## 常见问题  

**问：** *调用 Excel 转 HTML 转换 API 时如何进行身份验证？*  
**答：** 在请求中包含 `Authorization: Bearer <access-token>` 请求头，令牌需从 OAuth 2.0 `/connect/token` 端点获取。

**问：** *`FileInfo` 响应包含哪些内容？*  
**答：** 三个字段：`Filename`（字符串）、`FileSize`（整数，单位：字节）和 `FileContent`（Base64 编码的 HTML 内容）。

**问：** *可能遇到哪些错误代码？*  
**答：** `400`（请求无效）、`401`（未授权）、`404`（文件未找到）、`413`（载荷过大）、`429`（请求过多）、`500`（服务器内部错误）。每种错误均返回包含 `Code` 和 `Message` 字段的 JSON 载荷。

**问：** *是否可以指定自定义字体位置？*  
**答：** 是的。使用 `FontsLocation` 查询参数指向包含所需字体的文件夹或 URL。

**问：** *此操作是否存在速率限制？*  
**答：** 默认限制为 **每账户每分钟 60 次调用**。超出限制将返回 `429 Too Many Requests`。

---

## JSON-LD 面包屑导航（结构化数据）

添加此代码块可提升 SEO，使搜索结果中显示富片段面包屑导航。

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "首页", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "开发者中心", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "转换", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel 转 HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## 变更日志  

| 版本 | 日期 | 变更内容 |
|------|------|----------|
| **v3.0** | 2024-10-01 | 初始公开发布 `PostConvertWorkbookToHtml`。 |
| **v3.1** | 2025-04-15 | 新增 `region` 和 `FontsLocation` 查询参数；更新错误载荷格式。 |
| **v3.2** | 2026-03-20 | 引入速率限制文档和示例错误响应。 |

--- 

*如需进一步帮助，请联系 Aspose 支持或访问官方 API 参考文档：* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---