---
title: "Aspose.Cells Cloud Web API – 使用 AI 驱动的语言转换功能翻译文本文件"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud AI 翻译 API 翻译文本文件"
linktype: "翻译文本文件"
type: docs
url: /zh/translate-text-file/
keywords: "Aspose.Cells, 云 API, AI 翻译, 翻译文本文件, 多语言转换, REST PUT, 目标语言代码, 文件上传翻译, 原始文本翻译, 电子表格 AI"
description: "了解如何使用 Aspose.Cells Cloud AI 的 TranslateTextFile 端点将文本文件转换为任意支持的语言。支持多部件文件上传和原始文本载荷两种模式，保留原始格式，并返回可下载的已翻译文件。"
weight: 100
---

**TranslateTextFile** 端点利用 Aspose.Cells Cloud AI 服务，将文本文件的内容翻译为指定的目标语言。它支持两种操作模式：(1) **文件上传模式**——通过 multipart/form-data 发送文本文件，并接收已翻译的文件；(2) **直接内容模式**——在请求体中提交原始文本，并直接获取翻译后的文本。该服务会保留原始换行符和格式，自动为文件名添加 “\_translated” 后缀，并以可下载流的形式返回结果。适用于批量翻译文档、集成到多语言工作流中，或实时翻译用户生成内容。

## **TranslateTextFile API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **请求参数：**

| 参数名称       | 类型   | 位置     | 必需/可选 | 描述                                                                                                                                                                                                 |
| :------------- | :----- | :------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | 文件   | 请求体   | 必需      | 待翻译的源文本文件。必须为纯文本（.txt）或支持的电子表格格式。示例：通过名为 "file" 的 multipart/form-data 字段上传 `document.txt`。                                                                 |
| targetLanguage | 字符串 | 查询参数 | 必需      | 目标语言的 ISO-639-1 语言代码（例如："es" 表示西班牙语，"fr" 表示法语，"de" 表示德语）。该代码不区分大小写。                                                                                           |
| region         | 字符串 | 查询参数 | 可选      | 电子表格区域标识符，影响区域性特定格式（如日期、数字和货币）。常见取值："US"、"EU"、"CN"。若省略，则使用工作簿的原始区域设置。                                                                         |
| password       | 字符串 | 查询参数 | 可选      | 打开加密电子表格文件所需的密码。纯文本文件无需提供。                                                                                                                                                 |

### **响应**

成功响应（200 OK）
响应头：
Content-Type: application/octet-stream // 已翻译文件的二进制流
Content-Disposition: attachment; filename="<原文件名>\_translated.txt"
Content-Length: <字节数>

响应体：包含已翻译文本的二进制流，保留原始换行符和格式。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
| ------ | ---------------- | ------------------------------------------ |
| 200    | OK（成功）       | 翻译操作成功；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（载荷过大） | 上传的文件超过大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                     |

## 应在何处使用 TranslateTextFile API？

- **多语言文档门户**——自动翻译以文本文件形式上传的用户手册或帮助文档，按需提供本地化版本。
- **内容管理系统（CMS）**——集成至 CMS 工作流中，在发布前将博客文章或新闻稿翻译为面向国际受众的语言。
- **企业数据处理流程**——用于批处理作业，处理大量 CSV 或 TXT 报表，将其转换为区域办事处所需语言，同时保留原始格式。
- **客户支持平台**——实时翻译传入的纯文本工单或聊天记录，辅助使用不同语言的客服人员。

## 为何应使用 TranslateTextFile API？

- **AI 驱动的高精度翻译**——采用最先进的神经网络翻译模型，实现自然、上下文感知的输出。
- **双重输入灵活性**——支持文件上传和原始文本载荷，简化与各类客户端应用的集成。
- **保留原始布局**——维持换行符、缩进和特殊字符，避免后续处理清理工作。
- **无缝文件处理**——返回已自动生成 “\_translated” 后缀的可直接下载文件，降低客户端代码复杂度。

## 如何使用 SDK 调用 TranslateTextFile API

### TranslateTextFile API 规范

[TranslateTextFile API 规范](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) 提供了公开可访问的编程接口，允许直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您能够用简短代码快速实现电子表格合并等功能。
请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。
以下代码示例展示了如何使用多种 SDK 与 Aspose.Cells Web 服务进行交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}