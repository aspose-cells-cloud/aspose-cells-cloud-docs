---
title: Excel での列のグループ解除 – Aspose.Cells Cloud API  
description: Aspose.Cells Cloud REST API（v3.0）を使用して Excel ワークシート内の列のグループを解除します。エンドポイント、パラメータ、認証方法、cURL の使用例、レスポンス形式、および SDK スニペットを含みます。  
keywords: Aspose.Cells, 列のグループ解除, 列, Excel, API, REST, クラウド, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Excel での列のグループ解除  

Aspose.Cells Cloud は、指定されたワークシートから列のグループを解除するための **POST** 操作を提供します。このページでは、リクエスト形式、必要なパラメータ、認証方法、使用例、および SDK の利用方法を詳しく説明します。

---  

## 前提条件  

| 必要条件 | 必要な理由 |
|---------|-----------|
| **Aspose Cloud アカウント** | Aspose.Cells Cloud サービスへのアクセス権を取得します。 |
| **JWT アクセストークン** | すべての API 呼び出しは、ベアラートークンで認証される必要があります。詳細は [JWT 認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。 |
| **Aspose Cloud ストレージに保存されたワークブック** | API はクラウドストレージ（または接続された外部ストレージ）内に存在するファイルを対象とします。 |
| **ワークシート名** | 対象となるワークシートは、ワークブック内に存在している必要があります。 |

---  

## 認証  

すべてのリクエストでは、有効な JWT トークンを含む **Authorization** ヘッダーが必要です：

```http
Authorization: Bearer <access_token>
```

トークンは Aspose Cloud の OAuth フローにより取得します。トークンには有効期限があり、必要に応じて更新してください。

---  

## エンドポイント  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **パス** – ワークブックのファイル名（例：`test.xlsx`）。  
* `{sheetName}` – **パス** – ワークシート名（例：`Sheet1`）。  

---  

## パラメータ  

### パスパラメータ  

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| `name` | 文字列 | はい | ワークブックのファイル名。 |
| `sheetName` | 文字列 | はい | ワークシート名。 |

### クエリパラメータ  

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| `firstIndex` | 整数 | はい | グループ解除する最初の列の 0 から始まるインデックス。 |
| `lastIndex` | 整数 | はい | グループ解除する最後の列の 0 から始まるインデックス。 |
| `folder` | 文字列 | いいえ | ワークブックが配置されているフォルダのパス。 |
| `storageName` | 文字列 | いいえ | ファイルが存在するストレージサービスの名前。 |

---  

## リクエスト例（cURL）  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

* `<access_token>` を有効な JWT トークンに置き換えてください。*

---  

## 成功時のレスポンス  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

レスポンスオブジェクト（`CellsCloudResponse`）には、正常にグループ解除された列の範囲が含まれます。

### エラーレスポンス  

リクエストが失敗した場合、サービスは以下のフィールドを含む JSON ペイロードを返します：

| フィールド | 意味 |
|-----------|------|
| `Code` | HTTP スタイルのエラーコード（例：400、401）。 |
| `Status` | エラーの簡単な説明。 |
| `ErrorMessage` | エラーの詳細な説明。 |

---  

**HTTP ステータスコード**

| コード | 意味 | 説明 |
|-------|------|------|
| 200  | OK | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400  | 不正リクエスト | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | 認証エラー | JWT トークンが無効または不足しています。 |
| 413  | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | サーバーエラー | 予期しないサーバーエラーが発生しました。 |
---  

## SDK のコードサンプル  

以下は、最も人気のある SDK 用の実行可能なスニペットです。プレースホルダー（`<YourAccessToken>`、`<YourFileName>` など）を実際の値に置き換えて使用してください。

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **注:** PHP、Ruby、Perl など他の言語用の SDK も、同様のパラメータ順序を採用しています。完全なサンプルは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

---  

## 参照  

* **OpenAPI スペック:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **認証ガイド:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK リポジトリ:** <https://github.com/aspose-cells-cloud>

---  

## 履歴  

| 日付 | 著者 | 変更内容 |
|------|------|----------|
| 2026‑07‑30 | AI Optimizer | UTF‑8 エンコーディングの修正、前提条件の追加、メタキーワードの整理、見出し階層の改善、SDK スニペットの挿入。 |
| 2026‑07‑29 | Original | 初版ドキュメントの草案。 |

---