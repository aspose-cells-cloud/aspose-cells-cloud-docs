---
title: "垂直ページ区切りの取得"
second_title: "Document"
linktitle: "垂直ページ区切りの取得"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells, 垂直ページ区切り, Excel API, クラウドスプレッドシート, REST API"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して Excelワークシートから垂直ページ区切りを取得します。HTTPSエンドポイント、必須パラメータ、cURLの使用例、レスポンスの詳細、エラーハンドリング、SDKサンプルを含みます。"
weight: 20
---

この REST API は、ワークシートから**垂直**ページ区切りを取得します。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                                          | 必須 |
| ---------------- | ------ | ------ | --------------------------------------------- | ---- |
| `name`           | string | path   | Excel ファイルの名前。                        | はい   |
| `sheetName`      | string | path   | 区切りを読み取るワークシートの名前。          | はい   |
| `folder`         | string | query  | ファイルを含むストレージ内のフォルダ。        | いいえ |
| `storageName`    | string | query  | 使用する Aspose Cloud ストレージの名前。      | いいえ |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST によるやり取りを可能にします。

**cURL** を使って Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### レスポンスの詳細

| フィールド                | 型     | 説明                                                                 |
| ------------------------- | ------ | -------------------------------------------------------------------- |
| `VerticalPageBreakList`   | array  | 垂直ページ区切りオブジェクトのコレクション。                         |
| `Column`                  | int    | 区切りが発生する列インデックス（0始まり）。                          |
| `StartRow`                | int    | 区切り範囲の最初の行（0始まり）。                                    |
| `EndRow`                  | int    | 区切り範囲の最後の行（0始まり、通常は最終行で `1048575`）。         |
| `link.Href`               | string | リソースへの自己参照 URL（HTTPS）。                                 |
| `Code`                    | int    | サービスが返す HTTP ステータスコード。                               |
| `Status`                  | string | HTTP ステータスのテキストによる説明。                                |

### エラーハンドリング

| HTTP コード | 意味                | 一般的な原因                           |
| ----------- | ------------------- | -------------------------------------- |
| 401         | 認証エラー（Unauthorized）  | JWT トークンが不足しているか、無効です。     |
| 404         | 見つかりません（Not Found） | 指定されたファイルまたはワークシートが存在しません。 |
| 400         | 不正なリクエスト（Bad Request） | 無効または不正なクエリパラメータです。       |
| 500         | サーバ内部エラー（Internal Server Error） | サーバ側で予期しない状況が発生しました。 |

JSON レスポンス内の `Code` および `Status` フィールドを確認して、詳細情報を取得してください。

## クラウド SDK ファミリー

SDK を使用すると、Aspose.Cells Cloud に対する開発を最速で行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}