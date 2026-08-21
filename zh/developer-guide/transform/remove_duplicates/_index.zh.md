---
title: "移除重复项"
ArticleTitle: "移除重复项 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: /zh/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, 移除重复项, API"
description: "移除工作表、范围或表格中的重复值。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的移除重复项功能

移除工作表、范围或表格中的重复值。该方法会扫描目标范围，检查指定列中具有相同值的整行。对于每组重复项，仅保留首次出现的行，其余全部删除。比较操作通常区分大小写，并精确匹配单元格内容。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型   | 路径/查询字符串/HTTP 正文 | 描述 |
|----------------|--------|-----------------------------|------|
| Spreadsheet    | 文件   | FormData                    | 上传电子表格文件。 |
| worksheet      | 字符串 | 查询字符串                  | 工作表名称。（可选） |
| range          | 字符串 | 查询字符串                  | 需要去重的范围名称。（可选） |
| table          | 字符串 | 查询字符串                  | 需要去重的表格名称。（可选） |
| outPath        | 字符串 | 查询字符串                  | （可选）工作簿所在文件夹路径，默认为 null。 |
| outStorageName | 字符串 | 查询字符串                  | 输出文件的存储名称。 |
| region         | 字符串 | 查询字符串                  | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`）。影响数字格式、日期解析及区域特定行为。 |
| password       | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| [TBD]    | [TBD] | [TBD] |

### **响应**

```json
{
  "File": "二进制流，表示处理后的电子表格（例如 .xlsx）"
}
```

**响应状态码**

| 状态码 | 含义             | 描述 |
|--------|------------------|------|
| 200    | OK（成功）       | 返回已移除重复项的电子表格，以文件流形式提供。 |
| 400    | Bad Request（错误请求） | 请求参数无效或 URL 格式错误。 |
| 401    | Unauthorized（未授权） | 身份验证失败或未提供凭据。 |
| 413    | Payload Too Large（请求实体过大） | 上传文件大小超出允许上限。 |
| 500    | Internal Server Error（内部服务器错误） | 电子表格在获取数据时发生异常或出现其他服务器端错误。 |

## 如何使用 SDK 实现移除重复项功能

### 移除重复项规范

[移除重复项 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) 定义了公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API：

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}
{< tab tabNum="1" >}
```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=zh-CN&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "二进制流，表示处理后的电子表格（例如 .xlsx）"
}
```
{< /tab >}
{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 封装了底层细节，让您能专注于项目核心任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose Cells Cloud Web 服务：

```csharp
// C# 的 SDK 示例代码
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "zh-CN",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Java 的 SDK 示例代码
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "zh-CN",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Python 的 SDK 示例代码
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='zh-CN',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("调用 TransformApi->remove_duplicates 时发生异常: %s\n" % e)
```

`[TBD]`
---