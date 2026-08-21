---
title: "使用 Smart Marker 模板构建 Excel 报表"
second_title: "文档"
linktype: "SmartMarker"
type: docs
url: /zh/build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker（智能标记）, Aspose.Cells Cloud, REST API, 工作簿, SDK, API, 报表生成"
description: "了解如何使用 Aspose.Cells Cloud REST API 从 Smart Marker 模板生成 Excel 工作簿。内容包括请求/响应详情、cURL 示例、前置条件、注意事项以及 SDK 代码示例。"
weight: 40
ArticleTitle: "使用 Smart Marker 模板构建 Excel 报表 —— Aspose.Cells Cloud API 指南"
---

此 REST API 使用 Smart Marker 模板创建工作簿。

## 工作簿 SmartMarker API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **安全与认证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### **什么是 Smart Marker（智能标记）？**

Smart Marker（智能标记）是一种占位符语法，用于将 XML（或 JSON）文件中的数据字段映射到 Excel 模板中的单元格。在运行时，Aspose.Cells 会将这些标记替换为对应的数据，从而实现以编程方式生成完整填充的报表。

### **查询参数**

| 参数名称 | 类型   | 描述                                           |
| -------- | ------ | ---------------------------------------------- |
| outPath  | string | 生成的工作簿将被保存的目标路径。               |
| folder   | string | 包含原始工作簿的文件夹。                       |
| storageName | string | 要使用的存储服务名称。                         |

### **请求体参数**

| 参数名称 | 类型 | 描述                                         |
| -------- | ---- | -------------------------------------------- |
| xmlFile  | file | 随请求一起上传的 Smart Marker XML 数据文件。 |

### **响应**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**注意事项 / 限制：**  
- 该 API 仅支持最大 **50 MB** 的 Excel 文件。  
- 仅支持 **.xlsx**、**.xlsm** 和 **.xlsb** 格式。  
- 每个账户的速率限制为 **每秒 20 个请求**。

**HTTP 状态码**

| 状态码 | 含义           | 描述                                               |
| ------ | -------------- | -------------------------------------------------- |
| 200    | OK（成功）     | 成功应用筛选；响应包含操作详情。                   |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如，不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                            |
| 500    | Internal Server Error（内部服务器错误） | 服务器端意外错误。                               |

## 如何使用工作簿 SmartMarker API

### 工作簿 SmartMarker API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult)定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

**快速单行示例**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **错误处理**

| HTTP 状态码 | 描述               | 典型原因                                           |
| ----------- | ------------------ | -------------------------------------------------- |
| 400         | Bad Request（错误请求） | 缺少模板、XML 格式错误或参数无效。                 |
| 401         | Unauthorized（未授权） | 无效或缺失的认证令牌。                             |
| 404         | Not Found（未找到） | 指定的工作簿或存储位置不存在。                     |
| 500         | Internal Server Error（内部服务器错误） | 服务器端意外失败。                               |

**错误响应示例（400）**

```json
{
  "Code": 400,
  "Message": "XML 数据文件缺失或格式错误。"
}
```

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}