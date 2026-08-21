---
title: "将范围转换为 CSV"
ArticleTitle: "将范围转换为 CSV – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "将范围转换为 CSV"
type: docs
url: /cells/convert/range/csv
aliases: []
keywords: "转换, csv, 范围, Aspose.Cells"
description: "将本地磁盘上工作表中的指定范围转换为 CSV 文件。"
weight: 1
---

## Aspose.Cells Cloud Web 服务的将范围转换为 CSV 功能

此操作从本地文件系统读取电子表格文件，将指定范围转换为 CSV 格式，并直接返回转换结果。整个过程完全在云服务器上执行，因此无需将文件预先上传至云存储。API 支持可选参数，例如自定义字体、自动调整行/列宽、区域设置以及密码保护的工作簿。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
|------------------|---------|-----------------------------|----------------------------------------------------------------------|
| Spreadsheet      | 文件    | FormData                    | 上传电子表格文件。                                                   |
| worksheet        | 字符串  | 查询参数                    | 电子表格的工作表名称。**必填**。                                     |
| range            | 字符串  | 查询参数                    | 单元格区域，例如 `A1:C10`。**必填**。                                |
| outPath          | 字符串  | 查询参数                    | （可选）工作簿存储的文件夹路径，默认为 null。                        |
| outStorageName   | 字符串  | 查询参数                    | 输出文件的存储名称。                                                 |
| fontsLocation    | 字符串  | 查询参数                    | 使用自定义字体。                                                     |
| AutoRowsFit      | 布尔值  | 查询参数                    | （可选）自动调整工作表中所有行高。                                   |
| AutoColumnsFit   | 布尔值  | 查询参数                    | （可选）自动调整工作表中所有列宽。                                   |
| region           | 字符串  | 查询参数                    | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式化、日期解析及区域特定行为。 |
| password         | 字符串  | 查询参数                    | 打开电子表格文件所需的密码。                                         |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| 无       | N/A  | 无请求体参数。     |

### **响应**

```json
{
  "ResponseFile": "二进制文件流（CSV 内容）"
}
```

**响应状态码**

| 状态码 | 含义       | 描述                                       |
|--------|------------|--------------------------------------------|
| 200    | OK（成功） | 范围转换成功，CSV 文件返回于响应体中。     |
| 400    | 错误请求   | URL 无效或缺少必填参数。                   |
| 401    | 未授权     | 身份验证失败，或未提供凭据。               |
| 413    | 请求实体过大 | 请求体大小超过允许的上限。                |
| 500    | 内部服务器错误 | 电子表格在获取转换数据时发生异常。        |

## 如何使用 SDK 调用将范围转换为 CSV 功能

### 范围转换为 CSV 规范说明

[将范围转换为 CSV API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) 定义了公开可访问的编程接口，支持您直接通过网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=zh-CN&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64 编码的 CSV 内容"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务本身。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`