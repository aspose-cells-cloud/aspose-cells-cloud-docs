---
title: "Excelワークシートの表示制御の使い方"
second_title: "Document"
linktitle: "表示制御"
type: docs
url: /ja/worksheets/panes/
keywords: "Aspose.Cells Cloud, ワークシート非表示 API, ワークシート表示復元 API, Excel ワークシートの表示設定, REST API Excel, Aspose.Cells v3.0"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートをプログラムで非表示または表示復元する方法を学びます。リクエスト URL、cURL および .NET SDK のサンプル、エラー処理、バージョン固有の注意事項を含みます。"
weight: 20
---

## Excelワークシートの表示制御の使い方

*ワークシートの表示制御* とは、シートをエンドユーザーに表示するかどうかを定義します。Aspose.Cells Cloud を使用すると、シンプルな REST コールでワークシートを非表示または表示復元できます。使用する API エンドポイントは以下の通りです。

* **ワークシートを非表示にする** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **ワークシートを表示復元する** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **対応 API バージョン:** **v3.0**（2026年3月現在）

### 前提条件
1. 有効な **Aspose.Cells Cloud** アカウント。  
2. 有効な **クライアント ID** および **クライアント シークレット**（または OAuth 2.0 アクセストークン）。  
3. ワークブック（`{fileName}`）がすでに Aspose クラウドストレージにアップロードされていること。  

---

## ワークシートを非表示にする

### リクエスト
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### レスポンス
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### サンプル cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### サンプル .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"ワークシートが非表示になりました: {response.Worksheet.Visible}");
```

### よくあるエラー
| HTTP コード | 説明                                     | 対処方法                                                   |
|------------|------------------------------------------|------------------------------------------------------------|
| 400        | 無効な JSON ボディ、または `Visible` キーの欠如 | リクエストボディが有効な JSON で、キーが含まれていることを確認してください。 |
| 401        | 認証エラー – トークンの未指定または期限切れ | OAuth トークンを再生成し、ヘッダーに含めてください。         |
| 404        | ワークシートまたはファイルが見つかりません | `{fileName}` および `{sheetName}` が正しいことを確認してください。 |
| 409        | 既に非表示になっているワークシート          | リクエスト送信前に現在の表示状態を確認してください。         |

---

## ワークシートを表示復元する

### リクエスト
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### レスポンス
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### サンプル cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### サンプル .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"ワークシートが表示されました: {response.Worksheet.Visible}");
```

### よくあるエラー
| HTTP コード | 説明                                     | 対処方法                                                   |
|------------|------------------------------------------|------------------------------------------------------------|
| 400        | 無効な JSON ボディ、または `Visible` キーの欠如 | `"Visible": true` を含む正しい JSON ペイロードを提供してください。 |
| 401        | 認証エラー – トークンの未指定または期限切れ | アクセストークンを再生成して再試行してください。             |
| 404        | ワークシートまたはファイルが見つかりません | ストレージ内にファイル名およびシート名が存在することを確認してください。 |
| 409        | 既に表示されているワークシート              | 特に操作は不要です。ワークシートはすでに表示状態です。       |

---

## 関連する操作
> *ペインの固定* | *ペインの分割* | *ズーム* – 詳細なワークシートレイアウト制御については、対応するページをご参照ください。

---

## よくある質問

<dl>
  <dt>Aspose.Cells Cloud API を使用してワークシートを非表示にする方法は？</dt>
  <dd>`PUT` リクエストを `/cells/{fileName}/worksheets/{sheetName}/visibility` に送信し、JSON ボディに `{ "Visible": false }` を指定します。有効な OAuth 2.0 ベアラートークンをヘッダーに含めてください。`200 OK` レスポンスとともに更新されたワークシートオブジェクトが返されます。</dd>

  <dt>ワークシートを表示復元した後のレスポンス内容は？</dt>
  <dd>API は `200 OK` を返し、ペイロードに `"Visible": true` を含むワークシートオブジェクトを含みます。レスポンスにはワークシートの `Name`、`Index`、および `Visible` プロパティが含まれます。</dd>

  <dt>1回の呼び出しで複数のワークシートを非表示にできますか？</dt>
  <dd>いいえ。表示制御エンドポイントは `{sheetName}` で指定された単一のワークシートに対してのみ機能します。複数のシートを非表示にする場合、クライアントコード内で各シート名をループ処理してください。</dd>
</dl>

---

*Aspose Docs チームによって執筆 – 15年以上にわたり Excel ワークフローの自動化に携わっています。*