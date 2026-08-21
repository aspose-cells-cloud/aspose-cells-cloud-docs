---
title: Excelワークシート内のすべてのOLEオブジェクトを削除する
description: Aspose.Cells Cloud REST API（v3.0）を使用して、ExcelワークシートからすべてのOLE（オブジェクトの埋め込みとリンク）オブジェクトを削除する方法を学びます。エンドポイント、パラメータ、リクエスト／レスポンスの例、SDKスニペット、認証、エラー処理、FAQを含みます。
keywords: Aspose.Cells Cloud, OLEオブジェクトの削除, Excel API, REST API, ワークシートOLEクリア, クラウドSDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Excelワークシート内のすべてのOLEオブジェクトを削除する

**OleObjects – Clear** は、指定されたワークシートからすべてのOLE（オブジェクトの埋め込みとリンク）オブジェクトを削除し、セルデータはそのまま残します。この操作は、レガシースプレッドシートをクリーンアップしたり、ワークブックを再配布する準備をしたりする際に便利です。

---

## 前提条件

- 有効な **Aspose Cloud JWT アクセストークン**（OAuth 2.0）  
- 対象のワークブックは Aspose Cloud ストレージ内に保存されていること（または、存在する `folder`／`storageName` を指定すること）  
- API バージョン **v3.0** 以上  

> **注意:** この操作は *冪等性* を持ちます。OLEオブジェクトが既に存在しないワークシートに対して実行しても、成功応答 `200 OK` が返されます。

---

## HTTP リクエスト

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### パスパラメータ

| 名前         | タイプ   | 必須 | 説明                     |
|--------------|----------|------|--------------------------|
| `name`       | 文字列   | ✔️   | ワークブックファイル名   |
| `sheetName`  | 文字列   | ✔️   | ワークシート名           |

### クエリパラメータ

| 名前            | タイプ   | 必須 | 説明                                         |
|-----------------|----------|------|----------------------------------------------|
| `folder`        | 文字列   | 任意 | ワークブックを含むフォルダ                   |
| `storageName`   | 文字列   | 任意 | ワークブックが保存されているストレージ名     |

**ヘッダー**

| ヘッダー名           | 値                            |
|----------------------|-------------------------------|
| `Authorization`      | `Bearer <jwt token>`          |
| `Accept`             | `application/json`            |
| `Content-Type`       | `application/json`            |

---

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*`<jwt token>` を有効なアクセストークンに置き換え、必要に応じて `folder`／`storageName` を調整してください。*

---

## 成功時のレスポンス

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明                                                     |
|--------|------------------|----------------------------------------------------------|
| 200    | OK               | フィルターが正常に適用された；レスポンスには操作の詳細が含まれる |
| 400    | Bad Request      | パラメータが不足または不正（例：サポートされないファイル形式） |
| 401    | Unauthorized     | JWT トークンが無効または不足                             |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えた           |
| 500    | Internal Server Error | サーバー側で予期せぬエラーが発生                         |

---

## SDK サンプル

以下のコードスニペットは、公式 Aspose.Cells Cloud SDK を使用して **DeleteWorksheetOleObjects** を呼び出す方法を示しています。プレースホルダー値（`<YOUR_TOKEN>`、`<FILE_NAME>` など）を実際のデータに置き換えてください。

| 言語     | サンプル |
|----------|----------|
| **C#** | <details><summary>C# の例を表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Java の例を表示</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Python の例を表示</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Node.js の例を表示</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Go の例を表示</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("All OLE objects deleted")\n}\n```</details> |

*すべてのサポート言語の完全なソースファイルは [Aspose.Cells Cloud GitHub リポジトリ](https://github.com/aspose-cells-cloud) で公開されています。*

---

## エラーと対処

- **冪等性** – 既にOLEオブジェクトが存在しないワークシートで削除操作を実行しても、`200 OK` が返されます。  
- **トークンの有効期限切れ** – `401 Unauthorized` が返された場合は、新しい JWT トークンを取得して再試行してください。  
- **無効なワークシート名** – ワークブック内のワークシート名と大文字・小文字を完全に一致させる必要があります。一致しない場合、`400 Bad Request` が返されます。  

一時的な `500` エラーに対しては、指数バックオフ方式のリトライ処理を実装してください。

---

## FAQ

**Q1: `folder` および `storageName` パラメータを指定する必要がありますか？**  
**A:** いいえ。指定しない場合、Aspose Cloud はデフォルトストレージとルートフォルダを前提とします。

**Q2: 特定のセルからOLEオブジェクトのみを削除することは可能ですか？**  
**A:** このエンドポイントはワークシート内の**すべての**OLEオブジェクトを削除します。単一のオブジェクトを削除するには、「特定のOLEオブジェクトの削除」操作を使用してください。

**Q3: 編集のためにワークブックがロックされている場合、どうなりますか？**  
**A:** API は `400 Bad Request` を返し、ファイルがロックされている旨のメッセージを含めます。エンドポイントを呼び出す前に、ファイルが他の場所で開かれていないことを確認してください。

**Q4: ワークブックのサイズ制限はありますか？**  
**A:** サービスは Aspose Cloud 全体のファイルサイズ制限に従います（現時点で1ファイルあたり最大2 GB）。それより大きいファイルは分割またはチャンク処理が必要になる場合があります。

---

## ベストプラクティス

- **パフォーマンス** – ドキュメントサイトでサードパーティのスクリプトを読み込む際は、初期ページロード時間を短縮するため `async` または `defer` 属性を使用してください。  
- **セキュリティ** – 新しいタブで開く外部リンクには `rel="noopener noreferrer"` を追加してください。  
- **アクセシビリティ** – 装飾目的のアイコン（例：サイドバーの下向き矢印）には、WCAG AA 標準を満たすために `alt=""` および `role="presentation"` を設定してください。  
- **一貫性** – エンコーディングのアーティファクトを避けるため、日付形式は ISO‑8601（`YYYY‑MM‑DD`）形式を維持してください。  

---

## 関連する操作

- **OLEオブジェクトの追加** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **特定のOLEオブジェクトの削除** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

ページ下部のナビゲーションリンクを使用して、関連する API 操作間を移動してください。

---