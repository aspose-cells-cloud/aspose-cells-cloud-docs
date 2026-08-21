---
title: "フォルダの作成 – Aspose.Cells Cloud API | Excel ストレージ管理"
second_title: "ドキュメント"
ArticleTitle: "フォルダの作成 – Aspose.Cells Cloud API"
linktype: "docs"
url: /ja/create-folder/
keywords: "Aspose.Cells, Cloud API, フォルダの作成, ストレージ管理, Excel"
description: "Aspose.Cells Cloud ストレージに新しいフォルダを、シンプルな PUT リクエストで作成します。リクエスト形式、パラメータ、レスポンス、エラー処理を確認してください。"
weight: 100
---

**createFolder** 操作は、Excel API が使用するクラウドストレージ内の指定された場所に新しいフォルダを作成します。これはファイルの整理と構造化されたディレクトリ階層の維持に不可欠です。

## **Excel API: フォルダの作成**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **createFolder** API のリクエストパラメータは以下の通りです

| パラメータ名   | タイプ   | 位置   | 必須 | デフォルト | 説明                                                                 |
| -------------- | ------ | ------ | ---- | ---------- | ------------------------------------------------------------------- |
| `path`         | 文字列 | パス   | はい  | –          | 作成するフォルダのパス（例: `myFolder/subFolder`）                |
| `storageName`  | 文字列 | クエリ | いいえ | –          | 使用するストレージの名前。省略された場合、デフォルトストレージが適用されます。 |

### レスポンスの説明

```json
{}
```

この操作は成功時にコンテンツを返しません。典型的な HTTP ステータスコードは以下の通りです。

**HTTP ステータスコード**

| HTTP コード | HTTP ステータス        | 説明                                                          |
| ----------- | ---------------------- | ------------------------------------------------------------- |
| 200         | OK（成功）             | Web API が正常に呼び出された。レスポンスには操作の詳細が含まれます。 |
| 400         | Bad Request（不正なリクエスト） | パラメータが不足または無効（例: 未対応のファイル形式）            |
| 401         | Unauthorized（認証エラー）   | JWT トークンが無効または不足しています                            |
| 413         | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています              |
| 500         | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました                            |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発 speed を大幅に向上させることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}