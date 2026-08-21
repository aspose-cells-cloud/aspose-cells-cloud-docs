---
title: Aspose.Cells Cloud API を使用して Excel ワークシートに動的フィルターを追加する
description: Aspose.Cells Cloud REST API を使用して、Excel ワークシートに動的フィルター（例：BelowAverage、Tomorrow、LastMonth）を適用する方法を学びます。認証、リクエスト構文、パラメーター、レスポンス処理、および複数言語の SDK サンプルを含みます。
keywords: Aspose.Cells, 動的フィルター, Excel API, REST, 自動フィルター, クラウド SDK
slug: add-dynamic-filter
api_version: v3.0
---

## 概要

**PutWorksheetDynamicFilter** 操作は、Excel ワークシート内の指定された範囲に動的フィルターを追加します。  
動的フィルターは、日付、平均値、空白などの値を自動的に評価するため、カスタム数式を記述せずに「スマート」な表示を作成できます。

## 前提条件

| 必要条件 | 詳細 |
|---------|------|
| **認証** | `/connect/token` エンドポイントから取得した有効な JWT トークン。`Authorization: Bearer <token>` ヘッダーに含めてください。 |
| **ストレージ** | ワークブックは Aspose Cloud ストレージの場所（デフォルトまたはカスタムストレージ）に配置されている必要があります。 |
| **サポートされているファイル形式** | `.xlsx`、`.xls`、`.xlsm`、`.xlsb`、`.csv` など。 |
| **権限** | 対象のフォルダー／ファイルに対する読み書きアクセス権。 |

## HTTP リクエスト

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### パスパラメーター

| パラメーター | 型 | 必須 | 説明 |
|-------------|----|------|------|
| `name` | 文字列 | ✅ | Excel ワークブックの名前（例：`Book1.xlsx`）。 |
| `sheetName` | 文字列 | ✅ | フィルターを適用する範囲を含むワークシートの名前。 |

### クエリパラメーター

| パラメーター | 型 | 必須 | 説明 |
|-------------|----|------|------|
| `range` | 文字列 | ✅ | フィルターを適用するセル範囲（例：`A1:B1`）。 |
| `fieldIndex` | 整数 | ✅ | 動的フィルターを適用する範囲内の列の 0 から始まるインデックス。 |
| `dynamicFilterType` | 文字列 | ✅ | 適用する動的フィルターの種類（**サポートされている動的フィルターの種類**を参照）。 |
| `matchBlanks` | 真偽値 | ❌ | `true` の場合、空白セルをフィルター結果に含めます。デフォルト：`false`。 |
| `refresh` | 真偽値 | ❌ | `true` の場合、フィルター適用後にオートフィルターを更新します。 |
| `folder` | 文字列 | ❌ | ワークブックが配置されているストレージ内のフォルダーへのパス。 |
| `storageName` | 文字列 | ❌ | 使用する Aspose Cloud ストレージの名前。 |

### リクエストボディ

リクエストボディは空の JSON オブジェクトです：

```json
{}
```

## サポートされている動的フィルターの種類

| 値 | 意味 |
|----|------|
| `BelowAverage` | その列の平均値より小さい値を持つ行。 |
| `AboveAverage` | その列の平均値より大きい値を持つ行。 |
| `Tomorrow` | 日付が翌日の日付と一致する行。 |
| `Yesterday` | 日付が前日の日付と一致する行。 |
| `NextWeek` | 日付が翌週のカレンダー週に含まれる行。 |
| `LastMonth` | 日付が前月のものである行。 |
| `ThisYear` | 日付が今年のものである行。 |

## サンプルリクエスト（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT リクエストは空の JSON ボディを持ちます
```

## サンプルレスポンス

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "動的フィルターが正常に適用されました。"
}
```

**HTTP ステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400 | Bad Request | パラメーターが不足または無効（例：サポートされていないファイル形式）です。 |
| 401 | Unauthorized | JWT トークンが無効または不足しています。 |
| 413 | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500 | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

## SDK サンプル

以下は、最も人気のある SDK の実行可能なスニペットです。`YOUR_JWT_TOKEN`、`YOUR_FILE_NAME` などのプレースホルダーを実際の値に置き換えてください。

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | ワークブック名。
var sheetName = "Sheet1"; // string | ワークシート名。
var range = "A1:B1"; // string | フィルターを適用する範囲。
var fieldIndex = 0; // int? | 0 から始まる列インデックス。
var dynamicFilterType = "BelowAverage"; // string | 動的フィルターの種類。
var matchBlanks = true; // bool? | 空白セルを含める。
var refresh = true; // bool? | 適用後に更新する。
var folder = "myFolder"; // string（オプション）
var storageName = null; // string（オプション）

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("AutoFilterApi.PutWorksheetDynamicFilter の呼び出し時に例外が発生しました: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (オプション)
            undefined              // storageName (オプション)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Ruby、PHP、Go、Perl 用の類似スニペットは、公式 SDK リポジトリで提供されています。)*

## 関連トピック

- **標準のオートフィルターを追加する** – [標準フィルターを追加する](/autofilter/add-filter)  
- **日付フィルターを追加する** – [日付フィルターを追加する](/autofilter/add-date-filter)  
- **オートフィルターを削除する** – [オートフィルターを削除する](/autofilter/delete-filter)  
- **ワークシートの操作** – [ワークシート API 概要](/worksheets/)  

## 注意事項

* 元のドキュメントで使用されているすべての画像は、アクセシビリティに対応するためレビュー済みです。装飾用アイコンは `alt=""` および `role="presentation"` でマークされており、機能アイコンには説明的な `alt` テキストが保持されています。  
* メタキーワードは、空のエントリや重複を削除してクリーンアップされています。  
* 本ページは、SEO およびスクリーンリーダーでのナビゲーション向上のため、明確な見出し階層（ front matter 内に H1 を 1 つ、主要セクションに H2、サブセクションに H3/H4）に従っています。