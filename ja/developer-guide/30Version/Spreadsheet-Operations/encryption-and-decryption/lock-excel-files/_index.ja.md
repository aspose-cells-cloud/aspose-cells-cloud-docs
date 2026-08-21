---
title: "Excel ファイルをロックする"
second_title: "ドキュメント"
linktitle: "Excel ファイルをロック"
type: docs
url: /lock-excel-files/
aliases: [/lock/without-storage/, /lock/, /lock/without-using-storage/]
keywords: "ロック, Excel, API, Aspose.Cells, クラウド, REST, ワークブック, スプレッドシート, SDK"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークブックをロックする方法を学びます。HTTPS エンドポイント、認証、cURL リクエスト、レスポンススキーマ、および C#、Java、Python などの SDK コードサンプルを含みます。"
ArticleTitle: "Excel ファイルをロックする – Aspose.Cells Cloud API ドキュメント"
weight: 70
---

**API バージョン:** v3.0 (最新版)

この REST API は Excel ワークブックを**ロック**します。

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**前提条件** – リクエストは **HTTPS** 経由で送信され、`Authorization` ヘッダーに有効な OAuth 2.0 Bearer トークンを含める必要があります。

### リクエストパラメーター

| パラメーター名 | 型     | 位置                         | 説明                                   |
| -------------- | ------ | ---------------------------- | --------------------------------------------- |
| file           | ファイル | form‑data (multipart body) | アップロードおよびロックする Excel ワークブック |
| password       | 文字列  | クエリ文字列                 | ワークブックのパスワード (オプション)         |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を**呼び出す**方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*リクエストをテストするためのサンプルワークブック — [Sample.xlsx](https://example.com/Sample.xlsx) — をダウンロードできます。*

**注意:** この API は最大 100 MB のファイルをサポートします。それより大きなペイロードを送信すると、413 (ペイロードが大きすぎます) のレスポンスが返される可能性があります。

### **レスポンスの詳細**

| フィールド       | 型              | 説明                                          |
| --------------- | --------------- | --------------------------------------------- |
| Filename        | 文字列           | サービスから返されるロックされたワークブックのファイル名 |
| FileSize        | 整数            | ロックされたファイルのサイズ (バイト単位)     |
| FileContent     | 文字列 (Base64) | Base64 文字列としてエンコードされたロックされたワークブック |

ロックされたワークブックを取得するには、レスポンス内の `FileContent` の値を Base64 からデコードし、`Filename` で指定された名前で保存します。

### **エラーハンドリング**

– API は標準的な HTTP ステータスコード (例: `400 Bad Request`、`401 Unauthorized`、`500 Internal Server Error`) を返し、それに加えて `Code` と `Message` フィールドを含む JSON 形式のエラーオブジェクトも返します。

## クラウド SDK ファミリー

SDK を使用することが開発を高速化する最良の方法です。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}