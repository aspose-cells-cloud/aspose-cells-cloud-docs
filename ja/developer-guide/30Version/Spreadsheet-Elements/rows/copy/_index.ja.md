---
title: "Excelワークシートの行をコピーする"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excelワークシート内の特定の行全体からデータと書式をコピーします。認証、リクエスト/レスポンスの詳細、エラーハンドリング、およびSDKの使用例を含みます。"
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Excelワークシートの行をコピーする <span style="float:right;">v3.0</span>

ワークシート内の特定の行全体からデータと書式をコピーします。

---

## 前提条件

| # | 必要条件 |
|---|----------|
| 1 | 有効な **JWT** トークンが必要です。詳しくは[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)をご覧ください。 |
| 2 | ワークブック（`{name}`）は、選択された**フォルダ**／**ストレージ**内に既に存在している必要があります。 |
| 3 | 対象のワークシート（`{sheetName}`）がワークブック内に存在している必要があります。 |
| 4 | （任意）ファイルがデフォルトの場所にない場合は、**フォルダ**と**storageName**を事前に確認してください。 |

---

## エンドポイント

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*すべてのパスパラメータは大文字と小文字を区別します。*

### パスパラメータ

| パラメータ | 型     | 必須 | 説明 |
|------------|--------|------|------|
| `name`     | 文字列 | ✅  | ワークブックのファイル名（例：`test.xlsx`）。 |
| `sheetName` | 文字列 | ✅  | ワークシート名（例：`Sheet1`）。 |

### クエリパラメータ

| パラメータ            | 型      | 必須 | 説明 |
|-----------------------|---------|------|------|
| `sourceRowIndex`      | 整数    | ✅  | コピー元の行の 0 から始まるインデックス。 |
| `destinationRowIndex` | 整数    | ✅  | 行をコピーする先の 0 から始まるインデックス。 |
| `rowNumber`           | 整数    | ✅  | コピーする行数。 |
| `worksheet`           | 文字列  | ❌  | ワークシート識別子。通常は **sheetName** と同じです。 |
| `folder`              | 文字列  | ❌  | ワークブックが格納されているフォルダのパス。 |
| `storageName`         | 文字列  | ❌  | ストレージサービスの名前。 |

---

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意**  
> `<jwt token>` の部分を、認証サービスから取得した有効な JWT トークンに置き換えてください。

---

## 成功時のレスポンス

| コード | 説明 |
|--------|------|
| **200** | 行のコピーが正常に完了しました。 |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

レスポンスボディは `CellsCloudResponse` 型のインスタンスです。

---

## エラーハンドリング

| HTTP コード | 意味                                     | 例：レスポンスボディ |
|-------------|------------------------------------------|----------------------|
| **400**     | Bad Request – 必須パラメータの欠落または無効なパラメータ。 | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**     | Unauthorized – 無効または欠落している JWT トークン。 | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | Not Found – ワークブックまたはワークシートが存在しません。 | `{ "Code": 404, "Message": "File not found." }` |
| **500**     | Internal Server Error – サーバー側で予期しないエラーが発生しました。 | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**対応ガイドライン**

* **400** – 必須クエリパラメータがすべて正しく指定されているか確認してください。  
* **401** – JWT トークンを再生成または更新してください。  
* **404** – ワークブックおよびワークシート名が正しいか、またファイルが指定されたフォルダ／ストレージ内に存在するか確認してください。  
* **500** – 少し待ってから再試行してください。問題が継続する場合は Aspose のサポートへお問い合わせください。  

---

## SDKの使用例

以下のスニペットは、公式 Aspose.Cells Cloud SDK を使用して **行のコピー** 操作を呼び出す方法を示しています。

| 言語 | 例 |
|------|----|
| **C#**   | <details><summary>コードを表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi(\"clientId\", \"clientSecret\");\nawait api.PostCopyWorksheetRowsAsync(name: \"test.xlsx\", sheetName: \"Sheet1\", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>コードを表示</summary>```java\nCellsApi api = new CellsApi(\"clientId\", \"clientSecret\");\napi.postCopyWorksheetRows(\"test.xlsx\", \"Sheet1\", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>コードを表示</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>コードを表示</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>コードを表示</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>コードを表示</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>コードを表示</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>コードを表示</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*完全なソースファイルは [Aspose‑Cells‑Cloud GitHub リポジトリ](https://github.com/aspose-cells-cloud) で公開されています。*

---

## 関連情報

- [Excelワークシートに行を追加する](/rows/add/)  
- [Excelワークシートの行を削除する](/rows/delete/)  
- [Excelワークシートの行を更新する](/rows/update/)  

--- 

*このページは **{{DATE}}** に生成されました。この API の最新版については、[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows) を参照してください。*