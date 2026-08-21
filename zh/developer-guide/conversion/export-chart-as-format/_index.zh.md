---
title: "导出 Excel 图表 – Aspose.Cells Cloud API"
second_title: "文档"
description: "通过单次 REST 调用，将存储于云端的 Excel 工作簿中的图表转换为 PDF、PNG、SVG 或其他格式。"
ArticleTitle: "如何将本地电子表格工作表转换为 PDF 文件：分步指南"
linktitle: "将工作表转换为 PDF"
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, 导出图表, API, PDF, PNG, SVG, Excel, REST, 云端转换"
weight: 100
---

将存储于 Aspose Cloud 存储空间中的工作簿内图表转换为其他文件格式（PDF、PNG、SVG 等），无需下载源文件。

## ExportChartAsFormat API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **安全与身份认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

### 📦 请求参数

| 参数名称           | 类型    | 位置   | 是否必填 | 描述                                                     |
| ------------------ | ------- | ------ | -------- | -------------------------------------------------------- |
| **name**           | 字符串  | 路径   | 是       | 工作簿文件名。                                           |
| **worksheet**      | 字符串  | 路径   | 是       | 包含图表的工作表名称。                                   |
| **chartIndex**     | 整数    | 路径   | 是       | 待导出图表的从零开始的索引。                             |
| **format**         | 字符串  | 查询   | 是       | 目标输出格式（例如：`png`、`pdf`、`svg`）。              |
| **folder**         | 字符串  | 查询   | 否       | 工作簿所在文件夹路径（默认：根目录）。                   |
| **storageName**    | 字符串  | 查询   | 否       | 自定义存储空间名称；省略则使用默认存储空间。             |
| **outPath**        | 字符串  | 查询   | 否       | 转换后文件的保存路径。                                   |
| **outStorageName** | 字符串  | 查询   | 否       | 输出文件使用的存储空间名称。                             |
| **fontsLocation**  | 字符串  | 查询   | 否       | 自定义字体所在文件夹路径。                               |
| **region**         | 字符串  | 查询   | 否       | 区域设置（例如：`zh-CN`、`en-US`、`fr-FR`）。            |
| **password**       | 字符串  | 查询   | 否       | 打开受保护工作簿所需的密码。                             |

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP 状态码**

| 状态码 | 含义            | 描述                                           |
| ------ | --------------- | ---------------------------------------------- |
| 200    | OK（成功）      | 操作成功执行；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺失或无效参数（例如：不支持的文件类型）。    |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                          |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                        |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何结合 SDK 使用“导出图表为指定格式”API？

### 导出图表为指定格式 API 规范

[“导出图表为指定格式”API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) 提供了公开可访问的编程接口，可直接通过 Web 浏览器发起 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[]（Base64 编码）",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您能以极简代码实现将电子表格数据导出为 PDF 文件。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：