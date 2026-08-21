---
title: "ワークシート内の範囲を貼り付けオプション付きでコピー"
second_title: "Document"
linktitle: "Copy"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, REST API, Excel, 範囲のコピー, ワークシート, 貼り付けオプション"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークシート内の範囲を完全な貼り付けオプション対応でコピーします。複数のプログラミング言語向けの SDK サンプルを含みます。"
weight: 20
ArticleTitle: "ワークシート内の範囲を貼り付けオプション付きでコピー – Aspose.Cells Cloud API"
---

この REST API は、Excel ワークブックのワークシート内にある範囲をコピーします。関連する操作については、「**範囲の取得**」および「**範囲の更新**」のドキュメントをご覧ください。

**前提条件:** このエンドポイントを使用するには、有効な OAuth 2.0 / JWT トークンが必要であり、API のバージョンがリクエスト URL と一致していることを確認してください。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **リクエストパラメータ**

| パラメータ名   | タイプ   | 位置   | 説明                                                                 |
| -------------- | ------ | ------ | -------------------------------------------------------------------- |
| name           | string | path   | ワークブックの名前。                                               |
| sheetName      | string | path   | ワークシートの名前。                                               |
| rangeOperate   | string | body   | 実行する操作: `copydata`（データのみ）、`copystyle`（スタイルのみ）、`copyto`（データとスタイル）、`copyvalue`（数式を除く値のみ） |
| folder         | string | query  | ワークブックを含むフォルダ。                                       |
| storageName    | string | query  | ストレージサービスの名前。                                         |

**注意事項:** `rangeOperate` フィールドはコピー対象を決定します。`copydata` はセルの値のみをコピー、`copystyle` は書式設定のみをコピー、`copyto` はデータとスタイルの両方をコピー、`copyvalue` は数式を除いた値のみをコピーします。API は最大 100 万セルの範囲をサポートします。それ以上の範囲はタイムアウトが発生する可能性があります。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) はパブリックにアクセス可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

正常なレスポンスは `200 OK` ステータスを返します。エラー発生時は、以下のようなペイロードが返されることがあります：

```json
{
  "Code": 400,
  "Message": "Bad Request – 無効なパラメータです。"
}
```

または

```json
{
  "Code": 401,
  "Message": "Unauthorized – 認証トークンが不足または無効です。"
}
```

これらのエラーオブジェクトには、問題の診断に役立つ HTTP ステータスコードと説明的なメッセージが含まれています。

{{< /tab >}}

{{< /tabs >}}

コピー操作をテストするためのサンプルワークブックを[こちら](https://example.com/sample.xlsx)からダウンロードできます。

## Cloud SDK Family

SDK を使用すると、開発を最適化できます。SDK が低レベルの詳細を処理するため、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}
---