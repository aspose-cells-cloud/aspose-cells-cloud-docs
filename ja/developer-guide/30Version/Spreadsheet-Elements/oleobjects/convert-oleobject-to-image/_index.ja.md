---
title: "OLE オブジェクトを画像に変換 – Aspose.Cells Cloud REST API"
description: "Excelワークシートに埋め込まれたOLEオブジェクトを取得し、PNG、JPEG、TIFF、GIF、EMF、またはBMP形式に変換します。Aspose.Cells Cloud REST API を使用します。"
keywords:
  - "OLE オブジェクトを画像に変換"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "画像変換"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# OLE オブジェクトを画像に変換

ワークシートに埋め込まれたOLEオブジェクトを取得し、指定された画像形式で返します。

---

## 前提条件

このエンドポイントを呼び出す前に、以下の条件を満たしていることを確認してください。

1. **Aspose.Cells Cloud アカウント** – [Aspose Cloud ポータル](https://dashboard.aspose.cloud/) でアカウントを作成してください。  
2. **ワークブックをクラウドストレージにアップロード済み** – 「ファイルアップロード」API または Aspose Cloud UI を使用してください。  
3. **JWT アクセストークン** – [認証ガイド](/total/getting-started/rest-api-overview/authenticating-api-requests/) に従ってトークンを取得してください。  

---

## セキュリティと認証

すべての Aspose.Cells Cloud API は **JWT トークンベースの認証**を要求します。トークンは `Authorization` ヘッダーに含めてください。

```http
Authorization: Bearer <jwt-token>
```

HTTPS エンドポイントのみがサポートされます。`http://` は決して使用しないでください。

---

## リクエスト

### HTTP メソッド
`GET`

### エンドポイント
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### パスパラメーター

| 名前            | タイプ   | 必須 | 説明                                  |
|-----------------|----------|------|---------------------------------------|
| `name`          | 文字列   | ✅   | ワークブックファイル名 (例: `Book1.xlsx`) |
| `sheetName`     | 文字列   | ✅   | OLE オブジェクトを含むワークシート名     |
| `objectNumber`  | 整数     | ✅   | OLE オブジェクトの 0 から始まるインデックス |

### クエリパラメーター

| 名前           | タイプ   | 必須 | 説明                                                                 |
|----------------|----------|------|----------------------------------------------------------------------|
| `format`       | 文字列   | ❌   | 期望する画像形式 (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`)。省略した場合のデフォルトは `png` です。 |
| `folder`       | 文字列   | ❌   | ワークブックが存在するフォルダーのパス                              |
| `storageName`  | 文字列   | ❌   | ストレージサービス名 (例: `MyCloud`)                                |

---

## リクエスト例 (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*`<jwt-token>` を有効な JWT トークンに置き換えてください。*

---

## レスポンス

| ステータス | コンテンツ・タイプ          | 説明                                    |
|------------|-----------------------------|-----------------------------------------|
| `200`      | `image/png` (または指定された形式) | OLE オブジェクトを表すバイナリ画像データ     |
| `400`      | `application/json`          | 無効なリクエストパラメーター               |
| `401`      | `application/json`          | 認証失敗 (JWT トークンの不足・無効)          |
| `404`      | `application/json`          | 指定されたワークブック、ワークシート、OLE オブジェクトが見つかりません |
| `500`      | `application/json`          | サーバー側エラー                           |

### バイナリペイロードの処理

API は生の画像バイトを返します。以下のように処理できます。

* **直接ファイルに保存** (Linux/macOS の例):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **デバッグや JSON 内への埋め込み用に Base64 にエンコード**:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *例 (省略された) Base64 出力:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## エラーレスポンス

| HTTP ステータス | コード                   | メッセージ |
|-----------------|--------------------------|------------|
| `400`           | `InvalidParameter`       | 1 つ以上のリクエストパラメーターが無効です。 |
| `401`           | `AuthenticationFailed`   | JWT トークンが不足しているか、無効です。     |
| `404`           | `PropertyNotFound`       | 要求されたワークブック、ワークシート、OLE オブジェクトが存在しません。 |
| `500`           | `InternalError`          | サーバーで予期しないエラーが発生しました。   |

---

## SDK の例

以下のスニペットは、公式 SDK を使用してこの操作を呼び出す方法を示しています。`YOUR_JWT_TOKEN` とその他のプレースホルダーを実際の値に置き換えてください。

| 言語      | 例 |
|-----------|----|
| **C#** | <details><summary>コードを表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = \"YOUR_JWT_TOKEN\" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: \"Embedded_OleObject_Sample_Book1.xlsx\",\n    sheetName: \"Sheet1\",\n    objectNumber: 0,\n    format: \"png\"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create(\"oleobject.png\");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>コードを表示</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken(\"YOUR_JWT_TOKEN\");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    \"Embedded_OleObject_Sample_Book1.xlsx\",\n    \"Sheet1\",\n    0,\n    \"png\",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream(\"oleobject.png\")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>コードを表示</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = \"YOUR_JWT_TOKEN\"\nrequest = GetWorksheetOleObjectRequest(\n    name=\"Embedded_OleObject_Sample_Book1.xlsx\",\n    sheet_name=\"Sheet1\",\n    object_number=0,\n    format=\"png\"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>コードを表示</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>コードを表示</summary>```go\npackage main\nimport (\n    \"io\"\n    \"os\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = \"YOUR_JWT_TOKEN\"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         \"Embedded_OleObject_Sample_Book1.xlsx\",\n        SheetName:    \"Sheet1\",\n        ObjectNumber: 0,\n        Format:       \"png\",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create(\"oleobject.png\")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>コードを表示</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>コードを表示</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>コードを表示</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。)*

---

## 関連する操作

- **OLE オブジェクトの追加** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **OLE オブジェクトの更新** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE オブジェクトの削除** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE オブジェクト一覧の取得** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

詳細は、対応する API リファレンスページを参照してください。

---

## 補足リソース

- **OpenAPI 仕様** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **認証ガイド** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK リポジトリ** – <https://github.com/aspose-cells-cloud>
- **パフォーマンスとアクセシビリティ** – 最適な読み込み時間と WCAG 2.1 AA 準拠を確保するため、Lighthouse および axe‑core の監査を実行してください。

---