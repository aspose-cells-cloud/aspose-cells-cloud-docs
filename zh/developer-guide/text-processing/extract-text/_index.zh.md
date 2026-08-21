---
title: "Aspose.Cells Cloud Web API – 提取文本"
second_title: "Aspose.Cells Cloud – 在线短代码"
linktitle: "提取文本"
type: docs
url: /zh/extract-text/
keywords: "Aspose.Cells Cloud, 提取文本, Excel API, 单元格文本提取, REST API"
description: "使用 Aspose.Cells Cloud API 从 Excel 单元格中提取子字符串、数字或字符。支持基于前后文本、位置的提取，以及直接输出到新区域。"
weight: 100
ArticleTitle: "Aspose.Cells Cloud 提取文本 API 文档"
---

从电子表格单元格中提取子字符串、字符或数字，并写入另一单元格，无需使用复杂的 FIND、MIN、LEFT 或 RIGHT 公式。

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **extractText API 请求参数**

| 参数名称         | 类型    | 位置       | 描述                                                                                                                          |
| ---------------- | ------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件    | FormData   | 上传电子表格文件。                                                                                                            |
| extractTextType  | 字符串  | Query      | 枚举值，表示提取模式。允许值：`Before`、`After`、`BeforePosition`、`AfterPosition`。                                         |
| beforeText       | 字符串  | Query      | 提取子字符串前必须出现的文本。仅当 `extractTextType=Before` 时使用。                                                          |
| afterText        | 字符串  | Query      | 提取子字符串后必须出现的文本。仅当 `extractTextType=After` 时使用。                                                           |
| beforePosition   | 整数    | Query      | 从单元格左侧起返回的字符数。仅当 `extractTextType=BeforePosition` 时使用。                                                    |
| afterPosition    | 整数    | Query      | 从单元格右侧起返回的字符数。仅当 `extractTextType=AfterPosition` 时使用。                                                     |
| outPositionRange | 字符串  | Query      | 目标区域（例如 `Sheet1!A1`），用于写入提取出的文本。                                                                          |
| worksheet        | 字符串  | Query      | 包含源单元格的工作表名称。                                                                                                    |
| range            | 字符串  | Query      | 源单元格或区域（例如 `A1`）。                                                                                                  |
| outPath          | 字符串  | Query（可选） | 输出工作簿在存储中的文件夹路径。若省略，则结果将返回在响应体中。                                                               |
| outStorageName   | 字符串  | Query      | 用于输出文件的存储名称。                                                                                                      |
| region           | 字符串  | Query      | 电子表格区域设置（例如 `US`、`EU`）。                                                                                          |
| password         | 字符串  | Query      | 打开受保护工作簿所需的密码。                                                                                                  |

**示例 cURL 请求**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **响应**

请求成功时，API 返回一个 JSON 负载，包含提取出的文本及其写入的单元格地址：

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

若提供了 `outPath` 参数，则响应仅包含状态消息；工作簿将被写入指定位置。

**未提供 `outPath` 参数时的示例响应**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### 错误代码

- **200 OK** – 提取成功完成。  
- **202 Accepted** – 请求已接受，将进行异步处理。  
- **400 Bad Request** – Aspose.Cells Cloud API URI 无效或缺少必要参数。  
- **401 Unauthorized** – 访问令牌、客户端 ID 或客户端密钥无效。  
- **404 Not Found** – 无法访问指定的电子表格文件。  
- **500 Server Error** – 处理工作簿时发生意外错误。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 封装了底层细节，使您只需极少代码即可为单元格实现 **提取文本** 功能。请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C# 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go 示例 – 提取文本（为简洁起见省略代码）
```

{{</tab>}}

{{< /tabs >}}