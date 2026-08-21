---
title: 在 Excel 中取消分组列 – Aspose.Cells Cloud API  
description: 使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作表中移除列分组。包含端点、参数、认证方式、cURL 示例、响应格式及 SDK 代码片段。  
keywords: Aspose.Cells, 取消分组, 列, Excel, API, REST, 云服务, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# 在 Excel 中取消分组列  

Aspose.Cells Cloud 提供了一项 **POST** 操作，用于从指定工作表中移除列分组。本页面详细说明了请求格式、必需参数、认证方式、示例调用及 SDK 使用方法。

---  

## 前置条件  

| 要求项 | 必要原因 |
|--------|----------|
| **Aspose Cloud 账户** | 用于访问 Aspose.Cells Cloud 服务。 |
| **JWT 访问令牌** | 所有 API 请求必须通过承载令牌（bearer token）进行授权。详见 [JWT 认证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。 |
| **存储于 Aspose Cloud 存储中的工作簿** | API 仅处理位于云存储（或已连接的外部存储）中的文件。 |
| **工作表名称** | 目标工作表必须存在于工作簿中。 |

---  

## 认证  

所有请求均需在请求头中包含有效的 JWT 令牌，格式如下：

```http
Authorization: Bearer <access_token>
```

令牌通过 Aspose Cloud OAuth 流程获取。令牌具有有效期，过期后需重新刷新。

---  

## 端点  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **路径参数** – 工作簿文件名（例如 `test.xlsx`）。  
* `{sheetName}` – **路径参数** – 工作表名称（例如 `Sheet1`）。  

---  

## 参数  

### 路径参数  

| 名称 | 类型 | 是否必需 | 描述 |
|------|------|----------|------|
| `name` | string | 是 | 工作簿文件名。 |
| `sheetName` | string | 是 | 工作表名称。 |

### 查询参数  

| 名称 | 类型 | 是否必需 | 描述 |
|------|------|----------|------|
| `firstIndex` | integer | 是 | 要取消分组的第一列的从零开始索引。 |
| `lastIndex` | integer | 是 | 要取消分组的最后一列的从零开始索引。 |
| `folder` | string | 否 | 包含工作簿的文件夹路径。 |
| `storageName` | string | 否 | 文件所在存储服务的名称。 |

---  

## 请求示例（cURL）  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*请将 `<access_token>` 替换为有效的 JWT 令牌。*

---  

## 成功响应  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

响应对象（`CellsCloudResponse`）包含已成功取消分组的列范围。

### 错误响应  

请求失败时，服务将返回包含以下字段的 JSON 响应体：

| 字段 | 含义 |
|------|------|
| `Code` | HTTP 风格错误代码（例如 400、401）。 |
| `Status` | 错误的简短描述。 |
| `ErrorMessage` | 错误的详细描述。 |

---  

**HTTP 状态码说明**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK | 分组已成功取消；响应中包含操作详情。 |
| 400 | Bad Request | 缺少或参数无效（例如不支持的文件类型）。 |
| 401 | Unauthorized | 无效或缺失 JWT 令牌。 |
| 413 | Payload Too Large | 上传文件超过大小限制。 |
| 500 | Internal Server Error | 服务器内部意外错误。 |
---  

## SDK 代码示例  

以下为最常用 SDK 的可直接运行代码片段。请将占位符（`<YourAccessToken>`、`<YourFileName>` 等）替换为实际数据。

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **注意**：PHP、Ruby、Perl 及其他语言的 SDK 均遵循相同的参数顺序。完整示例请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

---  

## 参考资料  

* **OpenAPI 规范**：<https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **认证指南**：<https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK 仓库**：<https://github.com/aspose-cells-cloud>

---  

## 版本历史  

| 日期 | 作者 | 变更内容 |
|------|------|----------|
| 2026‑07‑30 | AI Optimizer | 修复 UTF‑8 编码问题；补充前置条件说明；清理元关键词；优化标题层级；插入 SDK 代码片段。 |
| 2026‑07‑29 | 原作者 | 初稿。 |

---