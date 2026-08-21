---
title: "Excel 转 JSON"
second_title: "文档"
linktitle: "Excel 转 JSON"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel 转 JSON, 云 API, 电子表格转换, REST API"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel 电子表格转换为 JSON 文件。包含 cURL 示例、SDK 代码片段（C#、Java、Python）、所需参数、身份验证和响应格式。"
weight: 100
ArticleTitle: "使用 Aspose.Cells Cloud API 将 Excel 转换为 JSON — 快速指南"
---


## REST API

此 REST API 将电子表格文件转换为 JSON 格式的文件。


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求

**查询参数**

| 参数名称                | 类型   | 描述                                                             |
| ----------------------- | ------ | ---------------------------------------------------------------- |
| `password`              | string | 打开 Excel 文件所需的密码（可选）。                             |
| `storageName`           | string | 文件所在存储空间的名称（可选）。                                 |
| `checkExcelRestriction` | bool   | 修改单元格时是否强制应用 Excel 特定限制（可选）。               |

**请求体参数**

| 参数名称 | 类型 | 描述                                                                                     |
| -------- | ---- | ---------------------------------------------------------------------------------------- |
| `datafile` | file | 待上传的 Excel 文件。必须作为 `multipart/form-data` 请求的第一部分发送。               |

#### 示例 cURL 调用

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### 响应

服务返回一个 **FileInfo** 对象。关键字段说明如下：

| 字段          | 类型    | 描述                                                                   |
| ------------- | ------- | ---------------------------------------------------------------------- |
| `Filename`    | string  | 生成的 JSON 文件名（例如 `myWorkbook.json`）。                         |
| `FileSize`    | integer | 生成文件的大小（单位：字节）。                                         |
| `FileContent` | string  | JSON 文件内容的 Base64 编码字符串。解码后可获取实际 JSON 内容。       |

**响应示例**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 字符串) ..."
}
```

#### 错误处理

若请求失败，API 将返回包含以下结构的错误对象：

| 字段      | 类型   | 描述                             |
| --------- | ------ | -------------------------------- |
| `Code`    | string | 机器可读的错误标识符。           |
| `Message` | string | 人类可读的错误描述。             |

常见 HTTP 状态码：

- **400** – 请求错误（例如，缺少文件、参数无效）。
- **401** – 未授权（访问令牌无效或缺失）。
- **500** – 服务器内部错误。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。             |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如，不支持的文件类型）。    |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                          |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                      |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                        |

## 如何使用 PostConvertWorkbookToJson API（配合 SDK）

### PostConvertWorkbookToJson API 规范

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI 规范 — 将工作簿转换为 JSON">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，让您能直接从 Web 浏览器发起 REST 请求。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 字符串)"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能专注于项目核心任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="GitHub 上的 Aspose.Cells Cloud SDK 列表">GitHub 仓库</a> 以获取完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现类似功能的其他 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 将 Excel 文件保存为 HTML 文件（支持额外设置），并将结果存储于指定存储空间中。
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 将 Excel 文件转换为 HTML 文件（支持额外设置），并将结果直接返回于响应中。
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – 获取 Excel 文件；可通过查询参数指定返回 HTML 格式。