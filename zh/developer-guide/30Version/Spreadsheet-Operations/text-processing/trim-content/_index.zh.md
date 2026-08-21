---
title: "Aspose.Cells Trim Content API — 移除 Excel 中的空格与换行符"
second_title: "文档"
linktype: "Trim Content"
type: docs
url: /zh/spreadsheet-trim-content/
keywords: "Aspose.Cells, Trim Content API, Excel 数据清理, 移除 Excel 空格, 换行符移除, 电子表格数据清洗"
description: "使用 Aspose.Cells Cloud 的 PostTrimContent API 自动清理 Excel 单元格中的多余空格、换行符及其他不需要的字符。了解接口地址、请求格式、示例代码及错误处理方式。"
weight: 100
---

## **电子表格 Web API：PostTrimContent**

**PostTrimContent** API 可对电子表格中指定范围内的内容进行处理与清理，移除所选单元格内容中的多余空格、换行符及其他不必要的字符，适用于数据录入清洗及确保电子表格格式一致性。

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

### **功能说明**

- **高效性**：仅清理指定范围内的内容，避免对整个工作表执行无意义操作，从而节省时间与资源。
- **灵活性**：允许用户自定义需处理的精确单元格范围，适配各类数据集与需求。
- **数据完整性**：移除多余空格与换行符，有助于维持一致可靠的数据，便于后续分析与报表生成。
- **易用性**：集成简单、配置要求低，适合开发者及终端用户使用。

### **请求参数**

| 参数名称           | 类型  | 位置 | 描述                                                   |
| ------------------ | ----- | ---- | ------------------------------------------------------ |
| trimContentOptions | 类    | 请求体 | 指定内容清理方式的选项（例如目标范围、清理模式等）。 |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[合并后文件名]",
    "Filesize" : [文件大小],
    "FileContent" : "[Base64字符串]"
}
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                       |
|--------|-------------------|--------------------------------------------|
| 200    | OK（成功）        | 清理操作成功；响应中包含操作详情。         |
| 400    | Bad Request（错误请求） | 请求参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权）   | JWT 令牌无效或缺失。                        |
| 413    | Payload Too Large（请求体过大） | 上传文件超出大小限制。                     |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                        |

## 如何使用 PostRemoveCharacters API（SDK 示例）

### PostRemoveCharacters API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_最后更新时间：2026-03-30_