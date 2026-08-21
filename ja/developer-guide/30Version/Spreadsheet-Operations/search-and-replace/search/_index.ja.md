---
title: "Excel ファイル内のテキストを検索する – Aspose.Cells Cloud API"
description: "Aspose.Cells Cloud API を使用して、Excel (XLS、XLSX、XLSM、XLSB) ファイルおよび ODS ファイル内の特定のテキストを検索します。リクエストの詳細、cURL および SDK の例、エラー処理を含みます。"
keywords: "Aspose.Cells, Excel, 検索, API, REST"
type: docs
url: /cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Excel ファイル内のテキストを検索する – Aspose.Cells Cloud API

## 概要
Aspose.Cells Cloud は、Excel ワークブック (XLS、XLSX、XLSM、XLSB) および OpenDocument Spreadsheet (ODS) ファイル内の指定されたテキスト文字列を検索するための **POST** エンドポイントを提供します。API は、リクエストされたテキストを含むすべてのセルを返し、一致したワークシートへのリンクも提供します。

> **使用例**  
> - 特定の値がレポート内に存在することを、さらに処理を進める前に確認する。  
> - すべての出現箇所をまず一覧表示する「検索・置換」ツールを構築する。  
> - スプレッドシートのバッチ全体からキーワードのインデックスを生成する。

---

## 前提条件
| 要件 | 詳細 |
|------|------|
| **認証** | Aspose Cloud OAuth フローによって取得した JWT トークン。トークンには **Cells** スコープが含まれている必要があります。 |
| **対応フォーマット** | XLS、XLSX、XLSM、XLSB、ODS |
| **最大ファイルサイズ** | 150 MB（圧縮後）。それより大きいファイルは **413 Payload Too Large** を返します。 |
| **必要なヘッダー** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **権限** | トークンは、リモートストレージを使用する場合、対象ストレージに対する *読み取り* 権限が必要です。ファイルを `multipart/form-data` としてアップロードする場合は不要です。 |

*ヒント:* JWT トークンの生成には **/connect/token** エンドポイントを使用します。詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

---

## エンドポイント

| 項目 | 値 |
|------|----|
| **HTTP メソッド** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **目的** | アップロードされた Excel ワークブック内に指定されたテキストを検索します。 |
| **セキュリティ** | JWT トークン（Bearer）– 上記「前提条件」を参照。 |

---

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

## リクエストパラメータ

| 名前 | 型 | 位置 | 必須 | 説明 |
|------|----|------|------|------|
| `file` | **file** | `formData`（multipart） | **はい** | アップロードするスプレッドシートファイル。 |
| `text` | **string** | クエリ文字列 | **はい** | 検索するテキスト文字列。 |
| `password` | **string** | クエリ文字列 | いいえ | 保護されたワークブックを開くためのパスワード（必要な場合）。 |
| `sheetname` | **string** | クエリ文字列 | いいえ | 検索対象を限定するワークシート名。省略された場合、すべてのワークシートが検索されます。 |
| `checkExcelRestriction` | **boolean** | クエリ文字列 | いいえ（デフォルト: `true`） | `true` の場合、API は検索前に Excel 固有の制約（例：読み取り専用セル）を検証します。 |

---

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*`<jwt-token>` を有効なトークンに置き換え、必要に応じてクエリパラメータを調整してください。*

---

## 成功時の応答

**HTTP 200 – 検索成功；応答には見つかったテキスト項目が含まれます。**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### 応答フィールド

| フィールド | 型 | 説明 |
|-----------|----|------|
| `Status` | string | 全体のリクエスト状態（成功時は `OK`）。 |
| `Code` | integer | HTTP ステータスコード（200）。 |
| `TextItems.link` | object | コレクションリソースへのハイパーメディアリンク。 |
| `TextItems.TextItemList` | array | 一致項目のリスト。各項目には以下が含まれます。 |
| `Text` | string | 検索テキストに一致したセルの値。 |
| `link` | object | 一致したワークシートへのハイパーリンク（`Href` は `Workbook/worksheets/SheetName` を指します）。 |

---

## エラー応答

| HTTP コード | 意味 | 典型的な原因 | 例（ボディ） |
|-------------|------|--------------|--------------|
| **400** | Bad Request（不正なリクエスト） | 必須パラメータの欠落、サポートされていないファイル形式、無効なクエリ値など。 | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401** | Unauthorized（未認証） | JWT トークンの欠落または無効。 | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }` |
| **413** | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルが 150 MB の制限を超えています。 | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }` |
| **500** | Internal Server Error（内部サーバーエラー） | 予期しないサーバー側の問題。 | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }` |

---

## SDK の例

以下は、公式 Aspose.Cells Cloud SDK を使用した **PostSearch** 操作の最小限のコードスニペットです。`YOUR_JWT_TOKEN` およびファイルパスを各自の値に置き換えてください。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(PHP、Ruby、Go、Perl の SDK は [Aspose.Cells Cloud GitHub リポジトリ](https://github.com/aspose-cells-cloud) で利用可能です。)*

---

## 補足事項

- **`checkExcelRestriction`** のデフォルト値は `true` です。ワークブックに検索を妨げる保護されたセルが含まれていないことが確実な場合のみ、`false` に設定してください。
- API はハイパーメディアリンク（`Href`）を返します。このリンクは、Aspose.Cells Cloud の他のエンドポイント（例：ワークシートのダウンロードやセル書式の取得）で使用できます。
- 大きなワークブックを検索する際は、`sheetname` パラメータで検索範囲を絞ることで応答時間を短縮できます。

---

## 関連リンク

- **認証ガイド** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **PostSearch の OpenAPI 仕様** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>
- **レート制限とクォータ** – <https://docs.aspose.cloud/total/getting-started/limits/>