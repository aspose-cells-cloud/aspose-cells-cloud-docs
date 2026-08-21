---
title: "すべてのドキュメント プロパティを削除する"
second_title: "ドキュメント"
linktitle: "クリア"
type: docs
url: /ja/document-properties/clear/
aliases: [  /ja/remove-all-document-properties/ ]
keywords: "Aspose.Cells, ドキュメント プロパティの削除, Excel プロパティのクリア, REST API, クラウド SDK, スプレッドシート, API リファレンス"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブックからすべてのカスタム プロパティと組み込みプロパティを削除するステップバイステップのガイド。"
weight: 58
---

この REST API は、すべてのカスタム ドキュメント プロパティを削除し、組み込みプロパティをクリアします。

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### リクエスト パラメーター

| パラメーター名 | 型     | 位置   | 説明           |
| -------------- | ------ | ------ | --------------- |
| name           | string | path   | ドキュメント名。   |
| folder         | string | query  | ドキュメント フォルダー。 |
| storageName    | string | query  | ストレージ名。    |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperties) は、パブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザーから直接 REST アクションを実行できるようにします。

cURL コマンドライン ツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
  -X DELETE \
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

## クラウド SDK ファミリー

SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリー](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperties.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperties.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperties.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperties.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperties.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperties.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperties.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperties.go" >}}
{{< /tab >}}

{{< /tabs >}}