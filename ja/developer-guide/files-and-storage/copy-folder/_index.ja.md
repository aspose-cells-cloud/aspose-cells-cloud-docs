---
title: "Aspose.Cells Cloud フォルダコピー API – クラウド内でのフォルダを高速にコピー"
second_title: "ドキュメント"
ArticleTitle: "クラウドベースの Excel ファイル管理ソリューション – Aspose.Cells フォルダコピー API のバッチコピー機能の詳細解説"
linktype: "docs"
url: /ja/copy-folder/
keywords: "フォルダコピー、Aspose.Cells Cloud、REST API、クラウドストレージ、スプレッドシート管理"
description: "Aspose.Cells Cloud ストレージ内のフォルダを単一の REST 呼び出しでコピーする方法を学びます。エンドポイント、パラメータ、サンプルリクエスト、エラーコード、SDK サンプルを含みます。"
weight: 100
---

**CopyFolder** API は、Aspose.Cells Cloud ストレージ内に既存のフォルダを複製します。これは、手動でのファイル移動なしに、バックアップの作成、データの再編成、さらなる処理のためのフォルダ階層の準備を行うのに便利です。

## **Excel API：フォルダのコピー**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### CopyFolder API は以下のパラメータを受け取ります

| パラメータ名        | 必須   | 型     | 位置（パス／クエリ） | 説明                                                           |
| ------------------- | ------ | ------ | -------------------- | -------------------------------------------------------------- |
| `srcPath`           | はい   | 文字列 | パス                 | コピー元のフォルダのパスです。                                 |
| `destPath`          | はい   | 文字列 | クエリ               | 新しいフォルダを作成するパスです。                             |
| `srcStorageName`    | いいえ | 文字列 | クエリ               | コピー元フォルダを含むストレージの名前です。                   |
| `destStorageName`   | いいえ | 文字列 | クエリ               | フォルダをコピーする宛先ストレージの名前です。                 |

### サンプル応答

正常な呼び出しは、空の JSON 本文を含む **HTTP 200** を返します：

```json
{}
```

**サンプル cURL リクエスト**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                       |
| ------ | -------------------- | ---------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用された。応答には操作の詳細が含まれる。 |
| 400    | Bad Request（不正なリクエスト） | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized（未認証）   | JWT トークンが無効または不足している。                      |
| 413    | Payload Too Large（ペイロードが大きすぎる） | アップロードされたファイルがサイズ制限を超えた。             |
| 500    | Internal Server Error（内部サーバーエラー） | サーバーで予期せぬエラーが発生した。                         |

## OpenAPI スペック

[OpenAPI スペック](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 経由の操作を実行できるようにします。

cURL コマンドラインツールを使用すれば、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

SDK を使用すると、開発を最速で進められます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスに呼び出しを行う方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}