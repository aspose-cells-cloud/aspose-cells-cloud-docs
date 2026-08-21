---
title: "保存 Excel 工作簿 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "另存为"
type: docs
url: /zh/save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, 另存为, PDF, CSV, JSON, Markdown, REST API"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 工作簿保存为 PDF、CSV、JSON、Markdown 等其他格式。"
weight: 30
---

此 REST API 允许您**将 Excel 文件保存为多种不同格式**。  
在调用此接口之前，请确保您已获取有效的 OAuth 2.0 访问令牌，并且源工作簿已存储在您的 Aspose Cloud 存储中。

**前置条件**  
1. 获取 JWT 访问令牌，并将其包含在每个请求的 `Authorization: Bearer <token>` 请求头中。  
2. 将源工作簿上传至 Aspose Cloud 存储（或确认其已存在）。  
3. 明确工作簿所在的存储名称及文件夹路径。

## PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### **路径参数**

| 参数名称 | 类型   | 描述                 |
| -------- | ------ | -------------------- |
| name     | string | Excel 文件的名称。   |

### **查询参数**

| 参数名称              | 类型   | 描述                                                                 |
| --------------------- | ------ | -------------------------------------------------------------------- |
| newfilename           | string | 保存文档的新文件名。                                                 |
| isAutoFitRows         | string | 若为 `true`，则自动调整工作簿中所有行高。默认值为 `false`。          |
| isAutoFitColumns      | string | 若为 `true`，则自动调整工作簿中所有列宽。默认值为 `false`。          |
| folder                | string | 包含原始工作簿的文件夹路径。                                         |
| storageName           | string | 源文件所在存储的名称。                                               |
| outStorageName        | string | 输出文件将被保存到的存储名称。                                       |
| checkExcelRestriction | bool   | 指定在修改单元格或相关对象时是否强制执行 Excel 限制。               |
| region                | string | 应用于工作簿的区域设置。                                             |
| pageWideFitOnPerSheet | bool   | 转换时将每张工作表的页面宽度适应到工作表宽度。                       |
| pageTallFitOnPerSheet | bool   | 转换时将每张工作表的页面高度适应到工作表高度。                       |
| sheetName             | string | 需要转换的工作表名称。                                               |
| pageIndex             | string | 指定工作表内需转换的页面索引（需配合 `sheetName` 使用）。            |
| onePagePerSheet       | bool   | 转换为 PDF 时，每张工作表生成一页。                                  |

### **请求体参数**

| 参数名称   | 类型   | 描述                                           |
| ---------- | ------ | ---------------------------------------------- |
| SaveOptions | object | 在 multipart 请求的第二部分中提供的保存选项。 |

**请求体示例（multipart 请求中的 JSON 部分）**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### 响应

API 返回一个 `SaveResponse` 对象。

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                   |
| ------ | ---------------- | -------------------------------------- |
| 200    | OK（成功）       | 过滤器成功应用；响应包含操作详情。     |
| 400    | Bad Request（错误请求） | 缺失或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                 |

## 如何结合 SDK 使用 PostWorkbookSaveAs API

### PostWorkbookSaveAs API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器执行 REST 交互。

您可使用 **cURL** 轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
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

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

有关其他转换场景，请参阅 [将 Excel 转换为 PDF](/zh/convert-excel-to-pdf/) 和 [将 Excel 导出为 CSV](/zh/export-excel-to-csv/) 指南。