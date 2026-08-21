---
title: "AutoFilter の取得"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートから AutoFilter の説明を取得します。"
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /ja/cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# ワークシートから AutoFilter の説明を取得する

**バージョン:** v3.0  
**エンドポイント:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **注意:** すべてのサンプルリクエストは **HTTPS** を使用します。JWT トークンを安全でない接続経由で送信しないでください。

---

## 概要

**AutoFilter** を使用すると、ユーザーは列の値、色、カスタム条件などを基にワークシートの行をフィルタリングできます。この API は、フィルタリング対象の列、範囲、並べ替えの詳細など、AutoFilter の完全な設定情報を返します。これにより、フィルタ設定をプログラムで確認または再現できます。

---

## 前提条件

| 必要条件 | 説明 |
|---------|------|
| **認証** | 有効な JWT トークンが必要です。詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。 |
| **ファイルの場所** | ワークブックは Aspose Cloud ストレージ（または接続された外部ストレージ）に保存されている必要があります。 |
| **サポートされるフォーマット** | Aspose.Cells でサポートされる任意の Excel 形式（例: `.xlsx`, `.xls`, `.xlsm`）。 |
| **SDK（任意）** | SDK を使用する場合は、適切なパッケージをインストールしてください（例: .NET の場合 `dotnet add package Aspose.Cells-Cloud`）。 |

---

## リクエスト

### HTTP リクエスト

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### パスパラメータ

| パラメータ名 | 型     | 説明 |
|-------------|--------|------|
| `name`      | string | **必須。** 拡張子を含むワークブックファイル名。 |
| `sheetName` | string | **必須。** AutoFilter を取得するワークシート名。 |

### クエリパラメータ

| パラメータ名  | 型     | 説明 |
|--------------|--------|------|
| `folder`      | string | ワークブックが配置されているストレージ内のフォルダーパス。 |
| `storageName` | string | 使用するストレージ名。 |

### セキュリティ

API は **JWT トークンベースの認証** を使用します。トークンは `Authorization` ヘッダに含めてください：

```http
Authorization: Bearer <your_jwt_token>
```

---

## リクエスト例（cURL）

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## レスポンス

サービスは `AutoFilter` モデルをラップした JSON オブジェクトを返します。

### 成功時のレスポンススキーマ

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### レスポンス例

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**HTTP ステータスコード**

| コード | 意味               | 説明 |
|-------|--------------------|------|
| 200   | OK                 | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400   | Bad Request        | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401   | Unauthorized       | JWT トークンが無効または不足しています。 |
| 413   | Payload Too Large  | アップロードされたファイルがサイズ制限を超えています。 |
| 500   | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

---

## SDK の例

この操作は、すべての Aspose.Cells Cloud SDK で利用可能です。以下は、すぐに実行できるコードスニペットです。

| 言語 | 例 |
|------|----|
| **C#** | <details><summary>コードを表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>コードを表示</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>コードを表示</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>コードを表示</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>コードを表示</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>コードを表示</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>コードを表示</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>コードを表示</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

SDK の完全なリストおよびインストール手順については、[Aspose.Cells Cloud GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

---

## 関連項目

- [AutoFilter – OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [ストレージ操作](https://docs.aspose.cloud/cells/storage/)  

---