---
title: "将 Excel 工作簿拆分为多个文件"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将 Excel 工作簿拆分为多个文件"
second_title: "文档"
linktitle: "拆分 Excel 文件"
type: docs
url: /zh/split-multi-excel-files/
aliases: [  /zh/split/multi-files/ ]
keywords: "Excel, Aspose.Cells Cloud, REST API, 拆分工作簿, 多个文件, JPEG, PNG, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API 支持将 Excel 工作簿拆分为多种格式的多个文件。本文档提供了请求参数说明、cURL 示例以及适用于 C#、Java、PHP、Ruby、Node.js、Python、Perl 和 Go 等语言的 SDK 代码示例。"
weight: 130
---

此 REST API 可将 Excel **工作簿** 拆分为多种格式的多个文件。

> **前提条件** – 使用本 API 前，您必须获取有效的 JWT 令牌，确保使用受支持的 SDK 版本，并确认您的工作簿已存储于支持的存储位置。此外，API 还实施了平台指南中说明的文件大小限制。

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名               | 类型    | 位置       | 描述                                                                                     | 必填 |
| -------------------- | ------- | ---------- | ---------------------------------------------------------------------------------------- | ---- |
| files[]              | file    | formData   | 待拆分的一个或多个 Excel 工作簿。请求中请使用 `file1`、`file2` 等命名。                 | 是   |
| format               | string  | Query      | 拆分后文件的目标输出格式。                                                               | 否   |
| from                 | integer | Query      | 起始工作表索引。                                                                         | 否   |
| to                   | integer | Query      | 结束工作表索引。                                                                         | 否   |
| horizontalResolution | integer | Query      | 图像水平分辨率。                                                                         | 否   |
| verticalResolution   | integer | Query      | 图像垂直分辨率。                                                                         | 否   |
| outFolder            | string  | Query      | 拆分文件的输出文件夹。                                                                   | 否   |
| splitNameRule        | string  | Query      | 应用于拆分文件的命名规则。                                                               | 否   |
| folder               | string  | Query      | 原始工作簿所在文件夹。                                                                   | 否   |
| storageName          | string  | Query      | 要使用的存储名称。                                                                       | 否   |

### **响应**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[file1 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file2 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file3 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**HTTP 状态码**

| 状态码 | 含义                | 描述                                         |
|--------|---------------------|----------------------------------------------|
| 200    | OK（成功）          | 过滤器应用成功；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 缺失或无效参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                       |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何结合 SDK 使用 PostWorkbookSplit API

### PostWorkbookSplit API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit)定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 将处理底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}