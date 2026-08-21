---
title: "Excel ワークブックからテキスト項目を取得する"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブックからテキスト項目を取得する"
second_title: "ドキュメント"
linktitle: "ワークブック内のテキスト項目を取得"
type: docs
url: /ja/workbook/get-text-items/
aliases: [  /ja/get-text-items-from-a-workbook/ ]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, スプレッドシート, テキスト項目の取得, ワークブック"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックからテキスト項目を取得します。C#、Java、Python、PHP、Ruby、Go、Node.js、Perl、Swift 向けの SDK で利用可能です。"
---


## REST API

この REST API は、Excel ファイル内のワークブックの**テキスト項目**を読み取ります。

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。


### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                                       |
| -------------- | ------ | ------ | ------------------------------------------ |
| name           | string | path   | ワークブックファイルの名前。               |
| folder         | string | query  | ワークブックが格納されているストレージ内のフォルダパス。 |
| storageName    | string | query  | ストレージサービスの名前。                 |

### **レスポンス**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP ステータスコード**

| コード | 意味                      | 説明                                                |
|------|---------------------------|-----------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request               | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized              | JWT トークンが無効または不足しています。            |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error     | 予期しないサーバーエラーが発生しました。            |
## SDK を使用した GetWorkbookTextItems API の利用方法

### GetWorkbookTextItems API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

一般的な HTTP ステータスコード：

| コード | 説明                                   |
|------|----------------------------------------|
| 200  | リクエストが成功し、テキスト項目が返されました。 |
| 401  | 認証エラー – トークンが不足または無効です。    |
| 403  | 禁止 – 権限が不足しています。               |
| 404  | 見つかりません – ワークブックまたはリソースが見つかりません。 |
| 500  | Internal Server Error – 予期しない失敗です。 |

### Aspose.Cells Cloud SDK の使用

この例では API バージョン **v3.0** を使用しています。最新バージョンについては変更履歴をご参照ください。SDK を使用することが開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
---