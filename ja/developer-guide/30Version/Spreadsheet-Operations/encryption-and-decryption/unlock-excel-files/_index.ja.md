---
title: "Excel ファイルのロックを解除する"
second_title: "ドキュメント"
linktitle: "Excel ファイルのロックを解除する"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "Excel のロック解除, Aspose.Cells Cloud, REST API, Excel ロック解除, パスワード保護されたワークブック, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Aspose.Cells Cloud REST API は、パスワードで保護された Excel ファイルのロックを解除するためのエンドポイントを提供します。SDK は Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift を含む複数のプログラミング言語で利用可能です。"
ArticleTitle: "Aspose.Cells Cloud REST API を使用して Excel ファイルのロックを解除する"
weight: 70
---

この REST API は、Excel ファイルのロックを解除します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置                 | 説明                                     |
| ------------ | ------ | -------------------- | ---------------------------------------- |
| file         | file   | formData (HTTP ボディ) | アップロードするファイル                 |
| password     | string | クエリ文字列         | ファイルのロックを解除するためのパスワード (保護されている場合) |

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明                                               |
| ------ | ---------------- | -------------------------------------------------- |
| 200  | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request      | パラメータが不足しているか無効です (例: サポートされていないファイル形式)。 |
| 401  | Unauthorized     | JWT トークンが無効または不足しています。            |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | サーバーで予期しないエラーが発生しました。         |

## SDK を使用した PostUnlock API の利用方法

### PostUnlock API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) は公開可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクションを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発速度を大幅に向上させることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

**注意事項**  
- この API は、単一のリクエストで複数の Excel ファイルのロックを解除できます。各ファイルはレスポンスの `Files` 配列に返されます。  
- SDK のバージョンが API バージョン (`v3.0`) と一致することを確認し、互換性の問題を回避してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}