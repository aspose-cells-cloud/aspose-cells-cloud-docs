---
title: "Excel で範囲内の行の高さを設定する – Aspose.Cells Cloud API（v3.0）"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークシート内の特定の範囲の行の高さを変更します。エンドポイント、パラメータ、cURL の例、サンプル応答、および複数言語向けの SDK スニペットを含みます。"
keywords: "Aspose.Cells, 行の高さ, 範囲, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Excel で範囲内の行の高さを設定する

この操作は、Aspose Cloud ストレージ内に保存されたワークシート上の指定された範囲の行の高さを更新します。

## 前提条件 / 認証

**Cells.ReadWrite** スコープ付きの JWT アクセストークンを Aspose Cloud OAuth サービスから取得し、すべてのリクエストの `Authorization` ヘッダーにトークンを含める必要があります。

```http
Authorization: Bearer <jwt token>
```

トークンをまだ取得していない場合は、「**Aspose Cloud 認証ガイド**」に従ってトークンをリクエストしてください。

## HTTP リクエスト

| メソッド | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### パスパラメータ

| 名前 | 型 | 説明 |
|------|------|-------------|
| `name` | `string` | **必須。** クラウド上に保存されている Excel ファイルの名前。 |
| `sheetName` | `string` | **必須。** 対象となる範囲を含むワークシート名。 |

### クエリパラメータ

| 名前 | 型 | 必須 | 説明 |
|------|------|----------|-------------|
| `value` | `number` | **はい** | 範囲に適用する希望の行の高さ（ポイント単位）。 |
| `folder` | `string` | いいえ | ファイルが配置されているストレージ内のフォルダーパス。 |
| `storageName` | `string` | いいえ | 使用するストレージサービスの名前（複数のストレージが設定されている場合）。 |

### リクエストボディ（JSON）

ボディには、どの行が影響を受けるかを定義する **Range** オブジェクトを含める必要があります。

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Range JSON スキーマ

| プロパティ | 型 | 必須 | 説明 |
|----------|------|----------|-------------|
| `FirstRow` | integer | **はい** | 範囲内の最初の行の 0 から始まるインデックス。 |
| `RowCount` | integer | **はい** | 高さを適用する行の数。 |
| `FirstColumn` | integer | いいえ | 最初の列の 0 から始まるインデックス（行の高さ設定のみの場合は省略可能）。 |
| `ColumnCount` | integer | いいえ | 範囲がまたがる列の数（省略可能）。 |

上記のプロパティのみが行の高さ設定操作で使用されます。追加のフィールドは無視されます。

## サンプルリクエスト

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### サンプル応答（成功）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。応答には操作の詳細が含まれます。 |
| 400  | Bad Request                 | 必須パラメータが不足しているか、無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足している。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えた。 |
| 500  | Internal Server Error       | 予期しないサーバーエラー。 |

すべての応答には数値の `Code` と人間が読める `Status`（エラーの場合は `Message`）が含まれます。エラーが発生した場合、追加で `ErrorDetails` が提供される場合があります。

## SDK の例

以下のスニペットは、公式の Aspose.Cells Cloud SDK を使用して **範囲の行の高さ設定** を呼び出す方法を示しています。

| 言語 | 例 |
|----------|---------|
| **C#** | <details><summary>コードを表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>コードを表示</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>コードを表示</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>コードを表示</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>コードを表示</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>コードを表示</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>コードを表示</summary>```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"context\"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = \"<jwt token>\"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ \"FirstRow\": 9, \"RowCount\": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), \"test.xlsx\", \"Sheet1\", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>コードを表示</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **注意:** すべての SDK は、アクセストークンが設定されている場合に自動的に必須の `Authorization: Bearer` ヘッダーを追加します。

## 関連項目

- **OpenAPI スペシフィケーション** – この操作の詳細な契約： <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK リポジトリ** – ソースコードおよび追加の言語バインディング： <https://github.com/aspose-cells-cloud>
- **認証ガイド** – JWT トークンの取得方法： <https://docs.aspose.cloud/cells/authentication/>

---