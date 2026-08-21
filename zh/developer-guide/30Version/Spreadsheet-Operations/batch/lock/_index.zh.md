---
title: "批量锁定 Excel 文件"
second_title: "文档"
type: docs
url: /zh/batch/lock
keywords: "批量锁定, Excel, Aspose.Cells, 云 API, 电子表格, 文件保护"
description: "Aspose.Cells Cloud API 支持批量锁定多个 Excel 文件。您可通过 REST 端点或任一支持的 SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go 等）进行批量文件锁定。"
weight: 100
---

此 REST API 支持对符合条件的 Excel 文件执行**批量锁定**操作。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称           | 类型               | 位置 | 描述                                     |
|--------------------|--------------------|------|------------------------------------------|
| BatchLockRequest   | BatchLockRequest   | body | 包含锁定参数的 JSON 请求体。            |

#### **BatchLockRequest** 属性

| 名称           | 类型                     | 描述                                          | 备注     |
|----------------|--------------------------|-----------------------------------------------|----------|
| SourceFolder   | string                   | 包含源 Excel 文件的文件夹。                   | 可选     |
| MatchCondition | MatchConditionRequest    | 用于选择需锁定文件的匹配条件。                | 可选     |
| Password       | string                   | 应用于已锁定文件的密码。                      | 可选     |
| OutFolder      | string                   | 存放已锁定文件的目标文件夹。                  | 可选     |

#### **MatchConditionRequest** 属性

| 名称               | 类型      | 描述                                     | 备注     |
|--------------------|-----------|------------------------------------------|----------|
| RegexPattern       | string    | 用于匹配文件名的正则表达式模式。         | 可选     |
| FullMatchConditions| string[]  | 用于精确匹配文件名以进行锁定的条件列表。 | 可选     |

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

| 状态码 | 含义                   | 返回条件                           |
|--------|------------------------|------------------------------------|
| 200 OK | 工作簿创建成功         | 正常流程                           |
| 201 Created | 工作簿已创建（替代响应） | 当 API 返回已创建状态时           |
| 400 Bad Request | 无效参数       | 客户端错误                         |
| 401 Unauthorized | 缺失或无效令牌 | 身份验证错误                      |
| 409 Conflict | 文件已存在且 `isWriteOver=false` | 与已有文件冲突 |

## 如何使用 SDK 调用 PostBatchLock API

### PostBatchLock API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) 定义了一个公开可访问的编程接口，您可直接通过网页浏览器执行 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

使用 SDK 是开发速度最快的方式。SDK 抽象了底层细节，让您能专注于锁定任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何通过多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}