---
title: "批量保护 Excel 文件"
second_title: "文档"
type: docs
url: /batch/protect
keywords: "批量保护 Excel 文件, Aspose Cells Cloud, REST API, Excel 保护, 批量保护"
description: "了解如何使用 Aspose.Cells Cloud REST API 批量保护多个 Excel 文件。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码示例。"
weight: 100
---

此 REST API 支持对符合条件的 Excel 文件执行**批量保护**操作。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **安全性与身份验证**

Aspose.Cells Cloud API 具备安全性，需要采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称              | 类型                | 位置 | 描述                                                                                              |
|-----------------------|---------------------|------|---------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body | JSON 载荷，指定源文件夹、匹配条件、保护类型、密码和输出文件夹。                                  |

### BatchProtectRequest 属性

| 名称             | 类型                     | 描述                                                                 | 说明     |
|------------------|--------------------------|----------------------------------------------------------------------|----------|
| SourceFolder     | string                   | 包含源 Excel 文件的文件夹。                                          | 可选     |
| MatchCondition   | MatchConditionRequest   | 用于选择需保护文件的匹配条件。                                       | 可选     |
| ProtectionType   | string                   | 要应用的保护类型（例如 `All`、`ReadOnly`）。                         | 可选     |
| Password         | string                   | 为受保护文件设置的密码。                                             | 可选     |
| OutFolder        | string                   | 受保护文件的目标文件夹。                                             | 可选     |

### MatchConditionRequest 属性

| 名称                | 类型       | 描述                           | 说明     |
|---------------------|------------|--------------------------------|----------|
| RegexPattern        | string     | 用于匹配文件名的正则表达式。   | 可选     |
| FullMatchConditions | string[]   | 完整文件名匹配条件列表。       | 可选     |

### 请求体参数

| 参数名称 | 类型 | 描述                         |
|----------|------|------------------------------|
| data     | file | 要创建的工作簿文件的二进制内容。 |

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
**HTTP 状态码**

| 状态码 | 含义               | 返回条件                         |
|--------|--------------------|----------------------------------|
| 200 OK | 工作簿创建成功     | 正常流程                         |
| 201 Created | 工作簿已创建（替代响应） | 当 API 返回已创建状态时         |
| 400 Bad Request | 参数无效 | 客户端错误                       |
| 401 Unauthorized | 缺少或无效的令牌 | 身份验证错误                    |
| 409 Conflict | 文件已存在且 `isWriteOver=false` | 与现有文件冲突                |

## 如何使用 SDK 调用 PostProtectConvert API

### PostProtectConvert API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PostProtectConvert) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}