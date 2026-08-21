---
title: "Aspose.Cells Cloud API – ワークシートからリストオブジェクト（テーブル）を取得"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートからリストオブジェクト（テーブル）を取得します。複数の形式（PDF、CSV、JSON など）へのエクスポートをサポートします。"
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Table
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – ワークシートからリストオブジェクト（テーブル）を取得

Excel ブック内の特定のワークシートから**リストオブジェクト**（*テーブル*とも呼ばれます）を取得します。このエンドポイントは、オプションの `format` クエリパラメータを使用して、テーブルを直接選択した形式でエクスポートすることもできます。

---

## 前提条件

| 要件 | 詳細 |
|------|------|
| **認証** | 有効な **JWT**（Bearer）トークンが必要です。トークンは [認証ガイド](/authentication/) に記載された **OAuth2** 認証フローで取得してください。 |
| **ストレージ** | ブックは Aspose Cloud ストレージ内に保存されている必要があります。ファイルがデフォルト以外のストレージにある場合は、`storageName` クエリパラメータを指定してください。 |
| **レート制限** | API は標準の Aspose Cloud レート制限ポリシー（デフォルト＝100リクエスト/分／アカウント）に従います。 |
| **SDK（任意）** | 公式 SDK（C#、Java、Python など）を使用すると、リクエストの構築とレスポンスの処理が容易になります。以下にある **SDK サンプル** を参照してください。 |

---

## リクエスト

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| パラメータ | 型 | 位置 | 必須 | 説明 |
|-----------|----|------|------|------|
| **name** | `string` | パス | ✔️ | Excel ファイル名（拡張子を含む）。 |
| **sheetName** | `string` | パス | ✔️ | リストオブジェクトを含むワークシート名。 |
| **listobjectindex** | `integer` | パス | ✔️ | 取得するリストオブジェクトの 0 から始まるインデックス。 |
| **format** | `string` | クエリ | ❌ | エクスポート先の形式（例：`pdf`、`csv`、`json`）。 |
| **folder** | `string` | クエリ | ❌ | ブックが保存されているフォルダのパス。 |
| **storageName** | `string` | クエリ | ❌ | 使用する Aspose Cloud ストレージ名。 |

#### 注釈

* すべての呼び出しは **必ず HTTPS 経由** で行う必要があります。  
* `format` パラメータを指定した場合、レスポンス本体はエクスポートされたファイルストリーム（例：`application/pdf`）になります。  
* `format` を指定しない場合、API はリストオブジェクトの JSON 記述を返します。

---

## cURL の例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*`<your_jwt_token>` は、認証エンドポイントで取得した有効な JWT に置き換えてください。*

---

## 成功時のレスポンス（JSON）

**`format` を省略した場合**、API はリストオブジェクトの内容を記述する JSON ペイロードを返します。

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**`format` を指定した場合**、レスポンス本体は要求されたファイル形式のバイナリストリーム（例：`Content-Type: text/csv`）になります。

---

## エラーハンドリング

| HTTP コード | 意味 | 例（JSON） |
|-------------|------|------------|
| **400** | 不正なリクエスト – パラメータが不足または無効です。 | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | 認証エラー – JWT トークンが不足または無効です。 | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | 見つかりません – ブック、ワークシート、またはリストオブジェクトが存在しません。 | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | サーバー内部エラー。 | `{"Code":500,"Message":"Unexpected server error."}` |

### 共通の落とし穴（注意事項）

* **0 から始まるインデックス** – `listobjectindex` は **0** から始まります。インデックス `1` を指定すると、シート内の 2 番目のテーブルが返されます。  
* **フォルダとストレージ** – ブックがサブフォルダ内に保存されている場合は、`folder` クエリパラメータを含めてください（例：`?folder=Reports/2024`）。  
* **エクスポート形式** – Aspose.Cells 変換エンジンがサポートする形式のみ使用可能です（`pdf`、`xlsx`、`csv`、`json` など）。サポートされていない形式を指定すると **400** エラーが発生します。

---

## SDK サンプル

以下のスニペットは、公式 Aspose.Cells Cloud SDK を使用してエンドポイントを呼び出す方法を示しています。プレースホルダー値（`<YOUR_CLIENT>`、`<YOUR_JWT>` など）を実際の設定に置き換えてください。

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API クライアントを初期化
var apiInstance = new ListObjectsApi();

// リクエストを構築
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // 例："csv" でエクスポート
    folder: null,
    storageName: null
);

// 実行
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## 関連項目

| 関連エンドポイント | 説明 |
|------------------|------|
| **リストオブジェクトの追加** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – 新しいテーブルを作成します。 |
| **リストオブジェクトの更新** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – テーブルのプロパティを変更します。 |
| **リストオブジェクトの削除** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – テーブルを削除します。 |
| **すべてのリストオブジェクトを一覧表示** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – ワークシート内のテーブルを列挙します。 |

---

## 参照

* **OpenAPI スペシフィケーション** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **認証ガイド** – <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub リポジトリ（SDK）** – <https://github.com/aspose-cells-cloud>  

---
---