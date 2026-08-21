---
title: "Aspose.Cells Cloud API を使用して Excel ワークシートから列を削除する"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートから 1 つまたは複数の列を削除する方法を学びます。認証、リクエスト構文、パラメーター、レスポンス、エラー処理、および SDK サンプルを含みます。"
keywords: ["Aspose.Cells", "列の削除", "Excel API", "REST", "クラウド", "ワークシート", "列"]
date: 2026-07-30
api_version: "v3.0"
---

# Excel ワークシートから列を削除する

**エンドポイント**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

この操作は、ワークシートから単一の列または列の範囲を削除します。削除後、セル参照（数式を含む）を自動的に更新できます。

---

## 目次
1. [前提条件](#前提条件)  
2. [認証](#認証)  
3. [リクエスト URL と HTTP メソッド](#リクエスト-url-と-http-メソッド)  
4. [パラメーター](#パラメーター)  
   - [パスパラメーター](#パスパラメーター)  
   - [クエリパラメーター](#クエリパラメーター)  
5. [cURL の例](#curl-の例)  
6. [レスポンス](#レスポンス)  
7. [エラーコード](#エラーコード)  
8. [SDK サンプル](#sdk-サンプル)  
9. [その他の注意事項](#その他の注意事項)  

---

## 前提条件
- Aspose Cloud の認証フローによって取得した有効な **JWT アクセストークン**。  
- ワークブック (`{name}`) は、あらかじめ Aspose Cloud ストレージにアップロードされているか、`folder` / `storageName` クエリパラメーターでアクセス可能である必要があります。  

---

## 認証
Aspose.Cells Cloud のすべてのリクエストでは、**Bearer トークン**認証が必要です。

```http
Authorization: Bearer <access_token>
```

JWT トークンの取得方法の詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

---

## リクエスト URL と HTTP メソッド
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – ワークブックのファイル名（例: `test.xlsx`）。  
- **`{sheetName}`** – ワークシート名（例: `Sheet1`）。  
- **`{columnIndex}`** – 削除する最初の列の 0 から始まるインデックス。  

---

## パラメーター

| 名前                | 位置   | タイプ    | 必須   | 説明 |
|---------------------|--------|-----------|--------|------|
| **name**            | path   | string    | ✅ はい  | ワークブックのファイル名。 |
| **sheetName**       | path   | string    | ✅ はい  | ワークシート名。 |
| **columnIndex**     | path   | integer   | ✅ はい  | 削除する最初の列の 0 から始まるインデックス。 |
| **startColumn**     | query  | integer   | ❌ いいえ | 削除を開始する 0 から始まるインデックス。省略された場合、`columnIndex` の値が使用されます。 |
| **totalColumns**    | query  | integer   | ❌ いいえ | 削除する列数。省略された場合、`columnIndex` で指定された列のみが削除されます。 |
| **updateReference** | query  | boolean   | ❌ いいえ | `true` の場合、削除後にワークブック全体のセル参照（数式を含む）を自動的に更新します。 |
| **folder**          | query  | string    | ❌ いいえ | ワークブックが含まれるフォルダーのパス。 |
| **storageName**     | query  | string    | ❌ いいえ | Aspose Cloud ストレージサービスの名前。 |

> **注意** – 低レベル API 仕様に示されている `columns` パラメーターは、より表現力のある `startColumn` および `totalColumns` クエリパラメーターに置き換えられました。後方互換性のため、両方のアプローチがサポートされています。

---

## cURL の例

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### 説明
- `test.xlsx` の `Sheet1` から列 **B** (`columnIndex = 1`) を削除します。  
- `startColumn=1` および `totalColumns=1` は、単一列の削除を指定します。  
- `updateReference=true` により、数式やその他の参照が自動的に調整されます。

---

## レスポンス

| HTTP コード | 説明 | 例 |
|-------------|------|-----|
| **200** | 成功 – 列が削除されました。 | `{ "Code": 200, "Status": "OK" }` |
| **400** | 不正リクエスト – パラメーターが不足または無効です。 | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401** | 認証失敗 – JWT トークンが不足または無効です。 | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | 見つかりません – ワークブックまたはワークシートが存在しません。 | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500** | サーバー内部エラー – サーバーで予期しない状態が発生しました。 | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

レスポンスボディは、共通の **`CellsCloudResponse`** モデルに従います。

---

**HTTP ステータスコード**

| コード | 意味                      | 説明                                           |
|--------|---------------------------|------------------------------------------------|
| 200    | OK                        | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request               | パラメーターが不足または無効です（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized              | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error     | 予期しないサーバーエラーが発生しました。 |

---

## SDK サンプル

以下は、最もよく使われる SDK 用の実行可能なスニペットです。プレースホルダー値（`<YOUR_ACCESS_TOKEN>`、`<WORKBOOK>` など）を、各自のデータで置き換えてください。

| 言語       | サンプル |
|------------|----------|
| **C#** | <details><summary>コードを表示</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>コードを表示</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>コードを表示</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>コードを表示</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>コードを表示</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>コードを表示</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>コードを表示</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>コードを表示</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*すべての SDK は、`access_token` が設定された場合、自動的に必要な `Authorization` ヘッダーを追加します。*

---

## その他の注意事項

### セキュリティヘッダー（本番環境で推奨）
ドキュメントページを提供する際には、セキュリティを強化するために以下の HTTP レスポンスヘッダーを含めてください。

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### パフォーマンスに関するヒント
- サードパーティの分析スクリプト (`gtag.js`、`containerize.js`) は、`async` 属性で読み込むか、ページ描画完了後に遅延読み込みしてください。  
- カスタム JavaScript/CSS バンドルは圧縮してください。  
- レンダリングをブロックする小さな SVG アイコンについては、事前読み込みしてください：

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO 向上（JSON‑LD）

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Delete Column from Excel Worksheet using Aspose.Cells Cloud API",
  "description": "Learn how to delete one or more columns from an Excel worksheet via Aspose.Cells Cloud REST API.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Delete Column", "Excel", "REST API"]
}
```

このスニペットを HTML の `<head>` 内に `<script type="application/ld+json">` ブロックとして挿入してください。

### アクセシビリティ
- 装飾用のすべての画像は `alt=""` を使用するか、`aria-hidden="true"` で隠されています。  
- Open Graph 画像には、完全性を確保するために meta タグ内に `alt` 属性が追加されています。  

---

## 関連項目
- [DeleteWorksheetColumns の OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [認証の概要](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [GitHub 上の Aspose.Cells Cloud SDK](https://github.com/aspose-cells-cloud)  

---