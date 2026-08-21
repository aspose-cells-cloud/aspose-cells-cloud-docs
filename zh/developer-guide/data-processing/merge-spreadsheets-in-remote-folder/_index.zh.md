---
title: "合并远程文件夹中的匹配电子表格"
description: "将存储在 Aspose Cloud 存储中的电子表格文件合并为单个文件。支持 30 多种输出格式，例如 PDF、CSV、JSON、XLSX、ODS、XPS 等。"
keywords: "Aspose.Cells, 合并电子表格, 远程文件夹, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

将位于远程 Aspose Cloud 存储文件夹中的多个电子表格文件合并为单个输出文件。该操作完全在云端执行，无需将源文件下载到本地。支持超过 30 种输出格式（PDF、CSV、JSON、XLSX、ODS、XPS 等）。

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数 <a id="request-parameters"></a>

| 参数名称                | 类型    | 位置   | 是否必需 | 描述                                                                                     |
| ----------------------- | ------- | ------ | -------- | ---------------------------------------------------------------------------------------- |
| **folder**              | string  | query  | **是**   | 包含源电子表格文件的云存储文件夹。                                                       |
| **fileMatchExpression** | string  | query  | **是**   | 用于选择文件的模式（例如 `*report*.xlsx`）。支持通配符 `*` 和 `?`。                     |
| **outFormat**           | string  | query  | **是**   | 目标输出格式（`PDF`、`CSV`、`JSON`、`XLSX`、`ODS`、`XPS` 等）。                          |
| **mergeInOneSheet**     | boolean | query  | **是**   | `true` 表示将所有数据合并到一个工作表中；`false` 表示每个源文件单独生成一个工作表。    |
| **storageName**         | string  | query  | 否       | 自定义存储名称；若省略，则默认使用主存储。                                               |
| **outPath**             | string  | query  | 否       | 合并后文件的目标文件夹。若省略，则保存在源文件所在文件夹中。                             |
| **outStorageName**      | string  | query  | 否       | 合并后文件将被写入的存储名称。                                                           |
| **fontsLocation**       | string  | query  | 否       | 包含自定义字体的文件夹路径（导出 PDF 或图片时必需）。                                   |
| **region**              | string  | query  | 否       | 用于数字、日期和货币格式化的区域设置（例如 `zh-CN`、`en-US`、`de-DE`）。                 |
| **password**            | string  | query  | 否       | 打开受密码保护的源电子表格所需的密码。                                                   |

## 请求示例（cURL） <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **响应**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

该文件可直接从 `FileUrl` 下载，或保存至 `outPath` 指定的位置。

**成功响应详情**

| 状态码       | 内容类型                   | 描述                             |
| ------------ | -------------------------- | -------------------------------- |
| 200 OK       | `application/octet-stream` | 合并后工作簿文件的二进制流。     |
| 202 Accepted | `application/json`         | 包含 `FileUrl`、`FileName` 等信息的 JSON。 |

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
| ------ | ---------------- | ------------------------------------------ |
| 200    | OK               | 成功应用筛选条件；响应中包含操作详情。     |
| 400    | Bad Request      | 缺失或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized     | 无效或缺失的 JWT 令牌。                    |
| 413    | Payload Too Large| 上传文件大小超出限制。                     |
| 500    | Internal Server Error | 服务器内部意外错误。                  |

## 如何结合 SDK 使用合并电子表格 API

### OpenAPI 规范

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI 规范</a> 提供了该 API 的机器可读描述，便于直接进行 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 编码)",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式，因为它抽象了底层细节，您只需少量代码即可将数据导入电子表格工作表。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。