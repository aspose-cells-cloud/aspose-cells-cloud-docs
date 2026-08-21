---
title: "ConvertWorksheetToPdf"
ArticleTitle: "将工作表转换为 PDF – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "ConvertWorksheetToPdf"
type: docs
url: /zh/cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, 将工作表转换为 PDF, API"
description: "使用 Aspose.Cells Cloud 将电子表格文件中的工作表转换为 PDF。"
weight: 10
---

## Aspose.Cells Cloud Web 服务的 ConvertWorksheetToPdf 方法

该方法从本地文件系统读取电子表格文件，将其工作表转换为 PDF 文件，并返回转换后的结果。必须正确指定源文件路径和目标格式。确保已具备读取源文件及必要时写入转换后文件的权限。转换过程完全在云端服务器上执行，无需使用云存储或进行外部下载。

主要功能包括：云原生转换、降低云资源负载、简化工作流。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### 安全性与身份验证

Aspose.Cells Cloud API 安全可靠，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                   |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | 上传电子表格文件。                                                                                                                     |
| worksheet        | String  | Query                       | 电子表格的工作表名称。                                                                                                                 |
| outPath          | String  | Query                       | （可选）工作簿的存储文件夹路径。默认为 null。                                                                                          |
| outStorageName   | String  | Query                       | 输出文件的存储名称。                                                                                                                   |
| fontsLocation    | String  | Query                       | 使用自定义字体。                                                                                                                       |
| AutoRowsFit      | Boolean | Query                       | （可选）自动调整工作表中所有行高。                                                                                                     |
| AutoColumnsFit   | Boolean | Query                       | （可选）自动调整工作表中所有列宽。                                                                                                     |
| region           | String  | Query                       | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式、日期解析和区域特定行为。                                                 |
| password         | String  | Query                       | 打开电子表格文件所需的密码。                                                                                                           |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| [待定]   |      |      |

### 响应

```json
{
  "file": "<生成的 PDF 的二进制流>"
}
```

**响应状态码**

| 状态码 | 含义       | 描述                                           |
|--------|------------|------------------------------------------------|
| 200    | 成功       | 工作表已成功转换为 PDF，并以文件流形式返回。   |
| 400    | 错误请求   | 请求参数无效或 URL 格式错误。                   |
| 401    | 未授权     | 身份验证失败或未提供凭据。                      |
| 404    | 未找到     | 无法访问源文件。                                |
| 413    | 请求实体过大 | 上传的文件超出允许的大小限制。                  |
| 500    | 内部服务器错误 | 转换过程中电子表格发生异常。                    |

## 如何使用 SDK 调用 ConvertWorksheetToPdf

### ConvertWorksheetToPdf 规范

[ConvertWorksheetToPdf API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) 定义了一个公开可访问的编程接口，使您能够直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=zh-CN&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<生成的 PDF 的二进制流>"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 抽象了底层细节，使您能够专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[待定]`
---