---
title: "Excelワークシートから行の情報を取得する"
second_title: "Document"
linktitle: "Row"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel 行 API, ワークシートの行を取得, REST API, .NET SDK, Java SDK, Python SDK"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内の特定の行（高さ、スタイル、非表示状態など）の詳細情報を取得します。cURLの例、SDKのコードスニペット、エラーハンドリングを含みます。"
weight: 10
ArticleTitle: "Excelワークシートから行の情報を取得する – Aspose.Cells Cloud API"
---

**前提条件:**  
- 有効なJWTアクセストークンを取得し、`Authorization: Bearer <jwt token>` ヘッダーに含めてください。  
- ワークブックがAspose Cloudストレージに保存されていることを確認するか、ワークブックが存在するフォルダのパスを指定してください。  
- エンドポイントURLに示されているように、APIバージョン **v3.0** を使用してください。

このREST APIは、Excelワークシート上の行インデックスを使って行データを取得します。

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名    | 型      | 位置   | 説明                                           |
| --------------- | ------- | ------ | --------------------------------------------- |
| name            | string  | path   | ワークブックファイルの名前。                   |
| sheetName       | string  | path   | ワークブック内のワークシートの名前。           |
| rowIndex        | integer | path   | 取得する行の0始まりのインデックス。            |
| folder          | string  | query  | ワークブックが存在するフォルダ。               |
| storageName     | string  | query  | ワークブックが存在するストレージの名前。       |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow)は、パブリックに利用可能なプログラミングインターフェースを定義し、Webブラウザから直接REST APIとのやりとりを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLを使用してクラウドAPIにリクエストを送信する方法を示しています。リクエストを認証するには、`Authorization: Bearer <jwt token>` ヘッダーを含めてください。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**レスポンススキーマ**

| プロパティ名       | 型      | 説明                                                         |
|-------------------|---------|------------------------------------------------------------|
| `GroupLevel`      | integer | 行のアウトラインレベル（グループ化に使用）。               |
| `Height`          | number  | 行の高さ（ポイント単位）。                                   |
| `Index`           | integer | 返された行の0始まりのインデックス。                          |
| `IsBlank`         | boolean | 行にデータが含まれているかどうかを示します。                 |
| `IsHeightMatched`| boolean | 行の高さが既定の行の高さと一致する場合に `true`。           |
| `IsHidden`        | boolean | 行が非表示の場合に `true`。                                  |
| `Style`           | object  | 行のスタイル情報を含むオブジェクト。                         |
| `link`            | object  | 行リソースへのハイパーリンク参照。                           |
| `Code`            | integer | レスポンスのHTTPステータスコード。                           |
| `Status`          | string  | ステータスのテキストによる説明（例: “OK”）。                |

{{< /tab >}}

{{< /tabs >}}

**注意事項 / エラーハンドリング:** APIは以下のHTTPステータスコードを返す可能性があります：

- **200** – 成功；行データが返されます。  
- **401** – 認証エラー；JWTトークンが欠落しているか、無効です。  
- **404** – 見つからない；指定されたワークブック、ワークシート、または行が存在しません。  
- **500** – サーバー内部エラー；予期しない状態が発生しました。

| コード | 説明                                         | 対処方法                               |
|--------|---------------------------------------------|---------------------------------------|
| 200    | 成功 – 行データが返されました。             | –                                     |
| 401    | 認証エラー – JWTトークンが欠落しているか、無効です。 | 有効なJWTトークンを提供してください。  |
| 404    | 見つからない – ワークブック、ワークシート、または行が存在しません。 | 名前と行インデックスを確認してください。 |
| 500    | サーバー内部エラー – 予期しない状態が発生しました。 | Asposeサポートにお問い合わせください。  |

エラーコードの完全なリストについては、Aspose.Cells Cloudの[エラーコードドキュメント](https://docs.aspose.cloud/cells/)をご参照ください。

## Cloud SDKファミリー

SDKを使用するのが開発を進める最も高速な方法です。SDKは低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}