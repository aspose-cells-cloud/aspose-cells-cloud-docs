---
title: "在 Excel 工作表中使用自动调整功能"
second_title: "文档"
linktitle: "自动调整"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "自动调整, 列, 行, Aspose.Cells, 云, Excel, API, 调整大小"
description: "了解如何使用 Aspose.Cells Cloud REST API 自动调整 Excel 工作表中的行和列大小。包含 cURL、.NET、Java 和 Python 示例。"
weight: 20
ArticleTitle: "在 Excel 工作表中使用自动调整功能 – Aspose.Cells Cloud API"
---

## 在 Excel 工作表中使用自动调整功能

- [如何自动调整 Excel 工作表中的一列。](/cells/worksheets/autofit/column/)
- [如何自动调整 Excel 工作表中的多列。](/cells/worksheets/autofit/columns/)
- [如何自动调整 Excel 工作表中的一行。](/cells/worksheets/autofit/row/)
- [如何自动调整 Excel 工作表中的多行。](/cells/worksheets/autofit/rows/)

**前置条件**  
使用自动调整功能前，您需具备以下条件：

1. 一个已获取有效 **Client Id** 和 **Client Secret** 的 Aspose.Cells Cloud 账户。  
2. 上传至 Aspose Cloud 存储（或可通过公开 URL 访问）的工作簿。  
3. 您打算修改的工作表名称。

**API 参考**

| 操作 | HTTP 方法 | 端点 | 必需参数 | 请求体 | 示例响应 | 状态码 |
|------|-----------|------|--------|--------|-----------|---------|
| 自动调整 **列** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName`（路径）<br> `columnIndex`（查询） | *无* | `{ "code": 200, "status": "OK", "message": "列已自动调整。" }` | 200, 400, 401, 404, 500 |
| 自动调整 **多列** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName`（路径）<br> `startColumn`, `endColumn`（查询） | *无* | `{ "code": 200, "status": "OK", "message": "列已自动调整。" }` | 200, 400, 401, 404, 500 |
| 自动调整 **行** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName`（路径）<br> `rowIndex`（查询） | *无* | `{ "code": 200, "status": "OK", "message": "行已自动调整。" }` | 200, 400, 401, 404, 500 |
| 自动调整 **多行** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName`（路径）<br> `startRow`, `endRow`（查询） | *无* | `{ "code": 200, "status": "OK", "message": "行已自动调整。" }` | 200, 400, 401, 404, 500 |

**代码示例**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// 身份验证
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// 调用自动调整列
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// 自动调整行
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# 自动调整单列
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

以上代码片段展示了如何：

1. 使用您的 **Client Id** 和 **Client Secret** 对 Aspose.Cells Cloud 进行身份验证。  
2. 调用适用于列或行的自动调整端点。  
3. 处理响应以确认操作成功。

**后续步骤**

自动调整调用完成后，您可下载更新后的工作簿：

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

请自由调整 `startColumn`、`endColumn`、`startRow` 和 `endRow` 参数以定位特定范围。