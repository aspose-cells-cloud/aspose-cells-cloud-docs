---
title: "Excel ファイルからメタデータを取得する"
second_title: "ドキュメント"
linktitle: "ストレージを使わずに取得する"
type: docs
url: /ja/metadata/get/
keywords: "Aspose.Cells, Excel, メタデータ, REST API, クラウド SDK"
description: "Aspose.Cells Cloud REST API を使って Excel ワークブックから組み込みまたはカスタムメタデータを取得します。リクエスト形式、パラメータ、サンプル SDK コード、エラー処理を含みます。"
weight: 23
ArticleTitle: "Excel ファイルからメタデータを取得する - Aspose.Cells Cloud API"
---

この REST API は、1 つ以上の Excel ファイルから**メタデータ**を取得します。  
リクエストには、OAuth 2.0 クライアント資格情報フローにより取得した `Authorization: Bearer <access_token>` ヘッダーを含める必要があります。

**前提条件**: このエンドポイントを呼び出すには、Aspose Cloud OAuth 2.0 トークンエンドポイントから取得した有効なアクセストークンが必要です。トークンを取得するための curl リクエストの例:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### クエリパラメータ

| パラメータ名 | 型     | 説明                                                                 |
| ------------ | ------ | -------------------------------------------------------------------- |
| type         | string | `ALL` / `BuiltIn` / `Custom` – 返すメタデータグループを指定します。 |

### リクエストボディパラメータ

| パラメータ名 | 型       | 説明                                                       |
| ------------ | -------- | ---------------------------------------------------------- |
| excel file   | データファイル | Excel ファイルをマルチパートリクエストの第 1 部として渡します。 |

### レスポンス

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| コード | 意味             | 発生条件                             |
|------|------------------|--------------------------------------|
| 200  | 成功             | メタデータが返されました。           |
| 400  | 不正なリクエスト | ファイルが欠落しているか、クエリが無効です。 |
| 401  | 認証エラー       | トークンが無効または不足しています。     |
| 404  | 見つかりません   | 指定されたファイルが見つかりません。     |
| 500  | サーバーエラー   | 想定外のサーバー障害が発生しました。     |

この API は、該当する場合はこれらの標準 HTTP ステータスコードに加えて、エラー応答 JSON オブジェクトを返します。

### クラウド SDK ファミリー

SDK を使用すると、低レベルの詳細を処理することで開発が加速します。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
---