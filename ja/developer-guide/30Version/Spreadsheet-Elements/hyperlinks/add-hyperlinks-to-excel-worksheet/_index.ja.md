---
title: "ワークシートにハイパーリンクを追加する"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, ハイパーリンクの追加, Excel REST API, クラウド SDK"
description: "Aspose.Cells Cloud v3.0 REST API を使用して Excel ワークシートにハイパーリンクを追加する方法を学びます。エンドポイント、パラメーターの完全ガイド、cURL の使用例、および C#、Java、Python などの SDK スニペットを含みます。"
weight: 20
---

この REST API は、Excel ワークシートにハイパーリンクを追加します。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### リクエストパラメーター

| パラメーター名   | 型      | 位置   | 説明                                                                                   |
| -------------- | ------- | ------ | ------------------------------------------------------------------------------------- |
| name           | 文字列  | パス   | ドキュメント名。                                                                        |
| sheetName      | 文字列  | パス   | ワークシート名。                                                                        |
| firstRow       | 整数    | クエリ | ハイパーリンクを適用する範囲の最初の行（0 から始まるインデックス）。                     |
| firstColumn    | 整数    | クエリ | ハイパーリンクを適用する範囲の最初の列（0 から始まるインデックス）。                     |
| totalRows      | 整数    | クエリ | ハイパーリンク範囲が含まれる行数。                                                      |
| totalColumns   | 整数    | クエリ | ハイパーリンク範囲が含まれる列数。                                                      |
| address        | 文字列  | クエリ | ハイパーリンクが指す宛先 URL（URL エンコード済み）。                                    |
| folder         | 文字列  | クエリ | ドキュメントが格納されたフォルダー。                                                   |
| storageName    | 文字列  | クエリ | ストレージ名。                                                                          |

リクエストには、同じフィールド（`Address`、`FirstRow`、`FirstColumn`、`TotalRows`、`TotalColumns`）を含む JSON ボディを含めることもできます。ボディを指定することで、クエリ文字列パラメーターではなくペイロードとしてデータを渡すことが可能です。

### エラーレスポンス

| HTTP コード | 理由                                     | 例ボディ                                                            |
| ----------- | ---------------------------------------- | ------------------------------------------------------------------- |
| **400**     | 不正リクエスト – 必須パラメーターが不足または無効です。 | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 認証エラー – JWT トークンが不足または無効です。        | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 見つかりません – ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | サーバー内部エラー – 予期しないサーバーエラーが発生しました。 | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用することで、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

リクエストが失敗した場合、API は標準の HTTP エラーコード（例：400 Bad Request、401 Unauthorized、404 Not Found、500 Internal Server Error）と、エラーメッセージとコードを含む JSON ペイロードを返します。

## クラウド SDK ファミリー

SDK を使用すると、開発が最も迅速に進みます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}