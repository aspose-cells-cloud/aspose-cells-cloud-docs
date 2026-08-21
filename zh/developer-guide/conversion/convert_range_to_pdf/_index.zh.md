---
title: "ConvertRangeToPdf"
ArticleTitle: "将范围转换为 PDF – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "ConvertRangeToPdf"
type: docs
url: /zh/cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, 将范围转换为 PDF, API"
description: "使用 Aspose.Cells Cloud 将电子表格的指定范围转换为 PDF。"
weight: 1
---

## Aspose.Cells Cloud Web 服务的 ConvertRangeToPdf 功能

将本地驱动器上的电子表格指定范围转换为 PDF 文件。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                         |
|------------------|--------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件   | FormData                   | 上传电子表格文件。                                                                                                                           |
| worksheet        | 字符串 | 查询字符串                 | 电子表格的工作表名称。                                                                                                                       |
| range            | 字符串 | 查询字符串                 | 单元格区域，例如 A1:C10                                                                                                                      |
| outPath          | 字符串 | 查询字符串                 | （可选）工作簿所在的文件夹路径。默认为 null。                                                                                                |
| outStorageName   | 字符串 | 查询字符串                 | 输出文件的存储名称。                                                                                                                         |
| fontsLocation    | 字符串 | 查询字符串                 | 使用自定义字体。                                                                                                                             |
| AutoRowsFit      | 布尔值 | 查询字符串                 | （可选）自动调整工作表中所有行高。                                                                                                           |
| AutoColumnsFit   | 布尔值 | 查询字符串                 | （可选）自动调整工作表中所有列宽。                                                                                                           |
| region           | 字符串 | 查询字符串                 | 电子表格的区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式、日期解析和区域性特有行为。                                                    |
| password         | 字符串 | 查询字符串                 | 打开电子表格文件所需的密码。                                                                                                                 |

### 请求体参数

| 参数名称    | 类型 | 描述             |
|-------------|------|------------------|
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "file": "<二进制 PDF 内容>"
}
```

**响应状态码**

| 状态码 | 含义                  | 描述                                     |
|--------|-----------------------|------------------------------------------|
| 200    | 成功（OK）            | 转换成功；返回生成的 PDF 文件流。         |
| 400    | 请求无效（Bad Request） | URL 无效。                               |
| 401    | 未授权（Unauthorized）  | 身份验证失败，或未提供凭据。              |
| 413    | 请求实体过大（Payload Too Large） | 上传的文件大小超出允许限制。             |
| 500    | 内部服务器错误（Internal Server Error） | 电子表格在获取转换数据时发生异常。 |

## 如何使用 SDK 调用 ConvertRangeToPdf

### ConvertRangeToPdf 规范

[ConvertRangeToPdf API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 保证安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<二进制 PDF 内容>"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：

```csharp
// C# 的 SDK 示例代码
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Java 的 SDK 示例代码
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python 的 SDK 示例代码
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// JavaScript/Node.js 的 SDK 示例代码
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---