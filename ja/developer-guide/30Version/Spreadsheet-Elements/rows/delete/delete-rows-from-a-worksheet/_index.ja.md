---
title: "Excelワークシートから複数の行を削除する"
second_title: "ドキュメント"
linktitle: "行"
type: docs
url: /ja/rows/delete/rows/
keywords: "Aspose.Cells Cloud、行の削除、複数行の削除、Excelワークシート、REST API、SDK"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートから1つまたは複数の行を削除する方法を学びます。エンドポイントの詳細、パラメータ、cURLの使用例、および複数の言語向けのSDKコードサンプルを含みます。"
weight: 80
ArticleTitle: "Aspose.Cells Cloud API を使用して Excelワークシートから複数の行を削除する"
---

この REST API は、Excelワークシート**から**複数の行を削除します。

**前提条件:** このエンドポイントを呼び出すには、Aspose Cloud の認証から取得した有効なJWTアクセストークンと、ワークブックに対する適切なストレージ権限が必要です。

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を要求します。

### **リクエストパラメータ**

| パラメータ名  | 型      | パス / クエリ文字列 / HTTP本文 | 説明                                                      |
| ------------- | ------- | ----------------------------- | --------------------------------------------------------- |
| name          | 文字列  | パス                          | ワークブック名。                                          |
| sheetName     | 文字列  | パス                          | ワークシート名。                                          |
| startrow      | 整数    | クエリ                        | 削除する最初の行の0から始まるインデックス（例：`0`＝最初の行）。 |
| totalRows     | 整数    | クエリ                        | 削除する行数。                                            |
| updateReference | 真偽値 | クエリ                        | 削除後に参照を更新するかどうか（`true`／`false`）。         |
| folder        | 文字列  | クエリ                        | ドキュメントが格納されたフォルダ。                        |
| storageName   | 文字列  | クエリ                        | ストレージ名。                                            |

[OpenAPI仕様書](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows)は、公開されているプログラミングインターフェースを定義し、Webブラウザから直接REST APIと対話できるようにします。

cURLコマンドラインツールを使用して、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLでクラウドAPIを呼び出す方法を示しています。**すべてのエンドポイントはHTTPSを要求し、HTTPは非推奨です。**

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**返される可能性のあるHTTPステータスコード**

| HTTPステータス | 説明                                      |
|----------------|-------------------------------------------|
| 200            | 行が正常に削除されました。                |
| 400            | 不正なリクエスト－無効なパラメータ。      |
| 401            | 認証エラー－JWTトークンが不足または無効。  |
| 404            | 見つかりません－ワークブックまたはワークシートが存在しません。 |
| 500            | サーバーエラー－予期しない状態が発生しました。 |

## Cloud SDKファミリー

SDKを使用することで、開発スピードを最大限に高めることができます。SDKは低レベルの詳細な処理を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}