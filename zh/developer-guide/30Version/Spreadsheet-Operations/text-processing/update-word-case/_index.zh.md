---
title: "Aspose.Cells – 更新单词大小写 API"
second_title: "文档"
linktype: "文档"
type: docs
url: /zh/post-update-word-case/
keywords: "Aspose.Cells, 更新单词大小写 API, 文本大小写转换, Excel, CSV, Google Sheets, REST API"
description: "使用 Aspose.Cells Cloud 的更新单词大小写 API，在 Excel、CSV 或 Google Sheets 文件中转换文本大小写。支持全大写、全小写、首字母大写和标题大小写。"
weight: 100
ArticleTitle: "Aspose.Cells – 更新单词大小写 API 文档"
---

**API 版本：** 3.0

在电子表格（Excel、Google Sheets、CSV）中处理不一致的文本大小写可能令人烦恼，尤其是在处理大型数据集时。**PostUpdateWordCase Web API** 可自动完成文本大小写转换，以最少的工作量确保数据整洁、标准化。

## **Excel Web API – 更新单词大小写 API**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **功能说明**

PostUpdateWordCase Web API 解决了电子表格中文本大小写不一致的常见问题，这类问题会显著影响数据分析与处理。该 API 可自动完成大小写转换，确保您的数据整洁、标准化，便于后续操作或分析。

- **自动文本大小写转换**
  - **全大写转全小写** – 将所有大写字母转换为小写。
  - **全小写转全大写** – 将所有小写字母转换为大写。
  - **首字母大写** – 将每个单词的首字母大写。
  - **标题大小写** – 将文本转换为标题大小写，即每个主要单词的首字母大写。

- **支持多种格式** – 该 API 支持广泛的电子表格格式，包括 Excel、OpenOffice、JSON、CSV 等。这种多功能性使其适用于各种数据处理需求。

### **请求参数**

| 参数名称          | 类型   | 位置         | 描述                                                                                                               |
| ----------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------ |
| `wordCaseOptions` | 对象   | 请求体       | 定义所需大小写转换的选项，例如源范围、目标大小写类型及其他设置。                                                 |

**`wordCaseOptions` 架构**

```json
{
  "Range": "A1:B10", // 需处理的 Excel 风格范围（必填）
  "CaseType": "Upper", // 枚举：Upper（全大写）、Lower（全小写）、Capitalize（首字母大写）、Title（标题大小写）（必填）
  "IgnoreBlank": true // 布尔值，可选 —— 为 true 时，空白单元格保持不变
}
```

**示例请求体**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range（范围）** – 应用大小写转换的单元格范围（例如 `A1:C5`）。
- **CaseType（大小写类型）** – 大小写转换类型。允许的值为 `Upper`、`Lower`、`Capitalize` 和 `Title`。
- **IgnoreBlank（忽略空白）** – 若为 `true`，则忽略空白单元格；默认为 `false`。

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[合并后的文件名]",
    "Filesize" : [文件大小],
    "FileContent" : "[Base64 字符串]"
}
```

- **Filename（文件名）** – 已处理文件的名称。
- **FileSize（文件大小）** – 文件大小（单位：字节）。
- **FileContent（文件内容）** – 已转换文件内容的 Base64 编码字符串。

**HTTP 状态码**

| 状态码 | 含义           | 描述                                             |
|--------|----------------|--------------------------------------------------|
| 200    | OK（成功）     | 筛选器应用成功；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。        |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                            |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。                      |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                          |

## 如何使用 SDK 调用 PostUpdateWordCase API

### PostUpdateWordCase API 规范

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---