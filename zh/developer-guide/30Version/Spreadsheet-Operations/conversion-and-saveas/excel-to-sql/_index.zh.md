---
title: "Excel 转 SQL"
second_title: "文档"
linktitle: "Excel 转 SQL"
type: docs
url: /zh/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel 转 SQL, 云 API, 电子表格转换, REST"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 电子表格转换为 SQL 文件。支持多种 SDK 和编程语言，便于无缝集成到您的应用程序中。"
weight: 100
ArticleTitle: "将 Excel 转换为 SQL – Aspose.Cells Cloud API"
---

此 REST API 可将电子表格文件转换为 SQL 格式文件。

**前置条件**  
要使用此接口，您必须拥有一个有效的 JWT 令牌，其生成方式请参阅 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a> 指南。API 支持的 Excel 文件大小不超过服务文档中定义的限制，并且在提供 `password` 查询参数时可处理密码保护的工作簿。

## PostConvertWorkbookToSQL API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### **查询参数**

| 参数名称              | 类型   | 描述                                                           |
| --------------------- | ------ | -------------------------------------------------------------- |
| password              | string | 打开 Excel 文件所需的密码。                                    |
| storageName           | string | 存放文件的存储空间名称。                                       |
| checkExcelRestriction | bool   | 指示在修改单元格相关对象时是否检查 Excel 文件限制。           |

### **请求体参数**

| 参数名称 | 类型       | 描述                                                 |
| -------- | ---------- | ---------------------------------------------------- |
| datafile | data file  | 待转换的电子表格文件，作为请求的第一个部分包含在内。 |

### 响应

API 返回一个 **FileInfo** 对象，其中包含生成的 SQL 文件。

| 字段            | 类型   | 描述                                   |
| --------------- | ------ | -------------------------------------- |
| **Filename**    | string | SQL 文件名（例如 `example.sql`）。    |
| **FileSize**    | int    | 文件大小（单位：字节）。               |
| **FileContent** | string | SQL 文件内容（Base64 编码）。          |

[FileInfo](/cells/file-info/)

**HTTP 状态码**

| 状态码 | 含义         | 描述                                   |
|--------|--------------|----------------------------------------|
| 200    | OK（成功）   | 过滤器应用成功；响应包含操作详情。     |
| 400    | Bad Request  | 缺少或无效参数（例如不支持的文件类型）。|
| 401    | Unauthorized | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large | 上传文件超出大小限制。            |
| 500    | Internal Server Error | 服务器内部错误。                |

## 如何使用 SDK 调用 PostConvertWorkbookToSQL API

### PostConvertWorkbookToSQL API 规范

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 请求。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现此功能的其他 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 将工作簿保存为其他格式，并将结果存储在指定存储空间中。

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 将工作簿转换为另一种格式（支持可选设置），并将结果返回于响应中。

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – 获取工作簿（支持可选转换设置）。

**注意事项**  
- 转换密码保护的 Excel 文件时，请确保提供 `password` 查询参数；否则转换将失败，并返回 400 错误。  
- 服务返回的 SQL 文件内容为 Base64 编码格式，请在保存为 `.sql` 文件前进行解码。

**示例文件**  
点击此处下载示例 Excel 工作簿 [sample.xlsx](https://example.com/sample.xlsx)，以及预生成的 SQL 结果 [sample.sql](https://example.com/sample.sql)，以快速测试该 API。