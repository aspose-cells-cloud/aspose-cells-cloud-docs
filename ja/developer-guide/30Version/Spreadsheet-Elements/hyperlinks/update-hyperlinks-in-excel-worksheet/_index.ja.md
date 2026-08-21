---
title: "Excelワークシート内のハイパーリンクを更新する – Aspose.Cells Cloud APIガイド"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークシート内のハイパーリンクを更新する方法を学びます。エンドポイント、パラメータ、リクエスト本文のスキーマ、cURLのサンプル、SDKコードスニペット、エラーハンドリング、レート制限、前提条件を含みます。"
keywords:
  - "Aspose.Cells"
  - "ハイパーリンク更新"
  - "Excel API"
  - "REST API"
  - "クラウドスプレッドシート"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Excelワークシート内のハイパーリンクを更新する  

**APIバージョン:** v3.0  

**PostWorksheetHyperlink** 操作は、0から始まるインデックスで識別されるワークシート内の既存のハイパーリンクを更新します。

---

## 目次
1. [前提条件](#前提条件)  
2. [レート制限](#レート制限)  
3. [エンドポイント](#エンドポイント)  
4. [パラメータ](#パラメータ)  
   - [パスパラメータ](#パスパラメータ)  
   - [クエリパラメータ](#クエリパラメータ)  
   - [リクエスト本文のスキーマ](#リクエスト本文のスキーマ)  
5. [レスポンス](#レスポンス)  
   - [成功レスポンス](#成功レスポンス)  
   - [エラーレスポンス](#エラーレスポンス)  
6. [cURLの例](#curlの例)  
7. [SDKコードスニペット](#sdkコードスニペット)  
8. [関連情報](#関連情報)  

---

## 前提条件 <a name="前提条件"></a>

| 要件 | 説明 |
|------|------|
| **認証** | JWTトークンベースの認証。トークンの取得方法については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を参照してください。 |
| **ストレージ** | ワークブックは、サポートされているAspose Cloudストレージ（デフォルトは **Default**）に保存されている必要があります。 |
| **権限** | JWTトークンには、対象のワークブックを読み取りおよび書き込みする権限が必要です。 |
| **ヘッダー** | すべてのリクエストで `Content-Type: application/json` および `Accept: application/json` が必要です。 |

---

## レート制限 <a name="レート制限"></a>

Aspose.Cells Cloudでは、**アクセストークンごとに最大60回/分**のリクエストが許可されています。この制限を超えると、HTTP **429 Too Many Requests** が返されます。レート制限が発生した場合、指数バックオフを実装するか、`Retry-After` ヘッダーに従ってください。

---

## エンドポイント <a name="エンドポイント"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*ファイル `name` のワークシート `sheetName` 内の `hyperlinkIndex` で識別されるハイパーリンクを更新します。*

---

## パラメータ <a name="パラメータ"></a>

### パスパラメータ <a name="パスパラメータ"></a>

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| `name` | 文字列 | ✅ | Excelファイル名（拡張子を含む）。 |
| `sheetName` | 文字列 | ✅ | ハイパーリンクを含むワークシート名。 |
| `hyperlinkIndex` | 整数 | ✅ | 更新するハイパーリンクの0から始まるインデックス。 |

### クエリパラメータ <a name="クエリパラメータ"></a>

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| `folder` | 文字列 | ❌ | ワークブックが存在するストレージ内のフォルダーパス。 |
| `storageName` | 文字列 | ❌ | ストレージサービス名（例: `Default`）。 |

### リクエスト本文のスキーマ <a name="リクエスト本文のスキーマ"></a>

リクエスト本文には **`hyperlink`** オブジェクトを含める必要があります。変更したいフィールドのみを指定してください。省略されたオプションフィールドは、既存の値が保持されます。

| フィールド | 型 | 必須 | 説明 |
|----------|----|------|------|
| `Address` | 文字列 | ✅ | ハイパーリンクの宛先URL。 |
| `Area` | オブジェクト | ✅ | ハイパーリンクが配置されているセル範囲。`StartRow`、`StartColumn`、`EndRow`、`EndColumn`（すべて整数、0から始まるインデックス）を含む必要があります。 |
| `ScreenTip` | 文字列 | ❌ | マウスオーバー時に表示されるツールチップ。 |
| `TextToDisplay` | 文字列 | ❌ | セル内に表示されるテキスト。 |
| `link` | オブジェクト | ❌ | ハイパーメディアリンク（`Href`、`Rel`、`Title`、`Type`）。通常、リクエストペイロードでは省略します。 |

**`Area` オブジェクトの定義**

| サブフィールド | 型 | 必須 | 説明 |
|---------------|----|------|------|
| `StartRow` | 整数 | ✅ | 0から始まる開始行インデックス。 |
| `StartColumn` | 整数 | ✅ | 0から始まる開始列インデックス。 |
| `EndRow` | 整数 | ✅ | 0から始まる終了行インデックス。 |
| `EndColumn` | 整数 | ✅ | 0から始まる終了列インデックス。 |

---

## レスポンス <a name="レスポンス"></a>

### 成功レスポンス <a name="成功レスポンス"></a>

| フィールド | 型 | 説明 |
|----------|----|------|
| `Code` | 整数 | HTTPステータスコード（成功時は200）。 |
| `Status` | 文字列 | ステータスのテキスト（`OK`）。 |
| `Hyperlink` | オブジェクト（オプション） | 更新されたハイパーリンクオブジェクト。`link` サブオブジェクトが要求された場合に返されます。 |

**JSONの例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### エラーレスポンス <a name="エラーレスポンス"></a>

| HTTPコード | 理由 | 例（ボディ） |
|-----------|------|--------------|
| **400** | 不正リクエスト – パラメータが不足または無効。 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | 認証エラー – JWTトークンが不足または無効。 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | 見つからない – ワークブック、ワークシート、またはハイパーリンクが存在しない。 | `{ "Code":"404", "Message":"File not found." }` |
| **429** | 多すぎるリクエスト – レート制限を超過。 | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | サーバー内部エラー – 予期しないサーバーエラー。 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## cURLの例 <a name="curlの例"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**レスポンス**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*ヒント:* JSONペイロードをファイル（例: `payload.json`）に保存し、`--data @payload.json` で参照すると、コピー＆ペーストが容易になります。

---

## SDKコードスニペット <a name="sdkコードスニペット"></a>

以下のスニペットは、公式Aspose.Cells Cloud SDKを使用して **PostWorksheetHyperlink** を呼び出す方法を示しています。プレースホルダー（`<YOUR_JWT_TOKEN>`、`<FILE_NAME>` など）を実際の値に置き換えてください。

| 言語 | サンプル |
|------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*すべてのSDKはオープンソースであり、[Aspose.Cells Cloud GitHubリポジトリ](https://github.com/aspose-cells-cloud)で公開されています。*

---

## 関連情報 <a name="関連情報"></a>

- **認証** – [JWTトークンによる始めてのガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **ストレージ操作** – [ファイルのアップロード](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **その他のハイパーリンク操作** – [ハイパーリンクの追加](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) \| [ハイパーリンクの削除](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI仕様** – エンドポイントの完全な定義: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*最終更新日: 2026‑07‑30*