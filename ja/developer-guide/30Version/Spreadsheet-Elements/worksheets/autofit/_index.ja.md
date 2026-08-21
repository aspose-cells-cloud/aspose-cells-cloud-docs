---
title: "Excelワークシートでのオートフィットの使用"
second_title: "Document"
linktitle: "オートフィット"
type: docs
url: /ja/worksheets/autofit/
aliases: [  /ja/autofit-rows-and-columns-of-worksheet/ ]
keywords: "オートフィット, 列, 行, Aspose.Cells, Cloud, Excel, API, リサイズ"
description: "Aspose.Cells Cloud REST API を使って Excel ワークシートの行と列を自動的にリサイズする方法を学びます。cURL、.NET、Java、Python のサンプルを含みます。"
weight: 20
ArticleTitle: "Excelワークシートでのオートフィットの使用 – Aspose.Cells Cloud API"
---

## Excelワークシートでのオートフィットの使用

- [Excelワークシートで列をオートフィットする方法。](/cells/worksheets/autofit/column/)
- [Excelワークシートで複数の列をオートフィットする方法。](/cells/worksheets/autofit/columns/)
- [Excelワークシートで行をオートフィットする方法。](/cells/worksheets/autofit/row/)
- [Excelワークシートで複数の行をオートフィットする方法。](/cells/worksheets/autofit/rows/)

**前提条件**  
オートフィット操作を使用する前に、以下の条件を満たしている必要があります：

1. 有効な **Client Id** および **Client Secret** を持つ Aspose.Cells Cloud アカウント。  
2. Aspose Cloud ストレージにアップロードされたワークブック（またはパブリックURLでアクセス可能なワークブック）。  
3. 変更対象のワークシート名。

**API リファレンス**  

| 操作 | HTTP メソッド | エンドポイント | 必要なパラメータ | リクエストボディ | サンプルレスポンス | ステータスコード |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| **列** をオートフィット | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName`（パス） <br> `columnIndex`（クエリ） | *なし* | `{ "code": 200, "status": "OK", "message": "Column autofitted." }` | 200, 400, 401, 404, 500 |
| **列** をオートフィット（複数） | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName`（パス） <br> `startColumn`, `endColumn`（クエリ） | *なし* | `{ "code": 200, "status": "OK", "message": "Columns autofitted." }` | 200, 400, 401, 404, 500 |
| **行** をオートフィット | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName`（パス） <br> `rowIndex`（クエリ） | *なし* | `{ "code": 200, "status": "OK", "message": "Row autofitted." }` | 200, 400, 401, 404, 500 |
| **行** をオートフィット（複数） | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName`（パス） <br> `startRow`, `endRow`（クエリ） | *なし* | `{ "code": 200, "status": "OK", "message": "Rows autofitted." }` | 200, 400, 401, 404, 500 |

**コードサンプル**

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

// 認証
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// 列のオートフィットを実行
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

// 行のオートフィット
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

# 単一列のオートフィット
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

これらのコードスニペットは以下のことを示しています：

1. **Client Id** および **Client Secret** を使用した Aspose.Cells Cloud の認証方法。  
2. 列または行の適切なオートフィットエンドポイントを呼び出す方法。  
3. 操作が成功したことを確認するレスポンスの処理方法。

**次のステップ**

オートフィット呼び出しが完了したら、更新されたワークブックをダウンロードできます：

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

`startColumn`、`endColumn`、`startRow`、`endRow` パラメータを調整して、特定の範囲を対象にすることもできます。
---