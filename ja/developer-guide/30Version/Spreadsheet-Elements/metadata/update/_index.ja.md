---
title: "メタデータの更新"
second_title: "ドキュメント"
linktitle: "ストレージを使わずに更新"
type: docs
url: /metadata/update/
keywords: "メタデータ, Excel, Aspose.Cells Cloud, REST API, 更新, スプレッドシート"
description: "Aspose.Cells Cloud REST API は、Excel ファイル内のメタデータを更新することを可能にします。複数のプログラミング言語（C#、Java、Python、Ruby、Go など）に対応する多数の SDK をサポートし、シームレスな統合を実現します。"
weight: 35
ArticleTitle: "メタデータの更新 – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、複数の Excel ファイルにおける**メタデータ**を更新します。

**前提条件:** アクティブな Aspose Cloud アカウント、有効な JWT アクセストークン、およびアップロード対象の Excel ファイル。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名       | 型     | 位置             | 説明                                     |
| ------------------ | ------ | ---------------- | ---------------------------------------- |
| file               | ファイル | formData         | アップロードする Excel ファイル。       |
| DocumentProperties | オブジェクト | HTTP 本体 (JSON) | Excel ファイルに設定するドキュメントプロパティ。 |

**注意事項:** 単一のリクエストで最大 10 個のファイルをアップロード可能です。対応フォーマットは `.xlsx`、`.xls`、`.csv` です。リクエスト全体のサイズは 100 MB を超えてはいけません。

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/PostMetadata) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

リクエストには、Bearer JWT トークンを含む **Authorization** ヘッダーが必要です。トークンは Aspose Cloud のクライアント認証情報を使って生成されたものを使用してください。

{{< /tab >}}

{{< tab tabNum="12" >}}

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

## クラウド SDK ファミリー

SDK を使用することで、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目:**  
- [メタデータの取得](/metadata/get/)  
- [メタデータの削除](/metadata/delete/)  
---