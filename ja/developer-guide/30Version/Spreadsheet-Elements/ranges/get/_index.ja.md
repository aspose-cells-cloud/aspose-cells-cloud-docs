---
title: "Excelワークシートから範囲の内容を取得する方法"
second_title: "Document"
linktitle: "取得"
type: docs
url: /ja/ranges/get/
keywords: "Aspose.Cells, Excel, API, get, range, spreadsheet, REST"
description: "Aspose.Cells Cloud REST API を使用して Excelワークシートから範囲の内容を取得する方法を学びます。リクエスト構文とサンプルコードを含みます。"
weight: 20
ArticleTitle: "Excelワークシートから範囲の内容を取得する方法 – Aspose.Cells Cloud API"
---

## Excelワークシートでの範囲の内容取得に関する操作

- [名前付き範囲に基づいてセルデータを取得する方法](/cells/ranges/get/values/)
- [Excelワークブックから名前付き範囲を取得する方法](/cells/ranges/get/name/)

**前提条件**

- 有効な Aspose Cloud アクセストークン（または OAuth 用の `client_id` / `client_secret`）。
- Excel ファイルは、対象のストレージフォルダにアップロードされていること。
- Aspose.Cells Cloud SDK バージョン 3.0 以降。

**範囲の取得（Get Range）** 操作は、ワークシート内の指定された範囲の内容を返します。  
これは単純な `GET` リクエストであり、範囲データを JSON 形式（または要求された他の形式）で返します。

**リクエスト概要**

| 要素 | 値 |
|------|-----|
| **HTTP メソッド** | `GET` |
| **エンドポイント** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **パスパラメータ** | `fileName` – Excel ファイル名（拡張子を含む）<br>`sheetName` – ワークシート名<br>`rangeName` – 範囲名（例：`A1:B10`） |
| **クエリパラメータ**（オプション） | `folder` – ストレージフォルダ<br>`storage` – ストレージ名<br>`outFormat` – 応答形式（例：`json`、`xml`） |
| **ヘッダー** | `Authorization: Bearer <access_token>`<br>`Accept: application/json` |

**サンプル cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**サンプル C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**サンプル Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**サンプル Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**応答スキーマ（JSON）**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**HTTP ステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | フィルターが正常に適用され、応答に操作の詳細が含まれます。 |
| 400 | Bad Request | 必須パラメータが欠落しているか、無効です（例：サポートされていないファイル形式）。 |
| 401 | Unauthorized | 無効または欠落している JWT トークン。 |
| 413 | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500 | Internal Server Error | 予期しないサーバーエラー。 |

- `200 OK` – 範囲が正常に取得されました。  
- `400 Bad Request` – 必須パラメータが欠落しているか、無効です。  
- `401 Unauthorized` – 無効または欠落しているアクセストークン。  
- `404 Not Found` – 指定されたファイル、ワークシート、または範囲が見つかりません。  
- `500 Internal Server Error` – 予期しないサーバーエラー。

**エラー応答の例**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "The request parameters are invalid or missing."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Invalid or missing access token."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "The specified file, worksheet, or range could not be found."
}
```

**関連項目**

- [名前付き範囲に基づいてセルデータを取得する方法](/cells/ranges/get/values/)  
- [Excelワークブックから名前付き範囲を取得する方法](/cells/ranges/get/name/)  
- [範囲の内容を更新する](/cells/ranges/update/)  
- [範囲を削除する](/cells/ranges/delete/)  
---