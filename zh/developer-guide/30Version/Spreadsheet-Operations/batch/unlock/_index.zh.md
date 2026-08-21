---
title: "批量解锁"
second: "文档"
type: docs
url: /zh/batch/unlock
keywords: "批量解锁, Aspose.Cells Cloud, Excel, REST API, 电子表格, 云 SDK"
description: "使用 Aspose.Cells Cloud REST API 批量解锁符合条件的 Excel 文件。支持 C#、Java、Python 等多种语言的 SDK。"
weight: 100
---

此 REST API 可批量解锁符合条件的 Excel 文件。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需要使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### 请求参数

| 参数名称         | 类型   | 位置   | 描述                               |
|------------------|--------|--------|------------------------------------|
| **BatchLockRequest** |  | body   | 包含解锁设置的请求体。              |

### **BatchLockRequest** 属性

| 名称           | 类型                     | 描述                           | 备注       |
|----------------|--------------------------|--------------------------------|------------|
| SourceFolder   | string                   | 包含源 Excel 文件的文件夹。    | [可选]     |
| MatchCondition | MatchConditionRequest    | 用于选择待解锁文件的匹配条件。  | [可选]     |
| Password       | string                   | 应用于受保护工作簿的密码。      | [可选]     |
| OutFolder      | string                   | 解锁后文件的输出文件夹。        | [可选]     |

### **MatchConditionRequest** 属性

| 名称               | 类型      | 描述                     | 备注       |
|--------------------|-----------|--------------------------|------------|
| RegexPattern       | string    | 用于匹配文件名的正则表达式。| [可选]     |
| FullMatchConditions| string[]  | 用于精确匹配的文件名条件。  | [可选]     |

### 请求体参数

| 参数名称 | 类型 | 描述                             |
|----------|------|----------------------------------|
| data     | file | 待创建的工作簿文件的二进制内容。 |

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

| 状态码 | 含义                   | 返回条件                           |
|--------|------------------------|------------------------------------|
| 200 OK | 工作簿创建成功         | 正常流程                           |
| 201 Created | 工作簿已创建（替代响应） | API 返回已创建状态时           |
| 400 Bad Request | 参数无效         | 客户端错误                         |
| 401 Unauthorized | 缺少或无效的令牌 | 认证错误                           |
| 409 Conflict | 文件已存在且 `isWriteOver=false` | 与现有文件冲突 |

## 如何使用 SDK 调用 PostBatchLock API

### PostBatchLock API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

使用 SDK 是开发解锁功能的最快方式。SDK 抽象了底层细节，让您专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}