---
title: カラムの詳細情報を取得 – Aspose.Cells Cloud API リファレンス (v4.0)
description: Aspose.Cells Cloud REST API を使用して、ワークシートのカラム（インデックス、幅、スタイル、非表示状態）に関する詳細情報を取得します。
keywords: Aspose.Cells, Cloud API, Excel カラム, カラム取得, REST API, JWT, ワークシート
date: 2026-07-30
---

# カラムの詳細情報を取得  

Aspose Cloud ストレージに保存された Excel ブックから、特定のワークシートのカラム（インデックス、幅、スタイル、非表示状態）に関する詳細情報を取得します。

## 目次
1. [前提条件](#prerequisites)  
2. [認証](#authentication)  
3. [エンドポイント](#endpoint)  
4. [リクエストパラメータ](#request-parameters)  
5. [cURL の例](#curl-example)  
6. [レスポンスの例](#response-example)  
7. [レスポンススキーマ](#response-schema)  
8. [発生し得るエラー](#possible-errors)  
9. [SDK の例](#sdk-examples)  
10. [その他のリソース](#additional-resources)  

---

## 前提条件
- Aspose Cloud 認証を通じて取得した有効な **JWT アクセストークン**。  
- ブックファイルは Aspose Cloud ストレージ（またはその他のサポート対象ストレージ）に保存されており、フォルダパス（ある場合）が事前にわかっていること。  

---

## 認証
すべての Aspose.Cells Cloud API は **JWT トークンベース認証** を使用します。`Authorization` ヘッダーにトークンを含めてください：

```http
Authorization: Bearer <access_token>
```

トークンの取得方法の詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

---

## エンドポイント
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – ブックファイル名（例: `test.xlsx`）。  
- **{sheetName}** – ワークシート名（例: `Sheet1`）。  
- **{columnIndex}** – 取得するカラムの 0 から始まるインデックス。  

---

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

## リクエストパラメータ

| 名前              | 位置   | タイプ    | 必須 | 説明 |
|-------------------|--------|-----------|------|------|
| **name**          | path   | string    | はい | ブックファイル名。 |
| **sheetName**     | path   | string    | はい | 対象のカラムを含むワークシート名。 |
| **columnIndex**   | path   | integer   | はい | 取得するカラムの 0 から始まるインデックス。 |
| **folder**        | query  | string    | いいえ | ブックが存在するストレージフォルダ。 |
| **storageName**   | query  | string    | いいえ | ストレージサービスの名前（例: Aspose Cloud Storage）。 |

---

## cURL の例
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## レスポンスの例
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## レスポンススキーマ
| フィールド             | タイプ    | 説明 |
|------------------------|-----------|------|
| `Column.GroupLevel`   | integer   | カラムのアウトラインレベル（グループ化に使用）。 |
| `Column.Index`        | integer   | カラムの 0 から始まるインデックス。 |
| `Column.IsHidden`     | boolean   | カラムが非表示の場合は `true`、それ以外は `false`。 |
| `Column.Width`        | number    | 文字数で表されたカラムの幅。 |
| `Column.Style`        | object    | カラムのスタイルリソースへの `link` を含む。 |
| `Column.link`         | object    | カラムリソースへの自己リンク。 |
| `Code`                | integer   | レスポンスの HTTP ステータスコード。 |
| `Status`              | string    | ステータスのテキストによる説明（例: **OK**）。 |

---

## 発生し得るエラー
| HTTP ステータス | コード | メッセージ                 | 発生条件 |
|------------------|--------|----------------------------|----------|
| 400              | 400    | Bad Request（不正なリクエスト） | 必須パラメータが不足または不正な形式。 |
| 401              | 401    | Unauthorized（認証エラー）      | `Authorization` ヘッダーが不足または無効。 |
| 404              | 404    | Not Found（存在しない）         | ブック、ワークシート、またはカラムが存在しない。 |
| 500              | 500    | Internal Server Error（内部サーバーエラー） | サーバー側で予期しない問題が発生した場合。 |

### 例 – 404 Not Found（存在しない）
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### 例 – 401 Unauthorized（認証エラー）
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## SDK の例
以下のコードスニペットは、公式 Aspose.Cells Cloud SDK を使用して **Get Worksheet Columns** 操作を呼び出す方法を示しています。Gist が利用できなくなった場合でも、インラインでコード例が提供されます。

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// API クライアントの設定
var apiInstance = new CellsApi("client_id", "client_secret");

// 必須パラメータの設定
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // オプション
string storageName = "MyStorage";    // オプション

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // オプション
        String storageName = "MyStorage";    // オプション

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # オプション
storage_name = "MyStorage"  # オプション

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // オプション
const storageName = "MyStorage"; // オプション

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **注:** すべての SDK は、`client_id` および `client_secret` を提供した後、`Authorization` ヘッダーを自動的に処理します。

---

## その他のリソース
- **OpenAPI スペック:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **認証ガイド:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **GitHub リポジトリ（SDK とサンプル）:** <https://github.com/aspose-cells-cloud>  

--- 

*最終更新日: 2026-07-30*