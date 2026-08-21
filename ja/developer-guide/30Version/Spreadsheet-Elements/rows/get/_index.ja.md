---
---
title: "Aspose.Cells Cloud API を使用して Excel ワークシートから単一の行を取得する"
description: "Aspose Cloud ストレージに保存された Excel ワークシートから特定の行を取得する方法を、Aspose.Cells Cloud REST API を使用して学びます。リクエスト構文、パラメータ、レスポンススキーマ、サンプル cURL、および SDK コード (C#、Java、Python) を含みます。"
keywords: "Aspose.Cells Cloud, 行の取得, Excel API, スプレッドシート REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Excel ワークシートから単一の行を取得する

**エンドポイント**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Aspose Cloud ストレージに保存されたワークシートから行を取得します。この操作には、**Read** スコープを含む有効な OAuth 2.0 アクセストークンが必要です。

---

## 目次
1. [前提条件](#前提条件)  
2. [HTTP リクエスト](#http-リクエスト)  
3. [パラメータ](#パラメータ)  
   - [パスパラメータ](#パスパラメータ)  
   - [クエリパラメータ](#クエリパラメータ)  
4. [cURL の例](#curl-の例)  
5. [レスポンス](#レスポンス)  
   - [成功時のスキーマ](#成功時のスキーマ)  
   - [ステータスコード](#ステータスコード)  
6. [SDK コードサンプル](#sdk-コードサンプル)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [関連操作](#関連操作)  
8. [注意事項と制限事項](#注意事項と制限事項)  

---

## 前提条件
- アクティブなサブスクリプションを備えた **Aspose Cloud アカウント**。  
- **Read** スコープを含む **OAuth 2.0 アクセストークン**。  
- 対象となるワークブックは、すでに Aspose Cloud ストレージに存在している必要があります。  

---

## HTTP リクエスト
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*ベース URL*: `https://api.aspose.cloud/v3.0`

---

## パラメータ

### パスパラメータ
| 名前        | 型     | 必須   | 説明                                      |
|-------------|--------|--------|-------------------------------------------|
| `name`      | 文字列 | ✅     | ワークブックファイルの名前 (例: `MyWorkbook.xlsx`)。 |
| `sheetName` | 文字列 | ✅     | ワークシートの名前 (例: `Sheet1`)。 |
| `rowIndex`  | 整数   | ✅     | 取得する行の 0 から始まるインデックス。 |

### クエリパラメータ *(オプション)*
| 名前            | 型     | 必須   | 説明                                      |
|-----------------|--------|--------|-------------------------------------------|
| `folder`        | 文字列 | ❌     | ワークブックが存在するクラウドストレージ内のフォルダのパス。 |
| `storageName`   | 文字列 | ❌     | ストレージサービスの名前 (カスタムストレージを使用する場合)。 |

---

## cURL の例
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## レスポンス

### 成功時のスキーマ (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* スタイルオブジェクト */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...その他のセル... */
    ]
  }
}
```

### ステータスコード
| コード | 意味 |
|--------|------|
| **200** | 行の取得に成功しました。 |
| **401** | 認証エラー – アクセストークンが不足しているか、無効です。 |
| **404** | ワークブック、ワークシート、または行が見つかりません。 |
| **500** | サーバー内部エラー。 |

### エラー例 (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

---

## SDK コードサンプル

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // オプション
);

Console.WriteLine($"Row {response.Row.Index} retrieved with {response.Row.Cells.Count} cells.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – オプション
);

System.out.println("Row index: " + response.getRow().getIndex());
System.out.println("Cells count: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Row {response.row.index} retrieved with {len(response.row.cells)} cells.")
except ApiException as e:
    print("Exception when calling CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## 関連操作
| 操作 | 説明 |
|------|------|
| **行の追加** | `POST /cells/{name}/worksheets/{sheetName}/rows` – ワークシートに行を新規に挿入します。 |
| **行の削除** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – 既存の行を削除します。 |
| **複数行の取得** | `GET /cells/{name}/worksheets/{sheetName}/rows` – 複数の行のコレクションを取得します。 |
| **行に関する概要** | `/cells/rows/` – 行関連のエンドポイントに関する一般ドキュメント。 |

---

## 注意事項と制限事項
- **レート制限**: アカウントあたり 1 分あたり 100 リクエスト。  
- **サポートされる形式**: XLS、XLSX、CSV、ODS。  
- 行インデックスは **0 から始まります**。最初の行は `0` です。  
- このエンドポイントを呼び出す前に、ワークブックが指定された `folder` にアップロードされていることを確認してください。  

---
---