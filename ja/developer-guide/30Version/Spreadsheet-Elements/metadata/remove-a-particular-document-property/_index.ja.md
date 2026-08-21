---
title: "特定のドキュメント プロパティを削除する"
second_title: "ドキュメント"
linktitle: "削除"
type: docs
url: /document-properties/delete/
aliases: [/remove-a-particular-document-property/]
keywords: "Aspose.Cells, ドキュメント プロパティの削除, Excel メタデータ API, REST, クラウド SDK, cURL の例"
description: "Aspose.Cells Cloud REST API v3.0 を使用して Excel ワークブックから特定のドキュメント プロパティを削除します。C#、Java、Python など、さまざまな SDK の cURL および SDK の使用例を含みます。"
weight: 50
---

この REST API は、ワークブックからドキュメント プロパティを削除します。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### リクエスト パラメーター

| パラメーター名   | 型     | 位置   | 必須 | 説明                                     |
| -------------- | ------ | ------ | ---- | ----------------------------------------- |
| name           | string | path   | はい  | Excel ワークブックの名前です。            |
| propertyName   | string | path   | はい  | 削除するドキュメント プロパティの名前です。 |
| folder         | string | query  | いいえ | ワークブックが保存されているフォルダーのパスです。 |
| storageName    | string | query  | いいえ | ストレージ サービスの名前です。             |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) は、パブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザーから直接 REST のやり取りを実行できるようにします。

cURL コマンドライン ツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
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

### エラー レスポンス

| HTTP ステータス | 説明                                                                 | 例 JSON                                                       |
| --------------- | -------------------------------------------------------------------- | ------------------------------------------------------------- |
| 400             | 不正リクエスト – 必須パラメーターが不足しているか、無効な値です。     | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401             | 認証エラー – 無効または不足している JWT トークンです。               | `{"Code":401,"Message":"Invalid access token."}`              |
| 404             | 見つかりません – ワークブックまたは指定されたプロパティが存在しません。 | `{"Code":404,"Message":"Document property not found."}`       |
| 500             | サーバー内部エラー – サーバーで予期しない状態が発生しました。         | `{"Code":500,"Message":"An unexpected error has occurred."}`  |

## クラウド SDK ファミリー

SDK を使用することが開発を最適化する最良の方法です。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}