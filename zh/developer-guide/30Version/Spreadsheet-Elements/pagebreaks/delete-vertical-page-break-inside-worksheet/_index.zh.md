---
title: 删除垂直分页符 – Aspose.Cells Cloud REST API
description: 使用 Aspose.Cells Cloud REST API（v3.0）删除 Excel 工作表中的垂直分页符。包含请求语法、参数、示例、响应代码和 SDK 代码片段。
keywords: 删除垂直分页符, Aspose.Cells Cloud, REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# 删除垂直分页符

使用 Aspose.Cells Cloud REST API 删除 Excel 工作簿中工作表的垂直分页符。

---

## 前置条件

* 必须在 `Authorization` 请求头中提供 **JWT 认证令牌**。  
* 工作簿（`{name}`）必须存储在指定的 **文件夹** 或 **存储空间** 中，并且 API 客户端可访问该文件。

---

## HTTP 请求

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| 参数 | 类型 | 位置 | 必填 | 描述 |
|-----------|--------|----------|----------|-------------|
| **name**      | string | path   | Yes | Excel 文件的名称。 |
| **sheetName** | string | path   | Yes | 包含该分页符的工作表名称。 |
| **index**     | integer| path   | Yes | 要删除的垂直分页符的从零开始的索引。 |
| **folder**    | string | query  | No  | 文件所在的文件夹路径。 |
| **storageName**| string| query  | No  | 存储服务的名称。 |

---

## 请求示例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## 成功响应

| 状态码 | 描述 |
|------|-------------|
| **200** | 垂直分页符已成功删除。 |

**示例响应体**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## 错误响应

| HTTP 状态码 | 描述 |
|-----------|-------------|
| **401** | 未授权 – 缺少或无效的令牌。 |
| **404** | 未找到 – 指定的文件、工作表或分页符索引不存在。 |
| **400** | 错误请求 – 请求语法格式错误或参数无效。 |
| **500** | 服务器内部错误 – 遇到意外情况。 |

**错误响应示例**

*401 – 未授权*

```json
{
  "Code": 401,
  "Message": "Invalid authentication token."
}
```

*404 – 未找到*

```json
{
  "Code": 404,
  "Message": "The specified file, worksheet, or page‑break index was not found."
}
```

*400 – 错误请求*

```json
{
  "Code": 400,
  "Message": "The request parameters are invalid or malformed."
}
```

*500 – 服务器内部错误*

```json
{
  "Code": 500,
  "Message": "An unexpected server error occurred."
}
```

---

## SDK 代码示例

以下示例演示如何使用 various Aspose.Cells Cloud SDK 调用 **DeleteVerticalPageBreak** 操作。

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*（PHP、Ruby、Perl 及其他语言的 SDK 代码片段遵循相同模式，可在官方 GitHub 仓库中获取。）*

---

## 相关资源

* **OpenAPI 规范** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>  
* **认证指南** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*文档最后更新时间：2026‑07‑30*