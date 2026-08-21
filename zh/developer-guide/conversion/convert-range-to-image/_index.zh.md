---
title: "将 Excel 区域转换为图像 – Aspose.Cells Cloud API"
description: "通过 Aspose.Cells Cloud REST API 将本地 Excel 文件中的指定区域转换为 PNG、JPEG、SVG、TIFF 或 BMP 格式图像——无需上传整个工作簿。"
keywords: "Aspose.Cells Cloud、将区域转换为图像、Excel API、图像格式、PNG、JPEG、SVG、TIFF、BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

该调用读取本地电子表格文件，转换指定区域，并以二进制流形式返回图像。

## 将区域转换为图像的方法

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

## 请求参数

| 名称               | 位置                              | 类型    | 必填项 | 描述                                                                 |
| ------------------ | --------------------------------- | ------- | ------ | -------------------------------------------------------------------- |
| **Spreadsheet**    | 表单数据 (`multipart/form-data`) | 文件    | 是     | 待处理的 Excel 文件。                                               |
| **worksheet**      | 查询参数                          | 字符串  | 是     | 包含目标区域的工作表名称（例如 `Sheet1`）。                         |
| **range**          | 查询参数                          | 字符串  | 是     | 待转换的单元格区域，例如 `A1:C10`。                                 |
| **format**         | 查询参数                          | 字符串  | 是     | 输出图像格式（`png`、`jpeg`、`svg`、`tiff`、`bmp`）。                |
| **printHeadings**  | 查询参数                          | 布尔值  | 否     | `true` 表示在图像中包含行/列标题。                                  |
| **outPath**        | 查询参数                          | 字符串  | 否     | 若需将生成的文件存储于云存储中，则指定其文件夹路径。                 |
| **outStorageName** | 查询参数                          | 字符串  | 否     | 存储服务的名称（例如 `MyStorage`）。                                 |
| **fontsLocation**  | 查询参数                          | 字符串  | 否     | 转换过程中使用的自定义字体的 URL 或路径。                            |
| **region**         | 查询参数                          | 字符串  | 否     | 区域标识符（例如 `en-US`、`fr-FR`），影响数字和日期的格式化方式。   |
| **password**       | 查询参数                          | 字符串  | 否     | 加密工作簿的密码。                                                   |
| **AutoRowsFit**    | 查询参数                          | 布尔值  | 否     | 渲染前自动调整行高。                                                 |
| **AutoColumnsFit** | 查询参数                          | 布尔值  | 否     | 渲染前自动调整列宽。                                                 |

## 响应

API 将转换后的 HTML 文件作为**二进制流**（`application/octet-stream`）返回。

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### 成功响应示例（HTTP）

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

将响应体保存为文件（例如 `report.png`），即可在浏览器中查看渲染后的图像。

---

**HTTP 状态码说明**

| 状态码 | 含义             | 描述                                         |
| ------ | ---------------- | -------------------------------------------- |
| 200    | OK（成功）       | 过滤器已成功应用；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                    |
| 500    | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                         |

## 如何使用 SDK 调用“将区域转换为图像” API？

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) 提供了一个公开可访问的 API，允许直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快的开发方式，因为它抽象了底层细节，使您能以极少的代码将数据区域转换为图像文件。  
请在我们的 [GitHub 仓库](https://github.com/aspose-cells-cloud) 中查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务。如果 Gist 加载被阻止，您可以直接从仓库下载示例文件。