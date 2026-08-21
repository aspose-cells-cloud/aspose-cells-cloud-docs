---
title: "删除 Excel 工作表中的所有数据透视表"
description: "使用 Aspose.Cells Cloud REST API 删除指定工作表中的所有数据透视表。"
keywords: "Aspose.Cells, 数据透视表, 删除, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# 删除 Excel 工作表中的所有数据透视表

## 概述
此操作将从 Excel 文件中的指定工作表中**全部**删除数据透视表。当您需要重置工作表的分析内容，或在一次调用中清理未使用数据透视表时，该操作非常有用。

## 前提条件
调用 API 前，请确保已完成以下步骤：

1. **Aspose Cloud 账户** – 若您尚未注册，请先注册 Aspose Cloud 账户。  
2. **JWT 令牌** – 生成用于身份验证的 JSON Web Token（JWT）。详情请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。  
3. **存储设置** – 将目标 Excel 文件上传至 Aspose Cloud 存储或已连接的外部存储中。请记录该文件所在的**文件夹路径**和**存储名称**（如适用）。

## 身份验证
Aspose.Cells Cloud API 需要基于 **JWT 令牌的身份验证**。请在每个请求的 `Authorization` 请求头中包含该令牌：

```
Authorization: Bearer <jwt token>
```

## HTTP 请求

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### 路径参数
| 名称 | 类型 | 必填 | 描述 |
|------|------|------|------|
| `name` | string | 是 | Excel 文件的名称（例如：`Sample.xlsx`）。 |
| `sheetName` | string | 是 | 将从中删除所有数据透视表的工作表名称（例如：`Sheet1`）。 |

### 查询参数
| 名称 | 类型 | 必填 | 描述 |
|------|------|------|------|
| `folder` | string | 否 | 文件所在的文件夹路径。 |
| `storageName` | string | 否 | 使用的存储名称（当文件不在默认存储中时）。 |

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## 成功响应
服务将返回标准 `CellsCloudResponse` 对象，指示操作状态。

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## 错误处理

| HTTP 状态码 | 含义 | 示例响应体 |
|-------------|------|------------|
| **400** | 请求错误 – 缺失或无效参数 | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | 未授权 – 无效或已过期的 JWT | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | 未找到 – 文件或工作表不存在 | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | 服务器内部错误 – 意外故障 | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## SDK 示例
以下代码片段展示了如何使用多个 Aspose.Cells Cloud SDK 调用该操作。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// 初始化 API 客户端
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// 配置请求参数
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# 配置 API 客户端
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*其他 SDK（包括 Go、PHP、Ruby、Swift、Perl、Android）可在 [Aspose.Cells Cloud SDK 代码仓库](https://github.com/aspose-cells-cloud) 中获取。*

## 参考资源
- [删除特定数据透视表](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [获取工作表中所有数据透视表](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [身份验证概述](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [DeleteWorksheetPivotTables 的 OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*本文档最后更新于 2026-07-30。所有内容均采用 UTF-8 编码。*
---