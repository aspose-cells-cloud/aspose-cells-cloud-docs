---
title: "Aspose.Cells Cloud ファイルダウンロード API – クラウド上で高速にファイルをダウンロードするためのインターフェース"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud ファイルダウンロード API – クラウド上で高速にファイルをダウンロードするためのインターフェース"
linktitle: "ファイルダウンロード API"
type: docs
url: /download-file/
keywords: "Aspose.Cells, ファイルダウンロード API, Excel クラウドストレージ, REST API, ファイルダウンロード, PDF, CSV, SDK"
description: "Aspose.Cells Cloud ストレージから Excel、PDF、CSV およびその他のファイルを Download File API（v4.0）でダウンロードします。エンドポイント、パラメーター、認証詳細、コードサンプルを含みます。"
weight: 100
---

**DownloadFile** API を使用すると、Aspose.Cells Cloud ストレージに保存されたファイルを取得できます。ファイルダウンロード API は、Excel スプレッドシート、PDF、CSV およびその他の対応フォーマットをクラウドから直接アクセスするのに不可欠です。

## **Excel API：ファイルのダウンロード**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **DownloadFile** API のリクエストパラメーター

| パラメーター名 | 型     | 位置（パス / クエリ） | 説明                                                    |
| -------------- | ------ | --------------------- | ---------------------------------------------------------- |
| path           | 文字列 | パス                  | ダウンロードしたいファイルの仮想パス                      |
| storageName    | 文字列 | クエリ                | ファイルを取得するストレージの名前                         |
| versionId      | 文字列 | クエリ                | ダウンロードするファイルのバージョン識別子（該当する場合） |

### **レスポンス**

API は**バイナリファイルストリーム**を返します。`Content-Type` ヘッダーはファイル形式に応じて設定されます（例：XLSX の場合は `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`）。JSON ペイロードは返されません。

**HTTP ステータスコード**

| コード | 意味                  | 説明                                                      |
| ------ | --------------------- | --------------------------------------------------------- |
| 200    | OK                    | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request（リクエストエラー） | パラメーターが不足または不正（例：サポートされていないファイル形式） |
| 401    | Unauthorized（認証エラー） | JWT トークンが不正または不足しています。                     |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。         |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。                      |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST API を操作できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を大幅に高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}