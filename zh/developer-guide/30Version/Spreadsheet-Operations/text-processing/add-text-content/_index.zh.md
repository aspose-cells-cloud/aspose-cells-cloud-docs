---
title: "向 Excel 添加文本：通过电子表格 Web API 高效插入数据"
second_title: "文档"
linktitle: "添加文本"
type: docs
url: /zh/excel-add-text/
keywords: "Excel, Aspose.Cells, 添加文本, 电子表格 API, REST API, Office Cloud, 文本插入, Excel API"
description: "通过 Aspose.Cells Cloud API 向 Excel 电子表格中的指定位置添加文本。"
weight: 100
---

向电子表格中指定位置添加文本内容。该操作需要一个对象，用于定义要添加的文本内容及插入位置。

## **Excel API：PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **功能说明**

该方法可安全地向指定单元格追加新文本，支持多种插入模式和格式处理。

- **在所选单元格开头添加文本**  
  在所有选定单元格前追加文本，确保数据录入的一致性。适用于添加通用标识符或标签，如产品编码、类别或前缀。

- **在特定文本前后插入字符**  
  在选定单元格中目标文本之前或之后插入字符，便于快速构建结构化、有序的内容。

- **在每个选定单元格末尾追加相同文本**  
  一次性向多个单元格末尾添加相同文本，简化数据录入并保证格式统一。

- **在指定字符数前后插入文本**  
  在目标范围内每个单元格的开头或结尾指定字符数后插入文本。典型应用场景包括格式化编码、时间戳或自定义分隔符。

### **请求参数**

| 参数名称       | 类型  | 位置 | 描述                                           |
| -------------- | ----- | ---- | ---------------------------------------------- |
| addTextOptions | 类    | Body | 指定要添加的文本内容及插入位置。               |

### **响应**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                               |
| ------ | -------------- | -------------------------------------------------- |
| 200    | OK（成功）     | 过滤器应用成功；响应包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。         |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（请求实体过大） | 上传的文件大小超出限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                             |

## 如何使用 SDK 调用 PostAddTextContent API

### PostAddTextContent API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) 定义了一个公开可访问的编程接口，支持您直接通过网页浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最高效方式。SDK 处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}